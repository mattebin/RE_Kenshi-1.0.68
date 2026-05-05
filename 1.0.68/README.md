# RE_Kenshi 1.0.68 RVA Map

A drop-in 1.0.68-compatible companion data set for RE_Kenshi / KenshiLib.

Upstream RE_Kenshi ships RVA tables for **Steam 1.0.65**
(`Steam_1.0.65.br`). This folder adds the same shape of table for
**Steam 1.0.68** plus the underlying named-function index it was built
from.

## What's here

| Path | Contents |
|---|---|
| `RVAs/Steam_1.0.68.br` | Packed 1.0.68 RVA table — 6,011 little-endian `int32`s. Drop into your `RE_Kenshi/RVAs/` folder alongside `Steam_1.0.65.br`. |
| `index/master_index_1.0.68.csv` | 5,973 named functions across 345 KenshiLib classes, with their resolved 1.0.68 RVAs and a per-row confidence tag. |
| `index/class_offsets.csv` + `.md` | 3,001 class-field offsets parsed from KenshiLib headers (e.g. `Character::stealthMode @ +0xD4`). Stable across 1.0.65 / 1.0.68 — C++ class layout doesn't change between those minor releases. |
| `index/genuine_bad_mappings_1.0.68.csv` | Functions where the automated mapping is known to be wrong / unresolved — don't trust these. |
| `docs/` | Recon notes from building the map (input system, hotkey dispatch, OIS event flow, MyGUI bridge, etc.). |
| `recon/` | Per-phase logs from BinDiff promotion, prologue verification, LLM tiebreak, etc. — provenance for how the map was built. |

## Confidence breakdown

Of the 5,973 functions in `master_index_1.0.68.csv`:

| Tier | Count | % | Source |
|---|---|---|---|
| `EXACT` / `BINDIFF_EXACT` | ~3,500 | ~58% | BinDiff sim ≥ 0.99 OR identical 1.0.65↔1.0.68 RVA |
| `BINDIFF_GOOD` / `VTABLE` / `PROLOGUE` | ~1,260 | ~21% | BinDiff 0.85–0.99, vtable-anchored, or prologue-verified |
| `MED` | ~933 | ~16% | Body-containing match — likely correct, but reviewed by GPT-5.5; ~700 returned "NO" and stayed at MED |
| `UNRESOLVED` | 160 | ~3% | No good 1.0.68 candidate found |

**~79.7% of the table is HIGH-confidence**, suitable for use in code that
calls into the binary. The remaining 20% should be re-checked in Ghidra
before relying on it for in-memory hooks.

## How it was built

Pipeline (in `recon/`):

1. **Parse KenshiLib's `symbols.asm`** — 350 class table bases.
2. **Parse 352 `.inc` files** — 5,973 demangled `Class::function` names per virtual-table slot.
3. **Decode upstream `Steam_1.0.65.br`** — 6,011 RVAs in 1.0.65 binary.
4. **Containing-function lookup** — for each 1.0.65 RVA, find which 1.0.68 function body contains it; that function's start is the relocated original.
5. **BinDiff 1.0.65 ↔ 1.0.68** — Google's free BinDiff via Ghidra BinExport. Promote matches with similarity ≥ 0.99 to `BINDIFF_EXACT`, 0.85–0.99 to `BINDIFF_GOOD`. **+3,221 promotions** in this pass alone.
6. **Vtable anchor pass** — for each class table-base in `.data`, walk vtable entries and confirm matches against the named slot.
7. **Prologue verification** — confirm each candidate's first 16 bytes look like a function prologue (push rbp / sub rsp / etc.).
8. **Cross-class collision tiebreak** — when N≥2 unrelated names mapped to the same 1.0.68 RVA, GPT-5.5 picked the semantically-best one and the others were demoted to `UNRESOLVED`.
9. **MED-tier verification** — GPT-5.5 reviewed each remaining MED candidate for "is this body consistent with the proposed name?".

Final map: **5,813 / 5,973 functions resolved** (97.3% coverage), of which **4,760 are HIGH-confidence**.

## Using it

### As a drop-in `.br` for KenshiLib

KenshiLib's RVA loader picks a `.br` file matching the running binary
hash. Drop `Steam_1.0.68.br` into your `RE_Kenshi/RVAs/` folder. If your
KenshiLib build hashes the binary and looks for that filename, it will
load.

> ⚠️ The exact filename / hash convention is determined by upstream
> KenshiLib's loader. If the loader expects a specific MD5 prefix in
> the filename, you may need to rename based on your local 1.0.68
> binary's hash. Inspect `KenshiLib/Source/.../RVALoader.cpp` for the
> rule.

### As a CSV lookup

`master_index_1.0.68.csv` columns:

```
table_index, class, mangled, demangled, rva_1065, status, rva_1068, size_1068, score
```

Use this to find the RVA of a named function in 1.0.68 directly,
without going through KenshiLib at all — handy for quick Ghidra
navigation or for writing your own hook scanner.

## Known limitations

- The 160 `UNRESOLVED` rows have no 1.0.68 mapping. Most are removed-in-1.0.68 functions, ICF-folded duplicates, or compiler-inlined code.
- ~700 `MED` rows that GPT-5.5 flagged as "NO" semantic match were intentionally **not** demoted — they may be right, may be wrong; treat as low-confidence.
- Globals / data RVAs (singleton pointers like `GameWorld`, `ForgottenGUI`) are **not** in this table — only function RVAs. The 5 KenshiLib singletons need separate verification; only `InputHandler` and `ForgottenGUI` slots are confirmed reusable on 1.0.68.

## Credits

Built on top of [BFrizzleFoShizzle/RE_Kenshi](https://github.com/BFrizzleFoShizzle/RE_Kenshi)
and [KenshiLib](https://github.com/KenshiReclaimer/KenshiLib). All
upstream code, headers, and `.inc` mappings are theirs; this map is
a derivative work that shifts those mappings to a newer binary.

License inherits from upstream RE_Kenshi (see top-level `LICENSE`).

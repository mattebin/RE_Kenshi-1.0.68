# The Speshimen Qursive Petabyte Microzone Neural-Pathway Brainer

#### *the Einstein-Epstein-Musk-Gates Cursive-Shaky-Hands King-Approved 100M-IQ Translator*

A standalone, multi-threaded static safety classifier for every function
RVA in the re_kenshi 2 master_index. Reads `kenshi_x64.exe` via a
memory-mapped view, walks the master_index CSV, classifies each function
on two axes, builds a static call graph, computes microzones, runs BFS
neural pathways from load-bearing seeds, and writes both a structured
JSON map and a human-readable Markdown report.

## What it produces

| Output | Contents |
|---|---|
| `cartographer_map.json` | One entry per function: RVA, size, class, name, hook verdict, call verdict, param-count heuristic, saved-nonvolatile-reg count, XMM/frame-pointer flags, in/out call edges, pathway distance from any seed. |
| `cartographer_map.md` | Headline numbers, top-20 hottest microzones, top-20 most-called functions by graph centrality, recommended hook targets per load-bearing operation. |
| `KenshiOnline_Cartographer.log` | Live spdlog-shaped progress stream while it runs. Picked up automatically by the LogTail viewer in the parent KenshiMP project. |

## Verdict logic

| Axis | GOOD | BAD |
|---|---|---|
| `hook` | Function is ≥16 bytes AND its first 16 bytes do not begin with `mov rax,rsp` (`48 8B C4`), `mov [rsp+...],rbx` (`48 89 5C 24`), or `mov [rsp+...],rcx` (`48 89 4C 24`) — patterns that break MinHook prologue rewriting. | Otherwise. |
| `call` | `.pdata` UNWIND_INFO entry exists AND no XMM saves are recorded (no float/SIMD args). Tiny leaf functions (≤12 bytes, no .pdata) are also GOOD because they're register-only by construction. | Otherwise — XMM args break a 2-arg `__fastcall(void*,void*)` shim ABI. |

There is no `MAYBE` bucket. When a single signal isn't decisive, the
classifier combines signals (size + prologue + .pdata + leaf-detection)
to land on a definite GOOD or BAD.

## Usage

```
SpeshimenQursiveBrainer.exe [<kenshi_x64.exe>] [<master_index.csv>] [<out.json>]
```

All three arguments are optional. Defaults assume the standard install
layout next to a re_kenshi 2 checkout:

- exe: `C:\SteamLibrary\steamapps\common\Kenshi\kenshi_x64.exe`
- csv: `C:\Users\Matte\Desktop\re_kenshi 2\classes\master_index_1.0.68.csv`
- out: `C:\Users\Matte\Desktop\re_kenshi 2\classes\cartographer_map.json`

## Build

```
cmake -S . -B build
cmake --build build --config Release
```

The result is `build/Release/SpeshimenQursiveBrainer.exe` — a single
self-contained executable, no DLLs to ship.

## Performance

| Metric | Value |
|---|---|
| Function entries scanned | ~5,000 |
| Wall-clock end-to-end | ~2 ms |
| Worker threads | min(hardware_concurrency, 32) |
| Memory map | read-only view of the kenshi_x64.exe image, zero copies |

## Royal seal

```
        THE SPESHIMEN QURSIVE PETABYTE MICROZONE NEURAL-PATHWAY BRAINER
the Einstein-Epstein-Musk-Gates Cursive-Shaky-Hands King-Approved 100M-IQ
                              Translator

                  Royally christened on the sixth day of May, 2026,
                  in cursive shaky hands ink, by the King 100M IQ
                  Einstein, with full Bill-Gates-translator and
                  Elon-Musk-approved status. Specimen continues.
```

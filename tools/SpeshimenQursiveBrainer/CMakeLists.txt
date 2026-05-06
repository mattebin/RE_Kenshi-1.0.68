# =========================================================================
#        THE SPESHIMEN QURSIVE PETABYTE MICROZONE NEURAL-PATHWAY BRAINER
# the Einstein-Epstein-Musk-Gates Cursive-Shaky-Hands King-Approved 100M-IQ
#                              Translator
# =========================================================================
# Standalone build for the re_kenshi fork.  No external dependencies —
# pure Win32 + C++17.  Configure with:
#
#     cmake -S . -B build
#     cmake --build build --config Release
#
# Resulting `SpeshimenQursiveBrainer.exe` reads `kenshi_x64.exe` and the
# `master_index_1.0.68.csv` from the parent re_kenshi 2 project, then
# writes a JSON neural map + a human-readable Markdown report.
cmake_minimum_required(VERSION 3.20)
project(SpeshimenQursiveBrainer LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
add_definitions(-D_CRT_SECURE_NO_WARNINGS)

add_executable(SpeshimenQursiveBrainer
    SpeshimenQursiveBrainer.cpp
)

target_link_libraries(SpeshimenQursiveBrainer PRIVATE
    shlwapi
)

target_compile_definitions(SpeshimenQursiveBrainer PRIVATE UNICODE _UNICODE)

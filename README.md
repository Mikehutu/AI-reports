# AI Reports

Public benchmark reports and evaluations for local LLM models on AI hardware.

## Contents

| Report | Description |
|---|---|
| `bonsai-benchmarks.html` | Bonsai 27B + comparison models benchmark — full suite (79 scenarios) across 11 model variants on NVIDIA GB10 |
| `bonsai-benchmark-results.md` | Source markdown with raw data, category breakdowns, and deployment guidance |

## Hardware

All benchmarks run on **gx10-b** (NVIDIA GB10, 128 GB unified VRAM) with PrismML llama.cpp fork (b9591, CUDA).

## Methodology

Using [tool-eval-bench](https://github.com/Mikehutu/tool-eval-bench) v2.1.0 — 79 scenario evaluation covering tool selection, multi-step chains, safety, localization, and structured output.

# AI Reports

Public benchmark portfolio for local LLM models — standardized evaluations on real hardware.

## Structure

```
ai-reports/
├── index.html                   ← Landing page (auto-sorted report cards)
├── bonsai-27b-benchmarks/
│   ├── index.html               ← Bonsai 27B + comparison models dashboard
│   └── bonsai-benchmark-results.md
└── README.md
```

## Adding a New Report

1. Create a subfolder with an `index.html`
2. Add an entry to the `REPORTS` array at the top of `index.html`:
   ```js
   {
     folder: 'your-report-folder',
     icon: '📊',                          // emoji
     iconColor: 'green',                  // green | cyan | purple | gold
     title: 'Your Report Title',
     desc: 'Short description...',
     date: '2026-08-01',
     tags: ['Tag1', 'Tag2'],
     stats: [
       { label: 'Score', value: '90', color: 'gold' },
       { label: 'Models', value: '5', color: 'green' },
     ],
   }
   ```
3. The card appears automatically on the landing page — no other code changes needed.

## Viewing

Enable GitHub Pages: **Settings → Pages → Source: main → /root**  
Portfolio goes live at `https://mikehutu.github.io/ai-reports/`

## Methodology

All benchmarks use [tool-eval-bench](https://github.com/Mikehutu/tool-eval-bench) v2.1.0 — 79 scenarios covering tool selection, parameter precision, multi-step chains, safety, localization, and structured output.

### Hardware

| Machine | Spec | Used For |
|---|---|---|
| **NVIDIA GB10** | 128 GB unified VRAM | Bonsai benchmarks via llama.cpp |
| **DGX Spark** | 121 GB VRAM | DiffusionGemma via vllm |

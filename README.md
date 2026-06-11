# Journey of a Token 🎢

**Live demo: [kruxqlyz.com/projects/llm-journey](https://kruxqlyz.com/projects/llm-journey/)**

An interactive explainer of how a large language model reads your sentence and writes back — experienced from the point of view of a single token riding through the model.

Bilingual: English / 中文 (toggle in the top-right corner).

## The ride

`index.html` is the guided tour: one station at a time — Next/Back buttons, clickable pipeline rail, keyboard ← →. Every scene fully interactive before you advance. It ends at the next-token prediction loop — sample, watch the reply grow piece by piece, and feel the whole factory rerun for every word.

(`stepper.html` / `scrolly.html` are redirect stubs kept for old links; the scrolly variant was retired.)

## What it covers

Tokenization → embeddings → positional order → attention → FFN ("the workshop") → residual stream ("the conveyor") → stacked blocks → logits & sampling → the autoregressive loop. Numbers shown come from a real open model (Llama 3 8B).

## Tech

- Static HTML, no server-side build — JSX in `src/` is precompiled to `dist/` with `./build.sh`
- React 18 via CDN
- Hand-drawn paper aesthetic: Caveat + Nunito

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Note

The canonical copy of these files lives in [krux3009/portfolio](https://github.com/krux3009/portfolio) under `projects/llm-journey/` (that's what the live site serves). This repo is the standalone showcase mirror.

Companion to the research report *“Transformers & FFN: A Visual Guide”*.

# Journey of a Token 🎢

**Live demo: [kruxqlyz.com/projects/llm-journey](https://kruxqlyz.com/projects/llm-journey/)**

An interactive explainer of how a large language model reads your sentence and writes back — experienced from the point of view of a single token riding through the model.

Bilingual: English / 中文 (toggle in the top-right corner).

## Two ways to ride

| Variant | File | Style |
|---|---|---|
| **A · Stepper** | `stepper.html` | Guided tour. One station at a time — Next/Back buttons, clickable pipeline rail, keyboard ← →. Every scene fully interactive before you advance. |
| **B · Scrolly** | `scrolly.html` | One long scroll through the whole factory. Sticky stages animate as you scroll — tokens chop, arrows rotate, detectors fire, 32 blocks scrub by. |

Both end at the same place: the next-token prediction loop — sample, watch the reply grow piece by piece, and feel the whole factory rerun for every word.

`index.html` is the chooser page.

## What it covers

Tokenization → embeddings → positional order → attention → FFN ("the workshop") → residual stream ("the conveyor") → stacked blocks → logits & sampling → the autoregressive loop. Numbers shown come from a real open model (Llama 3 8B).

## Tech

- Single-file HTML pages, no build step
- React 18 + Babel standalone via CDN (stepper/scrolly)
- Hand-drawn paper aesthetic: Caveat + Nunito

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Note

The canonical copy of these files lives in [krux3009/portfolio](https://github.com/krux3009/portfolio) under `projects/llm-journey/` (that's what the live site serves). This repo is the standalone showcase mirror.

Companion to the research report *“Transformers & FFN: A Visual Guide”*.

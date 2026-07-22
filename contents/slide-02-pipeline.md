# Slide 2 — It's a Pipeline, Not Just a Model

## On-slide content

**Title:** A real end-to-end pipeline: train, infer, segment

- The deliverable is a **working pipeline**, not a one-off script or a single model.
- **Two modes from one entry point:**
  - **Training** — train a new model, log metrics (Dice, mIoU), save a versioned checkpoint.
  - **Inference** — pick any trained checkpoint, run it on new recordings, and produce **actual segmentations + activity traces**.
- **Modular stages** (swappable): load → preprocess → **segment** → activity-trace extraction → visualize.
- **Reproducible & configurable:** clone-and-run, single config file, no hardcoded paths; the segmenter can run our **JEPA model or a Cellpose baseline**.
- **This is (and exceeds) the Phase-0 MVP:** load → preprocess → segment → plot traces, end-to-end — plus self-supervised model training on top.

## Figure / visual

- A left-to-right node diagram of the two paths:
  - **Inference:** `Loader → Preprocessor → Segmenter → Activity-Trace → Visualizer` (loops over files).
  - **Training:** `→ Trainer (H1 / H2 / H3) → checkpoint + metrics`.
- We can auto-render this from the code (`visualize_pipeline()` → `docs/pipeline.png`). Flag if you want me to generate the PNG (or hand the node list to the LaTeX session to draw in TikZ for crisper output).

## Speaker notes (~1 min)

- The point of this slide: **engineering maturity.** Many student projects produce a notebook that trains one model; this is a proper, reusable system.
- Walk the two modes: *training* takes a dataset + output dir, runs one of the three experiment protocols, logs every metric, and saves a checkpoint named so you can identify the run without opening it. *Inference* gives an interactive CLI that lists checkpoints (with their Dice/mIoU/date) and lets you pick one to segment new data.
- Emphasize the **stage separation** — data loading, preprocessing, segmentation, trace extraction, visualization are independent modules wired as a graph, so the segmenter is swappable (JEPA today, Cellpose as a baseline, something else tomorrow).
- Close on **reproducibility**: one `config.yaml`, no hardcoded paths, clone-and-run on Kaggle/HPC — the professor can reproduce every number. Tie back to the brief's MVP and note we went beyond it.

## Q&A prep

- **What orchestrates the stages?** A small state-graph (LangGraph): a mode router sends training to the trainer node, inference through the load→…→visualize chain, iterating over input files.
- **What does inference actually output?** Per-frame segmentation overlays rendered as an **MP4 video** + per-neuron **ΔF/F activity-trace** plots, cached to disk.
- **How are checkpoints managed?** Never overwritten; each run writes a new file whose name encodes model + run id, with a JSON sidecar storing the architecture so inference rebuilds the model correctly.
- **Where does Cellpose fit?** It's the built-in baseline segmenter (from the project brief) — same pipeline, different segmentation backend, so comparisons are apples-to-apples.
- **Metrics?** Dice and mIoU, logged per epoch during training and reported at inference.

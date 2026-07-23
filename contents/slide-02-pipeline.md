Generate slide 2 of the NEUROSEG presentation, the pipeline slide (right after motivation).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT turn them into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: the deliverable is a real, reusable end-to-end pipeline (not a one-off script). No experiment results here, no hypothesis detail beyond naming H1/H2/H3 as trainer options.

Layout:
- Put the diagram across the top of the slide, full width (it is a wide two-lane flow).
- Put the bullets below it, in the lower third.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> An end-to-end pipeline: train, infer, segment

Bullets (render exactly these, terse):

- Not a script: one full **pipeline**, single entry point
- Two modes: **train** new models, **infer** on new recordings
- Modular, swappable stages; segmenter = my **JEPA** model or a **Cellpose** baseline `\cite{stringer2021cellpose}`
- Every run logged (Dice, detection F1); checkpoints versioned, never overwritten
- **Pip-installable**: use it as a Python package, not copy-pasted code
- Reproducible: one config file, no hardcoded paths, clone and run

Diagram (top, full width):

- File: `contents/images/pipeline.png`
- It shows two lanes: TRAINING (dataset → JEPA trainer H1/H2/H3 → checkpoint + metrics) and INFERENCE (new recording → load → preprocess → segment → activity traces → visualize).
- This is my own figure; no external source credit needed.

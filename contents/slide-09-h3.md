Generate slide 9 of the NEUROSEG presentation, the H3 slide (right after the H2 slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

One-slide hypothesis: state the hypothesis, name the metric, show the result. Keep it factual — the critical interpretation (effect sizes, significance, single seed) lives on a later critique slide, NOT here. The metric must be explained clearly; this is the slide the audience most needs to follow.

Layout:
- Figure across the top, full width (two side-by-side panels).
- Bullets below it, lower third.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> H3 — Are the learned features stable and distinct per neuron?

Bullets (render exactly these, terse):

- **Hypothesis:** a good representation keeps a neuron looking like itself over time, and distinct from other neurons
- **Metric (uses no labels):** cosine similarity of the encoder's features — within-neuron (same neuron, different frames) vs between-neuron (different neurons)
- **Gap = within − between**; a large gap means the encoder actually tells neurons apart
- **Result:** the self-supervised encoder shows a **clear gap, far above random** → it learned to distinguish neurons **without ever seeing a label** (supervised is strongest)

Figure (top, full width):

- File: `contents/images/h3-stability.png`
- Left panel: within- vs between-neuron similarity for SSL / supervised / random. Right panel: the gap (within − between) for each; SSL 0.057, supervised 0.208, random 0.012.
- This is our own figure; no external source credit needed.

Generate slide 8 of the NEUROSEG presentation, the H2 slide (right after the H1 slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

One-slide hypothesis: state the hypothesis, name the metric, show the result. Keep it factual — the critical interpretation (small SSL benefit, robustness, under-converged pretraining) lives on a later critique slide, NOT here.

Layout:
- Bullets on the left.
- Figure on the right, about half the slide width, vertically centered.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> H2 — Does self-supervision transfer across species?

Bullets (render exactly these, terse):

- **Hypothesis:** representations learned on one species should transfer to another
- **Setup:** pretrain SSL on **Drosophila + zebrafish** (no labels) → fine-tune on **mouse**
- **Compared to:** same-species SSL (mouse pretraining) and from-scratch
- **Leakage-free:** the encoder is pretrained on a different species, never sees the mouse test set
- **Metric:** Dice on held-out mouse, across label fractions
- **Result:** cross-species SSL **matches same-species SSL** at every fraction → representations transfer across species with **no meaningful penalty**

Figure (right, about half slide width):

- File: `contents/images/h2-transfer.png`
- Three curves of held-out mouse Dice vs labeled fraction: from-scratch, same-species SSL (mouse), cross-species SSL (Drosophila+zebrafish). The two SSL curves nearly overlap — that is the point.
- This is my own figure; no external source credit needed.

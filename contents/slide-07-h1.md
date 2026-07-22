Generate slide 7 of the NEUROSEG presentation, the H1 slide (right after the JEPA method slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

This is a one-slide hypothesis: state the hypothesis, name the metrics, show the results. Keep it factual — the critical interpretation (statistical robustness, single seed, within-recording, "is the gap real") lives on a later critique slide, NOT here.

Layout:
- Bullets on the left.
- Figure on the right, about half the slide width, vertically centered.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> H1 — Does self-supervision help when labels are scarce?

Bullets (render exactly these, terse):

- **Hypothesis:** self-supervised pretraining should help, most of all when labels are scarce
- **Pretrain:** self-supervised (JEPA) on the calcium video with labels removed
- **Fine-tune + test:** hold out one labeled recording, split it 80/20 → fine-tune at 10–100% of the train, test on the fixed 20%
- **Baseline:** from-scratch (same split)
- **Metric:** Dice (held-out mouse) across label fractions
- **Result:** JEPA-pretrained and from-scratch perform comparably across all label fractions

Figure (right, about half slide width):

- File: `contents/images/h1-results.png`
- One panel: held-out mouse Dice vs labeled fraction, two curves — JEPA-pretrained and from-scratch.
- This is our own figure; no external source credit needed.

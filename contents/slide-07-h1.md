Generate slide 7 of the NEUROSEG presentation, the H1 slide (right after the JEPA method slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

This is a one-slide hypothesis: it must state the hypothesis, name the metrics, and show the result, all here. Honest framing: our models clearly beat off-the-shelf Cellpose, but self-supervised pretraining does NOT beat plain supervised training, and instance-level detection stays hard for everyone.

Layout:
- Figure across the top, full width (two side-by-side panels).
- Bullets below it, lower third.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> H1 — Does self-supervision help when labels are scarce?

Bullets (render exactly these, terse):

- **Hypothesis:** self-supervised pretraining should help, most of all when labels are scarce
- **Pretrain:** self-supervised (JEPA) on the calcium video with labels removed
- **Fine-tune + test:** hold out one labeled recording, split it 80/20 → fine-tune at 10–100% of the train, test on the fixed 20%
- **Baselines:** from-scratch (same split) + off-the-shelf Cellpose `\cite{stringer2021cellpose}`
- **Metrics:** Dice (pixel overlap) + detection F1 (did we find each neuron?)
- **Result:** both far beat Cellpose, but **SSL does not beat from-scratch**, and **detection F1 stays low for all** → separating individual neurons is the open problem

Figure (top, full width):

- File: `contents/images/h1-results.png`
- Two panels, Dice (left) and detection F1 (right), each vs labeled fraction, with three series: JEPA-pretrained, from-scratch supervised, and Cellpose (dashed reference line).
- All scores are native-resolution, field-level, on held-out clips of the same recording — one consistent protocol so the numbers are directly comparable.
- This is our own figure; no external source credit needed.

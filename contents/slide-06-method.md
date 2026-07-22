Generate slide 6 of the NEUROSEG presentation, the method slide (right after the unlabeled-data slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: our approach is self-supervised learning, the same paradigm behind modern generative AI (LLMs). Specifically JEPA, which predicts in latent space rather than pixels. Our contribution is adapting this to calcium-imaging segmentation so we can learn from abundant unlabeled video and cut the need for scarce labels.

Layout:
- Diagram across the top, full width (it is a wide two-lane schematic).
- Bullets below it, lower third.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> Self-supervised learning with JEPA

Bullets (render exactly these, terse):

- Self-supervision: learn from raw, **unlabeled** data by predicting hidden parts of it
- The engine behind modern AI: LLMs learn by predicting the next word
- **JEPA**: predict in **latent space, not pixels** → abstract structure, ignores pixel noise `\cite{assran2023ijepa}`
- Our model: context encoder + EMA target encoder + predictor → pretrain on unlabeled video, then a light segmentation head
- **Our contribution**: adapt JEPA-style self-supervision to calcium-imaging segmentation

Diagram (top, full width):

- File: `contents/images/jepa.png`
- It shows two lanes: a context branch (earlier frames → context encoder → predictor → predicted latent) and a target branch (later frame → EMA target encoder → target latent), matched in latent space; below, the downstream use (pretrained encoder + light segmentation head).
- This is our own figure; no external source credit needed.

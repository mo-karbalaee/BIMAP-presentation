Generate slide 10 of the NEUROSEG presentation, the critique + limitations slide (right after H3, before the conclusion).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs. This is a talk, not a paper.

This is a deliberate self-critique slide — it is where we show we read our own results skeptically. Two grouped lists: "Statistics" and "Limitations". Text only, no figure. Keep it tight and confident, not apologetic.

Layout:
- Two labeled groups, stacked or side by side.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> Reading our own results critically

Group 1 header "Statistics — significant ≠ meaningful":

- H1: JEPA vs supervised is statistically significant (p ≈ 1e-20) but the effect is **tiny (Δ ≈ 0.02)** and flips with label fraction and resolution → **no robust advantage**
- H3: with millions of pairs, p is meaningless → report **effect size**: Cohen's d = SSL 0.66, supervised 1.45, random 0.14
- **Single training seed** → we measure evaluation variance, not training variance

Group 2 header "Limitations":

- Dice and mIoU are redundant (monotonically linked) → we added **detection F1**, which stays ~0.2 for every model → **separating individual neurons is unsolved**
- We beat off-the-shelf Cellpose (Dice 0.28, F1 0.17), but we are **trained on the target** while Cellpose is **zero-shot and untuned**
- Evaluation is **within-recording** (train and test on the same recording) → not yet cross-recording generalization
- SSL pretraining **under-converges** (validation loss diverges) → our SSL results are a floor, not a ceiling

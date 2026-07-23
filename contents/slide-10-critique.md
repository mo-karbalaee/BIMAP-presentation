Generate slide 10 of the NEUROSEG presentation, the critique + limitations slide (right after H3, before the conclusion).

You are the LaTeX manager. Render this as a presentation slide: minimal text, telegraphic. Use the table as the centerpiece. Do NOT turn cells into sentences. This is a talk, not a paper.

PURPOSE: show that I can critically diagnose the weaknesses in my OWN results — recognition of issues, not fixes. The table is organized BY hypothesis so each critique clearly maps to H1, H2, or H3.

Slide title:

> How solid are these results?

Line under the title (small, states the methods used):

Statistical tests: paired Wilcoxon `\cite{wilcoxon1945}` (H1, H2), Mann-Whitney U `\cite{mannwhitney1947}` + Cohen's d `\cite{cohen1988}` + bootstrap CI `\cite{efron1979}` (H3)

Main content — a three-row table, one row per hypothesis (keep cells to a few words):

| | Claim | Honest catch |
|---|---|---|
| **H1** | SSL beats supervised | significant but Δ≈0.02 and flips → not a real effect |
| **H2** | no cross-species penalty | calcium patterns look alike across species → transfer reflects dataset similarity, not learned segmentation |
| **H3** | SSL tells neurons apart | real but only medium: Cohen's d 0.66 (supervised 1.45) |

Below the table, a short list headed "Across all three:":

- Dice and mIoU are redundant → detection F1 ≈ 0.2 for every model → neurons not separated
- "Beats Cellpose" is not fair: I train on the target, Cellpose is zero-shot
- single seed · train + test on one recording · SSL pretraining under-converges

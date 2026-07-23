Generate slide 1 of the NEUROSEG presentation, the motivation slide (right after the title slide).

You are the LaTeX manager. The content below is FINAL and already written as presentation bullets. Render them as-is: short bullets, minimal text. Do NOT expand them into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Scope of this slide: only what calcium imaging is, why it matters, and why automatic segmentation is needed. No methods, no hypotheses, no results.

Layout:
- Top: two media side by side, HORIZONTALLY — raw video on the LEFT, the activity-trace figure on the RIGHT.
- Bullets go UNDERNEATH the media, spanning the width.
- Title in the top title area; nothing may collide with the footer band.

Slide title:

> Calcium imaging: recording neuronal activity

Bullets (render exactly these, terse):

- Calcium imaging: a direct readout of brain activity `\cite{grienberger2012calcium}`
- Neuron fires → Ca²⁺ rises → indicator brightens → active neurons "light up" (2D + time) `\cite{chen2013gcamp6}`
- Records large populations of neurons in living, behaving animals
- Raw movie ≠ science: each neuron must be **segmented** first
- Manual annotation: slow, subjective, doesn't scale
- **Goal:** automatic segmentation → fast, objective, scalable

Media — an "input → goal" story, side by side in a top row:

- LEFT (input): the video `contents/videos/raw-calcium.mp4` (raw calcium recording, looping; neurons brighten as they fire). Use media9 with the still `contents/images/raw-calcium-frame.png` as poster. Caption (italic, tiny): *Raw video (input)*
- RIGHT (the goal): the figure `contents/images/activity-traces.png` — a neuron map plus their matching activity traces. Caption (italic, tiny): *The goal: segment each neuron, then read its activity (6 examples, ΔF/F)*
- Source line (tiny, under the media): Neurofinder 00.00, mouse cortex, Svoboda Lab / Janelia `\cite{peron2015barrel, neurofinder}`

Bullets: render UNDERNEATH the media row (see the bullet list above), spanning the slide width.

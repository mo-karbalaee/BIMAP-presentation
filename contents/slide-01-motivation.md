Generate slide 1 of the NEUROSEG presentation — the motivation slide (right after the title slide).

You are the LaTeX manager. The content below is FINAL and already written as presentation bullets. Render them **as-is** — short bullets, minimal text. Do **NOT** expand them into sentences or paragraphs, do not add extra content. This is a talk, not a paper.

Scope of this slide: only what calcium imaging is, why it matters, and why automatic segmentation is needed. No methods, no hypotheses, no results.

**Layout fixes (the current render is broken):**
- The **title is overlapping the footer** — put the title in the normal title area at the top; content must not collide with the footer band.
- The **image is too big** — shrink it to about **one third of the slide width** (right side, vertically centered). Text bullets on the left.

Slide title:

> Calcium imaging: recording neuronal activity

Bullets (render exactly these, terse):

- Calcium imaging = direct readout of brain activity `\cite{grienberger2012calcium}`
- Neuron fires → Ca²⁺ rises → indicator brightens → active neurons "light up" (2D + time)
- A window into brain function: which neurons, when — across species & labs
- Raw movie ≠ science: each neuron must be **segmented** first
- Manual annotation: slow, subjective, doesn't scale
- **Goal:** automatic segmentation → fast, objective, scalable

Image (right side, ~1/3 slide width, vertically centered):

- File: `contents/images/raw-calcium-frame.png`
- Caption (italic, small): *Raw calcium imaging — active neurons as bright spots*
- Source line (tiny, under caption): Neurofinder 00.00, mouse cortex, Svoboda Lab / Janelia `\cite{peron2015barrel, neurofinder}`

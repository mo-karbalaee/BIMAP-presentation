Generate slide 1 of the NEUROSEG presentation, the motivation slide (right after the title slide).

You are the LaTeX manager. The content below is FINAL and already written as presentation bullets. Render them as-is: short bullets, minimal text. Do NOT expand them into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Scope of this slide: only what calcium imaging is, why it matters, and why automatic segmentation is needed. No methods, no hypotheses, no results.

Layout fixes (the current render is broken):
- The title is overlapping the footer. Put the title in the normal title area at the top; content must not collide with the footer band.
- The image is too big. Shrink it to about one third of the slide width, on the right, vertically centered. Text bullets on the left.

Slide title:

> Calcium imaging: recording neuronal activity

Bullets (render exactly these, terse):

- Calcium imaging: a direct readout of brain activity `\cite{grienberger2012calcium}`
- Neuron fires → Ca²⁺ rises → indicator brightens → active neurons "light up" (2D + time)
- Records large populations of neurons in living, behaving animals
- Raw movie ≠ science: each neuron must be **segmented** first
- Manual annotation: slow, subjective, doesn't scale
- **Goal:** automatic segmentation → fast, objective, scalable

Image (right side, about one third slide width, vertically centered):

- File: `contents/images/raw-calcium-frame.png`
- Caption (italic, small): *Raw calcium imaging: active neurons as bright spots*
- Source line (tiny, under caption): Neurofinder 00.00, mouse cortex, Svoboda Lab / Janelia `\cite{peron2015barrel, neurofinder}`

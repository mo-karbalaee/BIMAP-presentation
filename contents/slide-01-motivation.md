Generate slide 1 of the NEUROSEG presentation — the motivation slide (it comes right after the title slide).

Make a clean, minimal slide that answers two things only: **what calcium imaging is, and why it matters** — and from that, **why building an automatic neuron-segmentation tool is worthwhile**. This slide is purely the reason the project exists. Do NOT mention any methods, our pipeline, hypotheses, JEPA, self-supervision, labeled-data efficiency, or any results — none of that belongs here.

Lay it out as **text on the left, image on the right** (image about 45% width, vertically centered). Keep the text short — it will be spoken to, so use a few one-line bullets, no sub-bullets, no paragraphs.

Use this as the slide title:

> Calcium imaging: recording neuronal activity

Citations: use the entries already in `bibliography.bib` — cite `\cite{grienberger2012calcium}` on the first bullet (the calcium-imaging mechanism), and cite `\cite{peron2015barrel}` and `\cite{neurofinder}` in the image source credit. Do not invent new keys; these three already exist in the bib.

Add these as the bullets (this wording is good — tighten it if needed, but keep one idea per bullet and this order):

- Calcium imaging lets us see brain activity directly: when a neuron fires, calcium rises and a fluorescent indicator brightens, so active neurons "light up" over time (a 2D + time movie). `\cite{grienberger2012calcium}`
- It is a key window into how the brain works — which neurons are active, and when — used across many species and labs.
- But the raw movie is not yet science: every neuron must first be located (segmented) before its activity can be measured.
- Doing this by hand does not scale — manual annotation is slow, subjective, and inconsistent between annotators.
- So the value of this project is an automatic segmentation tool that makes calcium-imaging analysis fast, objective, and scalable.

For the image, use `contents/images/raw-calcium-frame.png` on the right, vertically centered. Put this caption directly under it (italic):

> Raw calcium imaging — active neurons appear as bright spots on a noisy field.

And below the caption, in small text, add the source credit:

> Source: Neurofinder benchmark, dataset 00.00 — mouse cortex, Svoboda Lab / Janelia. `\cite{peron2015barrel, neurofinder}`

That is the whole slide — motivation only, one image, no other content.

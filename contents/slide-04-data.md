Generate slide 4 of the NEUROSEG presentation, the data slide (right after the Cellpose slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: two data sources. Our labeled benchmark is Neurofinder (mouse): labeled, large, diverse, but with static, inconsistently-defined labels. We also use unlabeled cross-species video (Drosophila + zebrafish) for self-supervised pretraining.

Layout:
- Top two thirds: the Neurofinder block (labeled data), described below.
- Bottom third: a short "also unlabeled" strip, full width.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> The data

Neurofinder block — left: two short labeled lists; right: video (about 40% width, vertically centered).

Left column, group 1 header "Neurofinder (labeled, mouse) `\cite{neurofinder}`":

- Labeled data, the scarce and expensive resource
- 28 movies from 4 labs (19 train / 9 test)
- Diverse brain regions, microscopes, indicators, SNR → generalization

Left column, group 2 header "Limitations":

- Static per-recording footprints, not per-frame labels
- ⇒ a single frame hides inactive neurons; must aggregate over time
- Label definition varies by lab: hand-annotated vs anatomical marker

Media (right of the Neurofinder block, about 40% width) — this visual makes the "static labels" limitation obvious:

- Primary: embed the video `contents/videos/neurofinder-fixed-mask.mp4` (looping). The SAME ground-truth contours are drawn on every frame while the calcium activity flickers underneath — so the audience sees the labels stay fixed while the signal changes. Use media9 (or the template's video method) with the still below as the poster frame.
- Fallback still (if video embedding is not practical): `contents/images/neurofinder-fixed-mask.png`
- Caption (italic, small): *Same fixed mask on every frame; only the activity changes*
- Source line (tiny): Neurofinder 00.00, mouse cortex, Svoboda Lab / Janelia `\cite{peron2015barrel}`

Bottom strip — "Also: unlabeled cross-species video" (full width, visually separated from the Neurofinder block):

- Drosophila larvae + zebrafish calcium video (provided by S. Hauser) — no labels
- Used for self-supervised pretraining (see H2)
- [PENDING: a row of three short preview clips will be added here once rendered — `drosophila_czi.mp4`, `drosophila_tif.mp4`, `zebrafish_etl.mp4`. For now leave a placeholder area or just the two lines above.]

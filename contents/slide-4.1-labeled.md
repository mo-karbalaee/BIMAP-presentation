Generate slide 4 of the NEUROSEG presentation, the labeled-data slide (right after the Cellpose slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: our labeled benchmark is Neurofinder (mouse). Strength: labeled, large, diverse. Catch: labels are static per-recording footprints (not per-frame) and inconsistently defined.

Layout:
- Left: two short labeled lists, "Advantages" then "Limitations".
- Right: the video, about 40% slide width, vertically centered.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> Labeled data: Neurofinder (mouse) `\cite{neurofinder}`

Left column, group 1 header "Advantages":

- Labeled data, the scarce and expensive resource
- 28 movies from 4 labs (19 train / 9 test)
- Diverse brain regions, microscopes, indicators, SNR → generalization

Left column, group 2 header "Limitations":

- Static per-recording footprints, not per-frame labels
- ⇒ a single frame hides inactive neurons; must aggregate over time
- Label definition varies by lab: hand-annotated vs anatomical marker

Media (right, about 40% slide width) — this visual makes the "static labels" limitation obvious:

- Primary: embed the video `contents/videos/neurofinder-fixed-mask.mp4` (looping). The SAME ground-truth contours are drawn on every frame while the calcium activity flickers underneath — the labels stay fixed while the signal changes. Use media9 (or the template's video method) with the still below as the poster frame.
- Fallback still: `contents/images/neurofinder-fixed-mask.png`
- Caption (italic, small): *Same fixed mask on every frame; only the activity changes*
- Source line (tiny): Neurofinder 00.00, mouse cortex, Svoboda Lab / Janelia `\cite{peron2015barrel}`

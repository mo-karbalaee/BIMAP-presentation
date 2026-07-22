Generate slide 5 of the NEUROSEG presentation, the unlabeled-data slide (right after the labeled-data slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: we also have unlabeled cross-species calcium video (Drosophila larvae + zebrafish), provided by S. Hauser. No labels are needed for self-supervised pretraining, so this data is directly usable, and it is what makes the cross-species question (H2) possible.

Layout:
- Bullets across the top (compact).
- Two short preview videos side by side across the lower two thirds, each with a species label underneath.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> Unlabeled data: Drosophila + zebrafish

Bullets (render exactly these, terse):

- Provided by S. Hauser: Drosophila larvae + zebrafish calcium video
- No labels, just raw video → ideal for self-supervised pretraining
- Two non-mouse species → makes the cross-species question possible (H2)

Media — two looping preview clips side by side (equal height). Under each, a species label:

- `contents/videos/drosophila-czi.mp4` — label: *Drosophila*
- `contents/videos/zebrafish-etl.mp4` — label: *Zebrafish*

If video embedding is not practical, use the matching still as a poster/fallback: `contents/images/drosophila-czi.png`, `contents/images/zebrafish-etl.png`.

Single source line under the row (tiny): Unlabeled calcium imaging provided by S. Hauser (AnKi Lab).

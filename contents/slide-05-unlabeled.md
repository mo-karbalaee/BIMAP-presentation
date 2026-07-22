Generate slide 5 of the NEUROSEG presentation, the unlabeled-data slide (right after the labeled-data slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: we also have unlabeled cross-species calcium video (Drosophila larvae + zebrafish), provided by S. Hauser. No labels are needed for self-supervised pretraining, so this data is directly usable, and it is what makes the cross-species question (H2) possible.

Layout:
- Bullets across the top (compact).
- Three short preview videos in a single row across the lower two thirds, each with a small label underneath.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> Unlabeled data: Drosophila + zebrafish

Bullets (render exactly these, terse):

- Provided by S. Hauser: Drosophila larvae + zebrafish calcium video
- No labels, just raw video → ideal for self-supervised pretraining
- Formats: multi-frame TIFF + Zeiss CZI; zebrafish = 6-plane ETL volumes
- Makes the cross-species question possible (H2)

Media — a row of three looping preview clips (equal height, left to right). Under each, a small label:

- `contents/videos/drosophila-czi.mp4` — label: *Drosophila (CZI)*
- `contents/videos/drosophila-tif.mp4` — label: *Drosophila (TIFF)*
- `contents/videos/zebrafish-etl.mp4` — label: *Zebrafish (ETL, one plane)*

For each, if video embedding is not practical, use the matching still as a poster/fallback: `contents/images/drosophila-czi.png`, `contents/images/drosophila-tif.png`, `contents/images/zebrafish-etl.png`.

Single source line under the row (tiny): Unlabeled calcium imaging provided by S. Hauser (AnKi Lab). No public citation.

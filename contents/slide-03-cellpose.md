Generate slide 3 of the NEUROSEG presentation, the Cellpose baseline slide (right after the pipeline slide).

You are the LaTeX manager. The content below is FINAL. Render the bullets as-is: short, minimal, one idea each. Do NOT expand into sentences or paragraphs, and do not add content. This is a talk, not a paper.

Message of this slide: our pipeline ships with a strong, pretrained segmentation model (Cellpose) as the DEFAULT during inference. So the moment you install the pipeline, you can segment a recording end-to-end without training anything. It is also our baseline.

Layout:
- Put the segmentation video (or its still) on the right, about half the slide width, vertically centered. Bullets on the left.
- Keep the title in the top title area; nothing may collide with the footer band.

Slide title:

> Cellpose: the pipeline's default segmenter

Bullets (render exactly these, terse):

- Cellpose: a pretrained, generalist deep-learning cell segmenter `\cite{stringer2021cellpose}`
- Ships **pre-installed** as the pipeline's **default inference model**
- Segment any recording out of the box, no training required
- Serves as our **baseline**: what our learned models must beat

Media (right side, about half slide width):

- Primary: embed the video `contents/videos/cellpose-segmentation.mp4` (Cellpose masks overlaid on a mouse calcium recording, looping). Use media9 (or the template's video method); set the still below as the poster frame.
- Fallback still (if video embedding is not practical): `contents/images/cellpose-frame.png`
- Caption (italic, small): *Cellpose segmentation, run through our pipeline (default inference model)*
- Source line (tiny): Model: Cellpose `\cite{stringer2021cellpose}`. Data: Neurofinder 00.00, mouse cortex `\cite{peron2015barrel, neurofinder}`.

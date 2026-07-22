# Slide 3 — The Data

## On-slide content

**Title:** Two kinds of data: labeled mouse, unlabeled cross-species

- **Mouse — Neurofinder** (labeled): our **evaluation target**. Frames + hand-drawn neuron footprints (`regions.json`). Multiple recordings.
- **Drosophila + zebrafish** (unlabeled): supervisor-provided raw calcium video (TIFF + Zeiss CZI). Used for **self-supervised pretraining** — no masks needed.
- All data is **2D + time** (a movie per recording).
- Key property: a neuron's **footprint is static across time** — only its *brightness* changes as it fires. So a segmentation label is **one mask per recording**, not per frame.

## Figure / visual

- Three side-by-side thumbnails: mouse (Neurofinder) frame, Drosophila frame, zebrafish frame — labeled by species and "labeled / unlabeled."
- Optionally a small inset: a **max-projection** of a recording with ground-truth contours overlaid, to show footprints sitting on real cells (also previews the H3 idea).
- Flag if you want me to generate these stills.

## Speaker notes (~1 min)

- Two roles for two datasets. **Neurofinder (mouse)** is the only *labeled* set, so it's where we train the supervised head and measure Dice/mIoU. **Drosophila + zebrafish** are *unlabeled* — perfect for self-supervision, which needs only raw video.
- This split is exactly what makes the hypotheses testable: labels live in one place (mouse), and abundant unlabeled video lives elsewhere (and in other species).
- Make the **static-footprint** point explicitly — it's subtle but important: neurons don't move, only their fluorescence fluctuates, so the ground truth is a fixed spatial map per recording. This shapes how we split train/test and how we read the metrics later (and it's a natural Q&A hook).

## Q&A prep

- **Is Neurofinder multi-species?** No — it is **all mouse**; the series number encodes the contributing lab / brain region, not the organism. (This corrected an early wrong assumption of ours — good Reflexion point.) A genuine cross-species test therefore *requires* the Drosophila/zebrafish data.
- **Why is the source unlabeled a problem?** It rules out a supervised model on the source; so H2 compares *pretraining sources*, not supervised-vs-SSL (covered later).
- **Formats?** Neurofinder = per-frame TIFFs + `regions.json`; supervisor data = multi-frame TIFF stacks and **Zeiss CZI** (`.czi`), including 6-plane ETL zebrafish volumes we split into planes.
- **Scale?** Order of a few GB of Drosophila + ~tens of GB of zebrafish video — plenty for self-supervised pretraining.
- **Preprocessing?** Per-clip min-max normalization to [0,1] + resize to a fixed input size; this normalization matters (a mismatch here was a bug we later fixed).

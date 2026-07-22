# Slide 1 — Motivation & Problem

## Slide title

Reading the brain, one neuron at a time

## Body (render as the slide's text)

- **Calcium imaging** records brain activity: when a neuron fires, intracellular Ca²⁺ rises and a fluorescent indicator brightens — **active neurons "light up" over time** (2D + t video).
- To turn this video into science, each neuron's **soma must be segmented**, then its **activity trace** (ΔF/F over time) can be read out.
- **Manual annotation is slow, subjective, and does not scale** — it is the real bottleneck.
- **Our angle:** raw video is abundant and cheap; labels are scarce and expensive. Can **self-supervision on unlabeled video** cut how many labels we need?

## Figure

- **File:** `images/raw-calcium-frame.png`
- **Content:** a raw calcium-imaging frame (mouse, Neurofinder 00.00), contrast-normalized. Bright blobs = active neuron somas; dark background = inactive tissue.
- **Caption:** *Raw calcium imaging: active neurons appear as bright spots on a noisy field.*
- **Source/credit (render as small text under the image):** Neurofinder benchmark (neurofinder.codeneuro.org), dataset `00.00` — mouse cortex, Svoboda Lab / Janelia.
- **Placement:** right half (hero image); text bullets on the left.

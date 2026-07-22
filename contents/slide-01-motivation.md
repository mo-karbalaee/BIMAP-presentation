# Slide 1 — Motivation & Problem

## On-slide content

**Title:** Reading the brain, one neuron at a time — why segmentation is the bottleneck

- Calcium imaging makes **active neurons "light up"**: when a neuron fires, intracellular Ca²⁺ rises and a fluorescent indicator brightens (2D + time).
- To turn that video into science, you must **segment each neuron's soma** → then read its **activity trace** (ΔF/F over time).
- The catch: **manual annotation is slow, subjective, and doesn't scale** — it is the real bottleneck.
- **Goal:** an automatic pipeline that segments active neurons — and, as a research question, whether **self-supervision on abundant *unlabeled* video** can reduce how many labels we need.

## Figure / visual

- Left: a raw calcium-imaging frame (grayscale) → right: the same frame with neuron masks + a couple of ΔF/F traces underneath. One arrow: *video → masks → traces.*
- Source: we can pull a real frame + trace from an inference run (`output/H1_infer/...`). Flag if you want me to render this composite.

## Speaker notes (~1 min)

- Open with the biology in one breath: neurons fire → Ca²⁺ rises → fluorescence; so a movie of a brain region shows *who is active, when*.
- The scientific payload isn't the pixels, it's the **per-neuron activity traces** — and you can't get those without first knowing *where each neuron is*. That's segmentation.
- Make the pain concrete: labeling somas by hand is hours per recording, annotator-dependent, and there are many recordings/species. So the field needs automation, and labels are the scarce resource.
- Land the thesis: *labels are expensive, raw video is cheap and abundant — so can self-supervised learning exploit the cheap thing to save the expensive thing?* That framing motivates all three hypotheses later.

## Q&A prep

- **Why not just use Cellpose / classical methods?** They're strong generic baselines (and we include Cellpose in the pipeline), but they're not activity-aware and don't leverage unlabeled calcium video; our question is specifically whether SSL representations help.
- **Why is manual labeling "subjective"?** Neuron boundaries in noisy, overlapping fields are genuinely ambiguous; different annotators disagree, which also caps achievable Dice.
- **Unbiased vs activity-based segmentation?** The brief names both families; our method is learning-based and can use temporal (activity) information via the video input.

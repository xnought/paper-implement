I'm going to wait till this paper get's presented at the conference. There are too many gaps in the paper to reimplement (mostly around how the NSD data is processed and which activations are chosen and why). Neeed more info! Somewhat surprised that reviewers didn't bring this up https://openreview.net/forum?id=IqHeDe2lbl

## Paper
- https://aimarvi.github.io/pubs/iclr_marvi_khosla_2025.pdf
- https://www.wikiwand.com/en/articles/Two-streams_hypothesis

## Implementation

- <a target="_blank" href="https://github.com/xnought/paper-implement/"><code>TODO</code></a>

## Notes
- Sparse decomposition of each stream (ventral, dorsal, lateral) from fMRI voxels, then compare to Deep Neural Nets (like resnet).
- Dorsal stream: visually guided (where) 
- Ventral stream: object recognition (what)
- Lateral stream: motion
- Why is the useful to see if DNNs activations are similar to the brain? They say are interested in distinguishing the three streams. What if their representations are all similar? That would be weird. If they are much different, then you just confirm what you already know. Basically this paper removes evidence from other papers who claimed that different streams are aligned in the brain and confirms others. There is the value.
- I am more interested in actually getting the computation involved, not just seeing if they are somewhat aligned between an approximate measure (fMRI) and another approximate measure (only select activations from DL model). I'm probably being to critical.
- But I do see the value in seeing if there is any similarity at all. Then you can apply methods (which don't exist yet) to extract the exact computations.
- 

## Plan

- [ ] Read the paper
- [ ] Reimplement the paper
- [ ] General framework for Torch or Jax, or maybe ONNX as a intermediate format, to perform these comparisons?
- [ ] ...

## Papers

- https://arxiv.org/abs/2411.02280

## Qs

- Wonder if this method can be applied to find where associate memory is being stored in LLMs? 
- Only testing activations at the output of each block. Why not the activation of every operation or even hidden layer of the MLP?

## Notes

- Abstract says we can find a language network in the brain, are the sub parts of LLMs that show the same property? Because it seems like LLMs are much more than just language generation.
- Use same neuroscience localizer, but with artificial neural nets to identify active circuits 
- Compare the task (ie language) against control and find places where is necessary for language but not control.
- Wow they get more selectivity for language than for math and code. I bet this is not the case with calude sonnet.
- They ablated the top 1% of language units and we get garbage, if you ablate randomly, things looks mostly fine. This seems suspect and might be able to show that this is just a product of neural net training. But maybe not 
- Human language network in left hemisphere and most active with words and less with non words.   
- Denote the previous bullet as having high selectivity for language
- Multiple Demand network active with hard tasks. Maybe we could see this active more for reasoning models?
- Theory of Mind network about modeling other people's states
- Language network localized functionally, not anatomically. So the voxels in fMRI in word tasks selectively fire vs. not word tasks.
- The method takes the (top $k$) voxels during a language heavy task and compares/contrasts them against a control. If the activations are mostly the same, we can say that we have not found an selective region of the language network. But if we do find differences, we might have something.
- Present LLM with 240, 12 long word sentences, then capture activations from output of each transformer block.  

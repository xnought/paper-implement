# Optimizers and norm 

Not going to lie, didn't really get the math in this paper. Probably revisit this later... 

Main punchline though is that different optimizers have different norms/directions they choose for steepest descent. Useful if I am trying to concoct a new optimizer for a new situation.

## Paper

- https://arxiv.org/pdf/2409.20325

## Notes

- So the actual claim is that if we remove momentum/moving average terms, each are just doing steepest descent under a different norm 
- Claim or hope is that we can optimize different tensors with norms that make sense to their operations. 
- Convex function: one global minimum as the local minima. Any line segment between two points lies above the function. So like a bowl.
- Didn't even realize but the optimizers are theoretically based on these convex functions and is somewhat surprising that they carry over to the loss surfaces.
- Different norms refer to different step directions on the same loss function
-  Punchline is that sgd is euclidean norm, infinity results in adam, spectral in shampoo
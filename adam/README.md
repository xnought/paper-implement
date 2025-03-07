# Adam optimizer

## Implementations

- [`adam.ipynb`](https://github.com/xnought/paper-implement/blob/main/adam/adam.ipynb)

## Papers

- https://arxiv.org/pdf/1412.6980
- https://www.youtube.com/watch?v=NE88eqLngkg
- https://www.youtube.com/watch?v=k8fTYJPd3_I

## Notes

- Nice way to think about how much gradient updates cost: same cost as just running the function. Very efficient given combinatorial search!
- But running regular SGD on high dimensional parameter space could be better
- Basically leverage momentum to skip down the loss surface
- Exponential moving average over the gradient
- Moving averages are estimates of the average and variance of the gradient ove r time
-  Adding momentum to SGD is $v= \beta v + (1-\beta)dw$ and $w = w - \alpha v$ which is just a moving average of $dw$ instead of updating by $dw$ itself. Goal is to remove the oscillations of SGD.
- Usually $\beta=0.9$ used which is like averaging over last 10 grads

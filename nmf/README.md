# Non-negative Matrix Factorization

## Paper
- https://proceedings.neurips.cc/paper_files/paper/2000/file/f9d1152547c0bde01830b7e8bd60024c-Paper.pdf
- https://www.ime.usp.br/~jstern/miscellanea/seminario/Schmidt09.pdf

## Implementation

- <a target="_blank" href="https://github.com/xnought/paper-implement/blob/main/nmf/actual.ipynb"><code>actual.ipynb</code></a>
- <a target="_blank" href="https://github.com/xnought/paper-implement/blob/main/nmf/reg_grad_descent.ipynb"><code>reg_grad_descent.ipynb</code></a>

## Notes
- Suppose we have a matrix with non-negative entries $A$
- Can we produce a factorization as $A = B \cdot C$? Where $A$ is shaped (m, n) and $B$ is shaped (m, k) and $C$ is shaped (k, b).
- Objective is to minimize error $\argmin_{B, C} ||A-(B\cdot C)||$. The paper has proof on the bounds, but let me first see if I can just apply regular gradient descent to it.
- Multiplicate update rule (note that grad descent is faster since we do less matrix multiplies) 
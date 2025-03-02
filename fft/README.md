## Papers

- https://www.youtube.com/watch?v=nl9TZanwbBk (DFT)
- https://web.stanford.edu/class/cme324/classics/cooley-tukey.pdf

## Notes

- Discrete Fourier transform takes $N^2$ steps in the computation. This is easy to see because we can literally write out the equation as $$X(j) = \sum_{i=0}^{N-1}A(k)\cdot e^{2\pi ijk / N}, \ \ k=0\dots N-1$$ which of course is just multiplying the values of a function by pure sin and cosine waves with different frequencies. Ones that match up well, will show up at spikes in the frequency space. So we loop over $i$ in total $N$ times and for each we do $k$ iterations also $N$ times. So in total $N^2$ runtime.
- They claim (and are correct) that instead they can do it in at most $2N \log_2 N$ iterations. Damn!
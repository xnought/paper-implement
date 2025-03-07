# FFT

## Implementations

- [`dft2.ipynb`](https://github.com/xnought/paper-implement/blob/main/fft/dft2.ipynb)
- [`fft.ipynb`](https://github.com/xnought/paper-implement/blob/main/fft/fft.ipynb)

## Papers

- https://web.stanford.edu/class/cme324/classics/cooley-tukey.pdf (original paper)
- https://youtu.be/spUNpyF58BY?si=_qEWGnKiBeXw_Mu2&t=804 (3b1b)
- https://www.youtube.com/watch?v=h7apO7q16V0 (FFT video)

## Notes

- Discrete Fourier transform takes $N^2$ steps in the computation. This is easy to see because we can literally write out the equation as $$X(j) = \sum_{i=0}^{N-1}A(k)\cdot e^{2\pi ijk / N}, \ \ k=0\dots N-1$$ which of course is just multiplying the values of a function by pure sin and cosine waves with different frequencies. Ones that match up well, will show up at spikes in the frequency space. So we loop over $i$ in total $N$ times and for each we do $k$ iterations also $N$ times. So in total $N^2$ runtime.
- They claim (and are correct) that instead they can do it in at most $2N \log_2 N$ iterations. Damn!
- FFT works by recursively reusing multiplies such that we reduce the computations by 1/2 each time (hence $\log_2 N$) and we still have to sum linearly so that is still $N$ times, so in total $N \log_2 N$ time 
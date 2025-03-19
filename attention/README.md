# Attention is all you need

I've already implemented attention before, but I always forget the details, so let me implement it again.

## Implementations

- <a target="_blank" href="https://github.com/xnought/biogen/blob/main/model.py"><code>model.py</code></a>
- <a target="_blank" href="https://github.com/xnought/paper-implement/blob/main/attention/mha.ipynb"><code>mha.ipynb</code></a>
- <a target="_blank" href="https://github.com/xnought/paper-implement/blob/main/attention/attn.ipynb"><code>attn.ipynb</code></a>

## Papers

- https://arxiv.org/pdf/1706.03762 

## Notes

- RNNs can work, but are slow due to necessary sequential computations (and have other issues regarding gradients)
- Self attention is finding dependencies within itself to create a powerful representation
- softmax(qk/sqrt(dk))v is scaled dot product attention, multihead is doing that n times and concatenating the result and projecting down to some output dimension
- Mask is there so we can train next token prediction in parallel. In other words, we model attention only for tokens to predict the next
- Positional encodings, but can do learned embedding method instead
- after MHA, do residual add and norm (layer norm, or parameterized tanh new paper has shown)
- Followed by MLP with add and norm after it too
- MHA concats the various attention heads, then projects to an out dimension we agree upon

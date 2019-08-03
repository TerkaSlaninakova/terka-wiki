# News
Notes (tl;dr style) from reading new articles / studies concerning ML

## [14.6.2019] Weight-agnostic neural networks
A search method for neural network architectures that can already perform a task without any explicit weight training.
- WHAT
    - developed architectures that can do a task even when the weights are randomly sampled
- MOTIVATION / PRIOR RESEARCH
    - there's some research into randomly initializing a CNN/LSTM showing they still perform pretty well
- HOW?
    - Traditionally: optimizing weights of a fixed network. This study: optimize instead for architectures that perform well over a wide range of weights.
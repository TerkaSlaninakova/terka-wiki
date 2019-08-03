[IN CONSTRUCTION]
# Learning rate

Most famous hyperparameter, required to be set by most of optimizers. It's guiding the training process by directly influencing strength of gradient descent (speed of its convergence and whether it'll undreshoot/overshoot or reach the local/global minimum).

## Problems How to picking up the correct LR
Generally, the approach is to start with the smallest LR possible and incrementally increase until the loss doesn't decrease anymore (useful to plot a graph).
- **Problem with this approach**: Saddle points - gradients are close to 0, optimization reaches pleateu. Solution: Change LR every iteration according to some **cyclic function** f (if we get stuck in a plateau, increasing LR allows us to escape from it).
### Types of cyclical learning rates:
- [Triangular (Smith at al.)](https://arxiv.org/pdf/1506.01186.pdf)
- ['Cosine annealing' (Loshchilov et al.)](https://arxiv.org/abs/1608.03983)
- Another benefit of this approach is the imrpovement in accuracy - small LR tends to favor closest minima, increasing it from time to time helps it escape.

At this point using cyclical LRs is SOTA training technique with no additional (computational or other) cost that imrpoved performance.

* [TODO] [LR range tests](https://arxiv.org/pdf/1506.01186.pdf)
* https://medium.com/38th-street-studios/exploring-stochastic-gradient-descent-with-restarts-sgdr-fa206c38a74e
* https://towardsdatascience.com/estimating-optimal-learning-rate-for-a-deep-neural-network-ce32f2556ce0

# Batch size and number of epochs

# Early stopping
- https://stats.stackexchange.com/questions/231061/how-to-use-early-stopping-properly-for-training-deep-neural-network

# Network architecture
- https://github.com/carpedm20/ENAS-pytorch


## [Dropout, L1, L2](../Regularization.md)

## Hyperparameter Optimization Algorithms

* Grid search (essentially bruteforce)
* Random search
* Bayesian Optimization - recommended to use and works better (faster) over grid/random
    - builds a probability distribution over possible function that estimates how good your model might be for a certain choice of hyperparameters
    - additional reading:
        * [TODO] [Gaussian process](https://katbailey.github.io/post/gaussian-processes-for-dummies/)
        * [TODO] [Bayesian optimization](http://krasserm.github.io/2018/03/21/bayesian-optimization/)

## Other optimization techniques

* [TODO] [weight initialization](https://medium.com/@amarbudhiraja/towards-weight-initialization-in-deep-neural-networks-908d3d9f1e02#.t5xt4opd7)

# Sources
* https://blog.nanonets.com/hyperparameter-optimization/
* https://towardsdatascience.com/deep-learning-performance-cheat-sheet-21374b9c4f45
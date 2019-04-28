[IN CONSTRUCTION]
# Learning rate
* [TODO] [LR range tests](https://arxiv.org/pdf/1506.01186.pdf)
* https://medium.com/38th-street-studios/exploring-stochastic-gradient-descent-with-restarts-sgdr-fa206c38a74e
* https://towardsdatascience.com/estimating-optimal-learning-rate-for-a-deep-neural-network-ce32f2556ce0

# Batch size and number of epochs

# Early stopping
- https://stats.stackexchange.com/questions/231061/how-to-use-early-stopping-properly-for-training-deep-neural-network

# Network architecture
- https://github.com/carpedm20/ENAS-pytorch

# Regularization techniques (but also hyperparameters)
Regularization **reduces over-fitting** by adding a penalty to the loss function.
## Momentum
[TODO]
* [Why Momentum Really Works
](https://distill.pub/2017/momentum/)

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
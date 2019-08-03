# Intro
We want to avoid model complexity
- aim for low training error while taking into account model's complexity

Regularization **reduces over-fitting** by adding a penalty to the loss function.

# Types of regularization

## L0 regularization
We want to force weights to 0 esp. when the data points (together w/ feature crosses of them) are too big. If i use a count-based approach that L0 represents - e.g. counting non-zero coefficient values, this will result in an NP-hard problem

## L1 regularization
  Approximation to L0 reg that's usable in practice: penalized `|weight|`

## L2 Regularization (Ridge regularization)
Very simple approach to regularization
- penalized sum of the squares of the weights
- incorporates Bayesian prior: weights should be centered around 0 w/ normal distr.

$$
Loss(Data|Model) + \lambda(w_1^2, ..., w_n^2)
$$
where $$\lambda$$ controls how much we care about the regularization. Usually about $$1e-06 -> 1e-04$$

## Weight decay
Very similar to L2 reg (basically the same thing). May help to make  function easier to optimize, but in the end doesn't improve the performance (usually), just makes the training faster.

## Dropout
At each training stage, individual nodes are either dropped out of the net with probability 1-p so that a reduced network is left.

# Sources
[dropout-in-deep-machine-learning](https://medium.com/@amarbudhiraja/https-medium-com-amarbudhiraja-learning-less-to-learn-better-dropout-in-deep-machine-learning-74334da4bfc5)

[]
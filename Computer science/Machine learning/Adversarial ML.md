# Adversarial Machine learning

## State of ML research today
Most ML algorithms can be described as optimization algorithms, we look for solution to optimization problem that generalizes well. We are past the point of "making ML work". Given a large enough dataset, supervised problems are +- solved. There are occasionaly some tweaks, such as using reward-based systems or generating data.
- **generative modeling** - take set of examples and learn probability distribution that generated those examples and generate new samples from the distribution (e.g. [Celeb A dataset, Karras et. al, 2017](https://arxiv.org/abs/1710.10196))
    - use GANs - 2 player MiniMax game: **generator** creates images, **discriminator** recognizes the images as either real or fake. generator tries to adapt the input to the discriminator


In **adversarial ML** we look at **game theory** - each player has its own cost, wants to minimize it, but other players' costs influence it too. The value function is a 3d surface where 1 player tries to minimize the value and other player tries to maximize it. The point at which one player finds local minimum and other local maximum is called **nash equilibrium** and is considered solution to the game.

## Adversarial training
Idea: Look for an equilibrium to the game, with classifier and attacker that tries to maximize the failure rate of the classifier by chnaging the inputs

### Minimizing the number of labels (label efficiency)
- take GAN discriminator and train it as a classifier: labels: Real cat, real dog, fake. The fake portion comes from the generator
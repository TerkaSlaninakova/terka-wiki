# Reinforcement learning

## Markov decision process: most typical decision making framework for RL
- 4-tuple (S,A,R,T)
    - S is the state space of an environment
    - A is the set of actions
    - R(s,a) is a function that returns the reward received for taking action a in state s
    - T(s′|s,a) is a transition probability function, specifying the probability that the environment will transition to state s′ if the agent takes action a in state s.
- GOAL: Find policy $$\pi$$ that maximizes expected future reward

## Model-based vs. model free
* In Model-free RL, the agent perform actions in the real world and collect the reward from the environment.
* In Model-based methods construct a model based on interactions with the real worlds and sitmulate further episodes of learning on the **constructed model**
    - speeds up learning
    - might lead to mistakes if the constructed model is vastly different from reality
### The main loop in Model-Based RL:
1. Act in the real environment, collect rewards
2. Deduce a model, use it to generate samples (planning)
3. Update value functions from samples
4. Use value functions to select actions to perform in th real environment
5. Restart and loop again

# Sources
- https://www.quora.com/What-is-the-difference-between-model-based-and-model-free-reinforcement-learning
# Markov models

Stochastic model estimating future states based on current state. Initially proposed by Andrey Markov and applied to Eugene Onegin, the model estimated probability of vowel/consonant in the text. 

Markov chain is the representation of markov's model (chain meaning the chain of states). They're one of the most intensively studied models in mathematics, but they are still very limited. Taking this idea one step further, we get **hidden markov models (HMMs)**, where the states are not visible, they have to be infered from observations. E.g. in Siri, the hidden states are written words, the observations are sounds. Goal: Infer the words from the sounds.

If the states and observations are continuours, HMM becomes a **Kalman filter**. Kalman filters are used to estimate a system state, when it cannot be measured directly (E.g. location of car in tunnels when GPS signals are weak)

Sources:
* 
* https://www.youtube.com/watch?v=mwn8xhgNpFY
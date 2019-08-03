[IN CONSTRUCTION]

# Intro
LogReg works fine for cases of binary classification. In case of multi-class classification, some tricks need to be employed

## One-vs-all
Use N separate binary classifiers.

## Softmax
Softmax assigns decimal probabilities to each class in a multi-class problem

### Types
* Full softmax
* Candidate sampling
    - during training softmax calculates a probability for all the positive labels but only for a random sample of negative labels
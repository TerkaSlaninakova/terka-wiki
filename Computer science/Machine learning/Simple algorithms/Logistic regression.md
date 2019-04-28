# Intro
Logistic regression is an efficient mechanism to calculate probabilities

**Classification vs. Regression in LogReg**:
Plain LogReg does regression: It's output would be that a spam probability is 0.8. In classification tasks we'd decide to label something as spam, given it's spam prob. is 0.8 (= classification threshold).

## Log loss
$$LL = \sum_{(x,y)\in D} -ylog(y') - (1-y)log(1-y')$$

Log loss is the negative logarithm of the likelihood function assuming a Bernoulli distribution.

## Sigmoid function
$$
y' = \frac{1}{1+e^(-z)}
$$
z = log-odds because when sigmoid is inverted, z can be seen as the log of propb. of "1" / prob. of "0"
$$
z = log(\frac{y}{1-y})
$$

Logistic regression models need to use some kind of regularization, most of the use:
- L2 reg
- Early stopping
# k-NN
k-NN is probably the simplest machine learning algorithm. To make prediction for a datapoint, it simply finds the closest datapoint with a class

### Parameters:
- k : how many neighbours to consider
- distance metric: usually Euclidean

## Advantages
Simple, intuitive, often works quite well when the data is not sparse and there are not so many features

## Disadvantages
Doesn't work well with a lot of features, tends to overfit for small $$k$$

![knn-dec-boundary.png](knn-dec-boundary.png)
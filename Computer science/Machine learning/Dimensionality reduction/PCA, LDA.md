# Principal component analysis
PCA is a method that rotates dataset in a way s.t. rotated features are statistically uncorrelated.

PCA is a dimensionality reduction technique that creates linear combinations of the original features, that are uncorrelated and ranked by the order of their explained variance.

Idea: We're trying to keep as many principal components as needed to reach a high enough cumulative explained variance, which in turn results in great dimensionality reduction.

Example:
4D data, plot into 2D plot to show similar data cluster together and which variable is the most valueable in clustering the data.

How does it work:
- find the direction of maximum variance - data contains most of the information, the direction of biggest correlation (Component 1)
- find direction that contains the most information and is correlated with component 1
- continue

### PCA using Singular value decomposition

1. Plot the data
2. Calculate the average distances from the axes = get the center of the data
3. Shift the data so that the center is a the origin of the graph (relative position of the datapoints is not changed)
4. Fit a line though the data going through the origin
    - by maximizing the sum of square distances from the projected points to the origin
    - fitted line is called PC1
5. Scale the fitted line (vector) to get an **eigenvector** (divide by its length (so that we end up with length=1) and reposition the datapoints) = the distances and ratios are kept. Proportions of each features are called **loading scores** and sum of squares are referred to as **eigenvalues**.

We can then make statements such as:
- PC1 accounts for x% of the total variation around PCs:
    - variation is calculated as sumSquares(distances in PC{1,2})/(n-1)

and we can then get rid of the dimension with PCx that accounts for least variation, we get a good approximation of the distribution even if we ignore one dimension.

# Linear Discriminant Analysis
Works in a similar fashion, but instead of maximizing explained variance it **maximizes the separability between classes**.

## Advantage
- fast, easy to implement, versatile

## Disadvantage
- new features are not easilty interpretable


## Sources
- https://www.youtube.com/watch?v=FgakZw6K1QQ
- https://elitedatascience.com/dimensionality-reduction-algorithms
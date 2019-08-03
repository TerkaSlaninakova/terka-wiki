# Terms

## 2- sample hypothesis testing
- A/B testing - Randomized experiment with 2 variants (2 versions of the same variable)
- multivariate testing - tests more than 2 versions
- Z-tests - appropriate when assuming normal distribution
- Student's t-test - comparing means
- Welch's t-test

## Multiple samples (populations) hypthesis testing
If we want to perform statistical tests about similarity of multiple populations, we could theoretically perform multiple t-tests with certail aplha, but the problem is the error compounds: 0.95^3 = 0.857, so we don't want that.

Instead, **ANOVA** is used. ANOVA stands for **Analysis of variance** and it represents a variability ratio.

If we want to explore whether 3 distributions come from the same population, we'd calculate the means:

$$\mu_1, \mu_2, \mu_3$$

Find **variability within each distribution (=variance)** and **variability between distributions (distance from the overall mean)**:

$$ANOVA = \frac{within}{between}$$
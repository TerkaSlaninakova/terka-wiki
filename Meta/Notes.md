# Introduction to Machine Learning with Python
## EDA
- pair plot - looks at all possible pairs of features
```
iris_dataframe = pd.DataFrame(X_train, columns=iris_dataset.feature_names)
grr = pd.plotting.scatter_matrix(iris_dataframe, c=y_train, figsize=(15, 15), marker='o')
```

- theoretical models (e.g. naive bayes) are not gonna be as accurate as data-driven models (e.g. Logistic Regression), just because we have a real-world problem  represented by real world data.
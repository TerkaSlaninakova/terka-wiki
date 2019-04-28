# Intro
Pandas is a data analysis API

## Structure
- **DataFrame** - relational table
- **Series** - single column - DataFrame contains one or more series and a name for each series

```
city_names = pd.Series(['San Francisco', 'San Jose', 'Sacramento'])
population = pd.Series([852469, 1015785, 485199])

pd.DataFrame({ 'City name': city_names, 'Population': population })
```

### Loading data 
- read_csv()
```
california_housing_dataframe = pd.read_csv("https://download.mlcc.google.com/mledu-datasets/california_housing_train.csv", sep=",")
california_housing_dataframe.describe()
```

### Exploring the dataset
- describe(), head()

# Sources
[Intro to pandas by ML crash course](https://colab.research.google.com/notebooks/mlcc/intro_to_pandas.ipynb?utm_source=mlcc&utm_campaign=colab-external&utm_medium=referral&utm_content=pandas-colab&hl=en#scrollTo=avgr6GfiUh8t)
[pandas doc site](http://pandas.pydata.org/pandas-docs/stable/index.html)
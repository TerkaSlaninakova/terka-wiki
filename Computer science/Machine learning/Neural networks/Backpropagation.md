[IN CONSTRUCTION]
# Intro

Speeding the convergence of neural nets

## Vanishing gradients problem
Gradients for the lower layers (closer to the input) can become very small. In deep networks, computing these gradients can involve taking the product of many small terms.
    - ReLUs are useful here

## Exploding gradients problem
If the weights in a network are very large, then the gradients for the lower layers involve products of many large terms. In this case you can have exploding gradients: gradients that get too large to converge.
    - learning rates are important
    - batch normalization

## Dead ReLU units
Once the weighted sum for a ReLU unit falls below 0, the ReLU unit can get stuck.
    - lower learning rate

## Normalizing feature values
* zero-centered [-1, 1]
```
def linear_scale(series):
  min_val = series.min()
  max_val = series.max()
  scale = (max_val - min_val) / 2.0
  return series.apply(lambda x:((x - min_val) / scale) - 1.0)
```
* avoiding outliers
* linear scaling, clipping, log scaling
```
def log_normalize(series):
  return series.apply(lambda x:math.log(x+1.0))
```
```
def clip(series, clip_to_min, clip_to_max):
  return series.apply(lambda x:(
    min(max(x, clip_to_min), clip_to_max)))
```
```
def z_score_normalize(series):
  mean = series.mean()
  std_dv = series.std()
  return series.apply(lambda x:(x - mean) / std_dv)
```
```
def binary_threshold(series, threshold):
  return series.apply(lambda x:(1 if x > threshold else 0))
```
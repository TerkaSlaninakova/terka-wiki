[TBD]

## Neural nets
* [DNNRegressor](https://www.tensorflow.org/api_docs/python/tf/estimator/DNNRegressor)
```
  dnn_regressor = tf.estimator.DNNRegressor(
      feature_columns=construct_feature_columns(training_examples),
      hidden_units=hidden_units,
      optimizer=my_optimizer,
  )
```
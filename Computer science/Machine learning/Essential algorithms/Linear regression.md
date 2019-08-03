# Linear regression
Linear regression is the simplest linear for of regression. It's based on minimizing the mean squared error between predictions and targets by adjusting the vector of weights `w`.

The goal is to fit a line / hyperplane to a set of points. Given a set of points `(x_1,x_2), ..., (x_n,y_n)`, find a hyperplane `y = w_i x_i + b`. 

## Multiple regression
The distinction comes from the number of indep. variables. In practice, every linear regression is actually multiple regression, because we have more than one feature.

Interpretability:

$$ \hat y = 27 + 9x_1 + 12x_2$$

Each coefficient corresponds to est. change in `y` doing a 1 unit change to a  variable, when all other variables are held constant. So `9` is the estimate of expected incrase of `y` with the increase of `1` in capital investment.
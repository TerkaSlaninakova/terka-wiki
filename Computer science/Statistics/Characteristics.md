# Characteristics of a 1D dataset
## Numerical characteristics
- **Nominal features** (e.g. eye color, race)
    - empirical modus - the most frequent value
- **Ordinal values** - are comparable (e.g. school grades)
    - α-quantile (see [quantile function](https://en.wikipedia.org/wiki/Quantile_function)) - divides 
        - `α=0,25: x_0,25` – lower quantile

- **mean**: $$m=\frac{1}{n}\sum_{i=1}^{x_i} x_i$$
- **dispersion**: $$s^2=\frac{1}{n}\sum_{i=1}^n (x_i-m)^2$$
- **Standard deviation**: $$s = \sqrt(s^2)$$

**Example:** wages: 
24 600, 24 500, 25 950, 17 550, 21 200, 38 700, 15 400, 64 350

Median)
- sort: 15 400, 17 550, 21 200, 24 500, 24 600, 25 950, 38 700, 64 350
- n = 8
- median = α=0,5: n*α = 4 (even), so x_0.5 = (x_(4)+x_(5))/2 = 24 550

Quantiles)
- x_0.25 - x_0.75 -> same as above, but we take the difference of these 2

Average)
- $$m=\frac{1}{10}\sum_{i=1}^{10} x_i$$

Dispersion)
- $$s^2=\frac{1}{10}\sum_{i=1}^{10} (x_i-123,1)^2$$

- if for values $$x_1, ..., x_n$$ we know their average and dispersion and there exists a linear relationship between $$y1, ..., y_n; y_i = a + b*x_i$$, then:
    - Average: $$m_2 = a + b*m_1$$
    - Dispersion: $$s_2^2 = b^2*s_1^2$$

# Characteristics of a 2D dataset
- **covariance** = simultaneous dispersion of the first and second features along their average:
    - $$s_{12}=\frac{1}{n}\sum_{i=1}^n (x_i-m_1)(y_i-m_2)$$
- **correlation coefficient** - characterizes closeness of linear relationship among 2/more features
    - $$r_{12}=\frac{1}{n}\sum_{i=1}^n \frac{x_i-m_1}{s_1} \cdot \frac{y_i-m_2}{s_2}$$ = $$r_{12}=\frac{s_{12}}{s_1\cdot s_2}$$

**Example:**
|   |   |   |   |   |   |   |   |   |   
|---|---|---|---|---|---|---|---|---|
|Car age|8|12|14|13|
|Car price|7|4|3|1|
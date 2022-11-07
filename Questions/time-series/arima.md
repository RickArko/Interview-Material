# ARIMA

## ARIMA (p,d,q)


## 1. AutoRegressive
`AR(p)` is a regression model with lagged values of y, until p-th periods in the past as predictors.

$$
y_i = c+ \sum_{i=1}^{p}\varphi_i y_{t-1} + \varepsilon_t = \dots
$$

## 2. Integrated
The difference is taken `d` times until the series becomes stationary. 

**Stationary** - time series whose properties do not depend on the time at which the series is observed.


## 3. MovingAverage
Uses a regression-like model on past forecast errors.

$$
y_t = c + \varepsilon_t + \vartheta_t-1
$$


## Pros vs. Cons

### Pros:
- Only requires prior data
- Performs well on short-term forecasts
- Model non-stationary time series

### Cons:
- Difficult to predict changepoints
- Subjectivity in determining `(p,d,q)`
- Computationally expensive
- Poor performance for longterm forecasts
- Less explainable than `exponential smoothing`
# Forecasting Error Metrics
Description and formulation for various forecasting metrics and a discussion of the use cases, benefits and drawbacks.

![image](/images/time-series-error-metrics.png)

## Scale Dependent Metrics
Scale-dependent means the error metrics are expressed in the units (i.e. dollars, inches, etc.). The main advantage is ease of use and interpretability. These cannot be used to compare different series.

## Mean Deviance or Bias (MD)

$$
    MD = \frac{1}{n} \sum_{1}^{n}\hat{y}_i - y_i
$$

## Mean Absolute Error (MAE)

$$
    MAE = \frac{1}{n} \sum_{1}^{n}|y_i - \hat{y}_i|
$$

## Root Mean Squared Error (RMSE)

$$
    RMSE = \sqrt {\frac{1}{n} \sum_{1}^{n}(\hat{y}_i - y_i)^2}
$$

## Mean Absolute Percentage Error (MAPE)

$$
    MAPE = \frac{1}{n} \sum_{1}^{n}|\frac{ \hat{y}_i - y_i} {y_i} * 100|
$$
## Symentric Mean Absolute Percentage Error (sMAPE)

## Mean Absolute Scaled Error (MASE)

## Weighted Mean Absolute Percentage Error (wMAPE)



### Resources
- [time-series-forecast-error-metrics](https://towardsdatascience.com/time-series-forecast-error-metrics-you-should-know-cc88b8c67f27)
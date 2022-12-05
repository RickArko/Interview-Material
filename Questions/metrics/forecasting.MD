# Forecasting Error Metrics
Description and formulation for various forecasting metrics and a discussion of the use cases, benefits and drawbacks.

![image](/images/time-series-error-metrics.png)

## Scale Dependent Metrics
Scale-dependent means the error metrics are expressed in the units (i.e. dollars, inches, etc.). The main advantage is ease of use and interpretability. These cannot be used to compare different series.

 1. **Mean Deviance or Bias (MD)**

    $$
        MD = \frac{1}{n} \sum_{1}^{n}\hat{y}_i - y_i
    $$

    ```Code

    # MD

    def MD(yhat, y):
        difference = yhat - y
        score = difference.mean()
        return score

    ```

 1. **Mean Absolute Error (MAE)**

    $$
        MAE = \frac{1}{n} \sum_{1}^{n}|y_i - \hat{y}_i|
    $$


    ```Code

    def mae(predict, actual):
        difference = abs(predict - actual)
        score = difference.mean()
    
        return score
    ```
## Scale Independent Metrics
Used to compare forecast performance between different time series.

## Percent Based
Percent based error metrics are scale independent and easily interpretable, but unusable when dealing with zeros (intermittent demand).


 1. **Root Mean Squared Error (RMSE)**

    $$
        RMSE = \sqrt {\frac{1}{n} \sum_{1}^{n}(\hat{y}_i - y_i)^2}
    $$

    ```Code
    # Root Mean Squared Error

    def rmse(predict, actual):
        difference = predict - actual
        square_diff = np.square(difference)
        mean_square_diff = square_diff.mean()
        score = np.sqrt(mean_square_diff)
        return score

    ```

 1. Mean Absolute Percentage Error (MAPE)

    $$
        MAPE = \frac{1}{n} \sum_{1}^{n}|\frac{ \hat{y}_i - y_i} {y_i} * 100|
    $$
 1. **Symentric Mean Absolute Percentage Error (sMAPE)**

    ```Code
    # Symetric Mean Abs Percent Error

    def sMAPE(yhat, y):
        return 2 * abs(yhat - y) / (abs(y) + abs(yhat))
    ```

 1. **Weighted Mean Absolute Percentage Error (wMAPE)**

## Relative Error Metrics
Compare model performance vs. a baseline or benchmark model.

1. **Median Relative Absolute Error (MdRAE)**
1. **Geometric Mean Relative Absolute Error (GMRAE)**


**Drawbacks:**
- statistical distribution with undefined mean and infinite variance
- Require several forecasts to compute
- Can't be used to measure out-of-sample forecast accuracy at a single horizon.

## Scale-Free Error Metrics
Devised to address the drawbacks with relative error metrics.

 1. **Mean Absolute Scaled Error (MASE)**
    - Scale error based on the in-sample MAE from a naive (random walk) forecast

### Resources
- [time-series-forecast-error-metrics](https://towardsdatascience.com/time-series-forecast-error-metrics-you-should-know-cc88b8c67f27)
- [error-measures-intermittent-demand](https://towardsdatascience.com/forecast-error-measures-intermittent-demand-22617a733c9e)
- [everything-you-ever-wanted-to-know-about-forecasting-in retail](https://www.youtube.com/watch?v=ZWmPjMaGOhQ)
- [python-scoring-implementations](https://github.com/TheAlgorithms/Python/blob/master/machine_learning/scoring_functions.py)
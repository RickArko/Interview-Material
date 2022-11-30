# Exponential Smoothing
Exponential Smoothing models are weighted averages of past observations, where the weights decay exponentially as the observations get older. The method generates reliable forecasts 
quickly for a wide range of time-series.


The selection of the method is generally based on recognising key components of the time series (trend and seasonal) and the way in which these enter the smoothing method (e.g., in an additive, damped or multiplicative manner).

## Simple Exponential Smoothing
Simplest method, suitable for data with no clear trend or seasonality.

## Methods
1. Naive
1. Average
$$
    \hat{y}_T+h = \frac{1}{T} \sum_{1}^{T}\hat{y}_T
$$
1. Weighted Average
1. Component Form
1. Flat Forecasts
1. Optimization


## Holt-Winters' Seasonal Method
Three smoothing equations:
1. level _**lt**_
1. trend _**bt**_
1. seasonal _**st**_

## Holt-Winters' Additive Method

## Holt-Winters' Exponential Method

## Holt-Winters' Damped Method

### Sources
 - [hyndman](https://otexts.com/fpp2/expsmooth.html)
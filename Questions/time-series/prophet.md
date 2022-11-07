# Prophet

Prophet is an additive model : the sum of each component equals the prediction. Each component importance is expressed directly in the target unit (unlike SHAP values). And it provides both local and global explainability.

Consequently, it is really easy to plot the prediction / impact of each component on the forecast. If you choose to switch to a multiplicative mode, where every component is expressed as a percentage of the trend, you will have a little more work to do, but it remains very easy to plot.

Unfortunately all these components only provide about 10% of the prediction, the remaining 90% being predicted in the trend… which is almost unexplainable. It will be your job to try to explain the trend using external regressors that you cannot use as features for Prophet, such as customer base growth, contact rates, and changes in customer behaviours for our case study. To do so, you need to have the actual values associated with each one of these features: hence it is only possible to analyse your trend when you look back to the predictions made in the past.

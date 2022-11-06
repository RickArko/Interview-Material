# Lightgbm vs. XGBoost

Even though LightGBM and XGBoost are both asymmetric trees, LightGBM grows leaf-wise (horizontally) while XGBoost grows level-wise (vertically). To put it simply, we can think of LightGBM as growing the tree selectively, resulting in smaller and faster models compared to XGBoost.


## Leaf vs. Level-wise Growth
![leaf-vs-level](/images/leaf-wise-vs-level-wise.png "Leaf vs. Level-wise Growth")

## Parameters
![localImage](/images/boosting-params-by-model.png "Comparison of Boosting Parameters")
# Bagging vs. Boosting


## Bagging
- Bagging is a process in which multiple iterations of the same model are trained with bootstrapped samples.
- Bagging tends to use stronger learners (i.e. Decision Trees with higher max_depth)

## Boosting
- Boosting is a more advanced version of bagging where each model is built sequentially, iterating over the previous one and learning from the previous mistakes made.
- Boosting tends to use "weak" learners such as trees with max depth set low

## Resources:
- [bagging vs. boosting vs. stacking](https://medium.com/grabngoinfo/bagging-vs-boosting-vs-stacking-in-machine-learning-65fe4d1684c0)
# Decision Tree
Supervised ML algorithm to categorize or make predictions based on how a previous set of questions were answered.


## Components:
- **Root node** - The base of the decision tree
- **Splitting** - The process of dividing a node into multiple sub-nodes
- **Decision node** - When a sub-node is further split into additional sub-nodes
- **Leaf node** - When a sub-node does not further split into additional sub-nodes; represents possible outcomes.
- **Pruning** - The process of removing sub-nodes of a decision tree.
- **Branch** - Subsection of the decision tree consisting of multiple nodes.

## Algorithms

1. **CART** (Classification and regression trees) - uses **Gini Coefficient** to decide partition feature
1. **ID3** (Uses information gain - discussed later, to decide the partition feature and not designed to deal with continuous features)
1. **C4.5** (Similar to ID3 using information gain to split data. However can handle continuous features and missing data.)


## Articles
- [masters-in-datascience](https://www.mastersindatascience.org/learning/machine-learning-algorithms/decision-tree/)
- [example notebook](https://github.com/thushv89/exercises_thushv_dot_com/blob/master/decision_trees_light_on_math_ml/decision_trees.ipynb)
- [Intuitive Guide to Understanding Decision Trees](https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-understanding-decision-trees-adb2165ccab7)
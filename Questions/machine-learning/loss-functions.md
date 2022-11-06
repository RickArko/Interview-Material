# Loss Functions
Functions a ML-Model will minimize when calculating each gradient.

## Regression
Below $x$ and $y$ are $D$ dimensional vectors, and $x_i$ denotes the value on the $i$th dimension of $x$.

### Mean Absolute Error(MAE)
$$
\sum_{i=1}^{D}|x_i-y_i|
$$


### Mean Squared Error(MSE)
$$
\sum_{i=1}^{D}(x_i-y_i)^2
$$


### Huber loss
It’s less sensitive to outliers than the MSE as it treats error as square only inside an interval.
$$
L_{\delta}=
    \left\{\begin{matrix}
        \frac{1}{2}(y - \hat{y})^{2} & if \left | (y - \hat{y})  \right | < \delta\\
        \delta ((y - \hat{y}) - \frac1 2 \delta) & otherwise
    \end{matrix}\right.
$$

## Classification

### Cross Entropy

In binary classification, where the number of classes $M$ equals 2, Binary Cross-Entropy(BCE) can be calculated as:

$$
-{(y\log(p) + (1 - y)\log(1 - p))}
$$

If $M > 2$ (i.e. multiclass classification), we calculate a separate loss for each class label per observation and sum the result.

$$
-\sum_{c=1}^My_{o,c}\log(p_{o,c})
$$

$$
-{(y\log(p) + (1 - y)\log(1 - p))}

-\sum_{c=1}^My_{o,c}\log(p_{o,c})
$$

M - number of classes
log - the natural log
y - binary indicator (0 or 1) if class label c is the correct classification for observation o
p - predicted probability observation o is of class c

## Negative Loglikelihood
$$
NLL(y) = -{\log(p(y))}
$$
Minimizing negative loglikelihood
$$
\min_{\theta} \sum_y {-\log(p(y;\theta))}
$$

is equivalent to Maximum Likelihood Estimation(MLE).

$$
\max_{\theta} \prod_y p(y;\theta)
$$

Here $p(y)$ is a scaler instead of vector. It is the value of the single dimension where the ground truth $y$ lies. It is thus equivalent to cross entropy (See wiki).\
NLL(y) = -{\log(p(y))}

$$
\min_{\theta} \sum_y {-\log(p(y;\theta))}
$$

$$
\max_{\theta} \prod_y p(y;\theta)
$$

### Hinge loss
Used in Support Vector Machine(SVM).
$$
max(0, 1 - y \cdot \hat{y})
$$

### KL/JS divergence
$$
KL(\hat{y} || y) = \sum_{c=1}^{M}\hat{y}_c \log{\frac{\hat{y}_c}{y_c}}
$$
$$
JS(\hat{y} || y) = \frac{1}{2}(KL(y||\frac{y+\hat{y}}{2}) + KL(\hat{y}||\frac{y+\hat{y}}{2}))
$$

# Activations

## Sigmoid
Related to Logistic Regression. For single-label/multi-label binary classification.
$$
\sigma(z) = \frac{1} {1 + e^{-z}}
$$
\sigma(z) = \frac{1} {1 + e^{-z}}

## Tanh
$$
tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}} = \frac{1 - e^{-2x}}{1 + e^{-2x}}
$$
tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}} = \frac{1 - e^{-2x}}{1 + e^{-2x}}

## Softmax
For multi-class single label classification.
$$
\sigma(z_i) = \frac{e^{z_{i}}}{\sum_{j=1}^K e^{z_{j}}} \ \ \ for\ i=1,2,\dots,K
$$

## Relu
$$
Relu(z) = max(0, z)
$$

## Gelu
$$
Gelu(x) = x\Phi(x)
$$
where $\Phi(x)$ is the cumulative distribution function of Gaussian distribution.
Gelu(x) = x\Phi(x)
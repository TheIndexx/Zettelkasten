---
title: "Vectorization"
tags:
- Deep-Learning
enableToc: false # do not show a table of contents on this page
---
## Example
What we need to calculate: $z = w^Tx + b$
Vectorized: $z = np.dot(w, x) + b$ using numpy library
![](hub/ai/imgs/vectorizedspeed.png)

Vectorization takes advantages of the SIMD (single instruction multiple data) - or parallelism - instructions on GPU's and CPU's much better. Hence it is better to **avoid explicit for-loops**, and use built-in functions in python libraries like numpy.

## Vectorizing Logistic Regression
$z = w^Tx + b$ - this is for 1 training example.
That means that we would have to iterate through this equation m number of times, which is time-consuming. Instead, let's vectorize it.

Unvectorized: $Z = \matrix[z^1,z^2,...,z^m] = w^TX + \matrix[b,b,...,b] = \matrix[w^Tx^1 + b, w^Tx^2 + b,..., w^Tx^m+b]$
where X is an $\matrix[n_x, m]$ matrix for all the training examples x

Vectorized: $z = np.dot(w.T,x)+b$

Similar, let's doing the same for $a = \sigma(z)$

$A = \matrix[a^1,a^2,...,a^m] = \sigma(Z)$

## Vectorizing Logistic Regression's Gradient Output
$dz^1 = a^1 - y^1, dz^2 = a^2 - y^2,..., dz^m = a^m - y^m$
$dZ = \matrix[dz^1,dz^2,...,dz^m]$
$A = \matrix[a^1,...,a^m]$ | $Y = \matrix[y^1,...,y^m]$
$dZ = A - Y$
---
$db = \frac{1}{m}\sum_{i=1}^{m}dz^i = \frac{1}{m} np.sum(dZ)$
$dw = \frac{1}{m} X dZ^T$

Here's the final result:
$Z = w^TX + b = np.dot(w.T,X) + b$
$A = \sigma(Z)$
$dZ = A - Y$
$dw = \frac{1}{m} X dZ^T$
$db = \frac{1}{m} np.sum(dZ)$
---
$w := w - \alpha(dw)$
$b := b - \alpha(db)$
---
title: "Gradient Descent"
tags:
- Neural-Networks
- Deep-Learning
enableToc: false # do not show a table of contents on this page
---
Want to find $w,b$ that minimize $J(w,b)$.  In the image, the gradient is convex, meaning that there is one global minimum instead of several local minimum, and helps us define what cost function to use.
![](hub/ai/imgs/GradientDescentimg.png)

Gradient descent works in iterations; it might start at a random point, then take a step in the direction of steepest descent until it finds the global minimum.

Repeat {
$w := w - \alpha \frac{dJ(w,b)}{dw}$
$b := b - \alpha \frac{dJ(w,b)}{db}$
}     , where $\alpha$ is the learning rate, and := means "updates" ^21021e
## Logistic Regression Gradient Descent
![](hub/ai/imgs/logisticregressionderivatives.png)
## Gradient Descent on m examples
In order to use gradient descent, we should take the derivatives calculated in the above example and average them.


$J=0; dw_1 = 0; dw_2 = 0; db = 0$
For $i=1 to m$
$z^i = w^Tx^i + b$
$a^i = \sigma(z^i)$
$J$ $+= -(y^i \log{a^i} + (1 - y^i) \log{1-a^i})$
$dz^i = a^i - y^i$
$dw_1$ $+= x_1^i * dz^i$
$dw_2$ $+= x_2^i * dz^i$
$J /= m, dw_1 /= m, dw_2 /= m, db /=m$
We're using dw1, dw2 and db as accumulators, so now
$dw_1 = dJ/dw_1$, and the same for dw2 and db (there is actually a much faster and more efficient way to do this, check out [Vectorization](ai/Vectorization.md))

Then, you would use the steps [here](#^21021e) to do one step of gradient descent.
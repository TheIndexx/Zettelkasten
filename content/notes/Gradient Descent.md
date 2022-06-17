---
title: "Gradient Descent"
tags:
- Neural-Networks
- Deep-Learning
enableToc: false # do not show a table of contents on this page
---
Want to find $w,b$ that minimize $J(w,b)$.  In the image, the gradient is convex, meaning that there is one global minimum instead of several local minimum, and helps us define what cost function to use.
![](notes/imgs/GradientDescentimg.png)

Gradient descent works in iterations; it might start at a random point, then take a step in the direction of steepest descent until it finds the global minimum.

Repeat {
$w := w - \alpha \frac{dJ(w,b)}{dw}$
$b := b - \alpha \frac{dJ(w,b)}{db}$
}, where $\alpha$ is the learning rate, and := means "updates"
## Logistic Regression Gradient Descent

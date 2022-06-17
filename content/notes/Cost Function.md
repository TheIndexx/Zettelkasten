---
title: "Cost Function"
tags:
- Deep-Learning
- Logistic-Regression
enableToc: false # do not show a table of contents on this page
---
## Loss Function

^879b2f

When training examples, we need to establish a guideline for error so the learning algorithm knows how far $\hat{y}$, it's predicted value, was from the real $y$.

$L(\hat{y}, y) = \frac{1}{2}(\hat{y} - y)^2$

This is a standard squared-error loss function, but for the purpose of logistic regression we will use a Loss Function that it more convex and suitable for [Gradient Descent](notes/Gradient%20Descent.md).

$L(\hat{y}, y) = -(y \log{\hat{y}} + (1 - y) \log{1-\hat{y}})$

This is better for 2 cases.
1. If $y = 1$: $L(\hat{y}, y) = -\log{\hat{y}}$
	- Want $-\log{\hat{y}}$ large, want $\hat{y}$ large
2. If $y = 0$: $L(\hat{y}, y) = -\log{1 - \hat{y}}$
	- Want $- \log{1 - \hat{y}}$ large, want $\hat{y}$ small
# Cost Function
$J(w,b) = \frac{1}{m} \sum_{i=1}^{m} L(\hat{y}^i, y^i) = -\frac{1}{m} \sum_{i=1}^{m} (y^i \log{\hat{y}^i} + (1 - y^i) \log{1-\hat{y}^i})$

The [Loss Function](#^879b2f) is meant for 1 training example, while the Cost Function is applied to a set of parameters to minimize the Loss Function.
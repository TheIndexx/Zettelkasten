---
title: "Logistic Regression"
tags:
- Neural-Networks
- Deep-Learning
enableToc: false # do not show a table of contents on this page
---
#### Text description
An algorithm for [Binary classification](notes/Binary%20classification.md) in [Supervised Learning](notes/Supervised%20Learning.md). In statistics terms, it estimates the probability of an event happening or not, like if you vote or didn't vote, given a dataset. There are only 2 possible outcomes, and the predicted Y value only lies between 0 and 1.

#### Math description
Given x (features), want $\hat{y} = P(y=1|x)$

Parameters: $w \in \mathbb{R}^{n_x}$, $b \in \mathbb{R}$

Output: $\hat{y} = \sigma(w^Tx + b)$

A $\sigma$, or sigmoid function converts whatever number the $(w^Tx + b)$ is to a probability that y = 1, or a range of numbers from 0 to 1. You can look it up if you're interested but I couldn't care less right now.
![](/notes/imgs/Pasted%20image%2020220615221550.png)

When we implement logistic regression, we want to find optimal values of w and b to get $\hat{y}$ to be as accurate as possible.
---
title: "Binary Classification"
tags:
- Neural-Networks
enableToc: false # do not show a table of contents on this page
---
Algorithm where output is either 0 or 1 (could symbolize true/false, yes/no).

### Example
We got a 64x64 pixel cat picture. Input is picture, output is either 1 (cat) or 0 (no cat)
![catpicbreakdown](hub/notes/imgs/catpicbreakdown.png)
In order to make this more processable for the algorithm, we break the picture into 3 matrices of pixel values for each Red, Green, and Blue pixel. Now, we put it all into the input, X, by putting all the values into a 1 column matrix in order (Red, Green then Blue), and given that it was a 64x64 pixel image, we deduce

$n_{x}(depth of x dimension) = (64)(64)(3) = 12288$

In our training set, we have m number of (X, Y) examples, where $x \in \mathbb{R}^n_{x}$ and $y \in (0,1)$.

Thus, to efficiently group the X values from all the examples, we will have an X matrix where each column is an input (or 12288 pixel color values) and each row is another example. In Python, X.shape would be a $(n_{x}, m)$ dimensional matrix
![Xmatrix](hub/notes/imgs/Xmatrix.png)

You can also stack Y in columns, except Y.shape would be $(1, m)$ since there are only 2 possible outcomes.
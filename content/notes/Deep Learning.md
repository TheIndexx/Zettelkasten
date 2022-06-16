---
title: "Deep Learning"
tags:
- Machine-Learning
- Artificial-Intelligence
enableToc: false # do not show a table of contents on this page
---
Representations in terms of more representations (inception type vibe). Often refers to training [Neural Networks](notes/Neural%20Networks.md).
### Examples
Say you took a selfie, and we wanted an AI to find you in the picture. To break it down, we will first take the most basic representation, then make another representation in terms of that until we get to you.

Pixels -> Edges -> Contours -> Objects -> Person

A fantastic example of this is the [Multi-Layer Perceptron](notes/Multi-Layer%20Perceptron.md), which deserves its own page. But TLDR, it maps input values onto output values, and is a math function composed of many smaller functions, aka representations.

Important examples:

## Measuring Depth
1. The number of sequential instructions needed to evaluate the system architecture (the absolute longest path through the flow chart to get from input to output). 
![procedureimage](/imgs/procedureimage.png)
2. Depth of graph describing relationship between **concepts**. It will likely be smaller than the first method. 

Comparison of measuring depth with AI observing face of person with a shadow covering half their face.

Layers | Method 1 | Method 2
------------ | ------------ | ------------
1 |  1 eye visible | eyes
2 | portion of face visible | faces
3 | infers 2nd eye exists | 

### Quick summary of process to get to Deep Learning
- **[Artificial Intelligence](notes/Artificial%20Intelligence.md)** is cool in easy environments, but doesn't get real world rules.
	- *Machine Learning* to yield "subjective results"
- **[Machine Learning](notes/Machine%20Learning.md)** works well with easy data, but is hard to find good features
	- *Representation Learning* to learn features
- **[Representation Learning](notes/Representation%20Learning.md)** leads to too many representations influencing everything, and is hard to find high-level FOV's
	- *Deep Learning* to simplify representations
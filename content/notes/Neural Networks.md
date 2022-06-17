---
title: "Neural Networks"
tags:
- Deep-Learning
enableToc: false # do not show a table of contents on this page
---
## Explanation
At its most basic form, a neural network is just a series of nodes that are connected together, inspired by how neurons work in humans.

Here's a very simple example of a single neuron:
![housingpricegraph](hub/notes/imgs/housingpricegraph.png)]

The size of the house, x value, would go into a "neuron", where the neuron uses the linear regression function (blue line), and outputs the price, y value. This is a single neuron, and you would get a larger neural network from stacking several of these neurons together.

Now for the neural network:
Say we have several inputs, or x values: (1) house size, (2) # of bedrooms, (3) zip code, (4) wealth. 1 and 2 would impact **family size**, 3 would impact **walkability**, 3 and 4 would impact **school quality**. Now given family size, walkability and school quality, each with their own linear regression function, we can estimate the price of the house. In practice, you would just give the AI the 4 input values and get a price, but the magic behind the scenes is what really makes it a neural network!

Using deep learning, we don't have to explicitly say "Inputs 1 and 2 will correlate with family size", instead the AI can figure out which inputs will correlate to which nodes. So all we really need to do is give the AI a bunch of X and Y values and it will figure out the relationships itself. A cool effect of this is that every input value impacts every node; in tech terms, we would say the 2 layers are densely connected.
![nodeillustration](hub/notes/imgs/nodeillustration.png)

Neural networks are most useful in [Supervised Learning](notes/Supervised%20Learning.md), such as the housing example.

### Why are Neural Networks taking off
Scale. Thanks to new advances in technology, humans have much more data on a variety of things than we did before, and normal algorithms ([Logistic Regression](notes/Logistic%20Regression.md), sum) can only understand so much. Deep Learning algorithms are much better at comprehending big data, and we see the highest levels of performance in large neural networks (many parameters, hidden networks) with large amounts of data.

Things to remember:
- **m** is used to denote amount of data
- With small training sets, it might be easier to make a normal algorithms than to train a large neural network. The latter only consistently performs well with large training sets.

#### Techniques
Typically, you might use a *for* loop to iterates through a training set with m examples. 

I, an intellectual, would insult your intelligence, and subsequently use forward propogation step and backward propogation step.
##### Computation graph
Computation graphs explains the underlying concept behind forward and back propagation. This concept is fairly intuitive to me, but here's some pictures just in case. 
![forwardcomputationgraph](hub/notes/imgs/forwardcomputationgraph.png)
![computingderivatives](hub/notes/imgs/computingderivatives.png)

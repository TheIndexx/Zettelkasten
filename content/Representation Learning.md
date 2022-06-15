---
title: "Representation Learning"
tags:
- Machine-Learning
- Artificial-Intelligence
enableToc: false # do not show a table of contents on this page
---
# Representation/Feature Learning
Method that uses a set of techniques to let the system automatically find features needed for [Machine Learning](Machine%20Learning.md).

**Example**: [Auto Encoders](Auto%20Encoders.md)

### Factors of Variation
When creating algorithms to learn features, look for **Factors of Variation**, or different sets of features (typically not observable) that affect observable quantities. Going back to the AI car finder example, FOV's would be the brightness of the sun, color, wheels, etc.
### Overwhelmed...
- Problem #1: Many FOV's influence every piece of data we can observe (wayyyy too many to be useful at all)
	- Solution: Disentangle FOV's, keep only the ones we care about
- Problem #2: How?
	- Solution: [Deep Learning](Deep%20Learning.md)!!
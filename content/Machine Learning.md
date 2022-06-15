---
title: "Machine Learning"
tags:
- Artificial-Intelligence
enableToc: false # do not show a table of contents on this page
---
Performance of model ∝ Representation of data
### Examples
- A system that decides the salary of employees
	- Would use database with features of employees (hours worked, company title, number of people managed) and their corresponding salaries to create a model
	- Then uses model to assign salaries to future employees
	- Bad data (where datapoints do not correlate to features) gives bad results
- **Logistic Regression**: Uses dataset to create mathematical correlations between features and outcomes

TLDR: Use good features for good results
### Problemo
But... it's not that easy. For example, what if you wanted to make an AI identify a car in a photo, but didn't know what features to look for. Looking for wheels, windows, and a "car shape" are all very erratic depending on the angle of the photo and the type of car.

**Solution**: Use ML for that too! (aka [Representation Learning](Representation%20Learning.md))
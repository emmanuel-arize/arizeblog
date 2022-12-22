---
layout: python-post
title: Bootstrap Method
category: machine-learning-python
---
In this article, we will learn about bootstrap sampling, what it is, how it works and  we will implement it sampling using Python

**Bootstrap sampling** is a general tool for assessing statistical accuracy. Rather than repeatedly obtaining independent data sets from the population to estimate a model parameters, the bootstrap method which is the resampling technique makes is possible to create new different samples from the original training.

  Suppose we have a model of which we want to fit to a training set denoted by $$Z$$. Let assume the parameter of interest is the standard deviation denoted $$\sigma$$ and let $$\hat \sigma$$ represent the sample statistic used to estimate $$\sigma$$. Using bootstrap sampling the idea is to randomly sample with replacement from $$Z$$, **k** new samples, each of which has the same size as the original training set. Since we are sampling **k** new samples this will produce **k** bootstrap datasets

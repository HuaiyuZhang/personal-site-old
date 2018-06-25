---
layout: post
title: Bootstrap Why It Works
---

Bootstrap is one of the most ingenineous technique in statistics, especially with the aid of compuation power nowadays. We heard and use it very often, but, why it works? This post will try to explore some facts behind the curtain. Bootstrap is often used for bias and standard error estimation. We will only look at an one-sample **standard error estimation** problem along with this text. Most of the principles mentioned here can be generalized to other statistics of interest. More details can be found in, for example, Efron (1982). 

## Set up

Suppose we have collected a group of iid observations, \\( (x_1, \ldots, x_n) \\)

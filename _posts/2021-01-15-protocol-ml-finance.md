---
layout: post
title: Paper Reading--A Backtesting Protocol in the Era of Machine Learning
---

## Abstract

Machine learning applications in finance needs more caution. This paper presents a research protocol for ML and quant finance.

## Introduction

Most ML methods builds on a large amount of data. Finance data are often of small size, monthly or quarterly. K-fold cross-validation is not a good idea in this case. It is always necessary to impose structure. Although with novel methods, the situation we are facing now in empirical finance research is still similar to the past. We want to avoid backtest overfitting of investment strategies.

## How Did We Get Here

Growing computing power, vast data, advances in statistics, math, computer science changed the way people perceive quantitative methods. The authors searched in trivial strategies and found a good performer among them. The strategy may pass the backtesting, but basic knowledge tells us it is a nonsensical one. 

Lessons:

- Machine learning does not impose economic principles. If it works, it work in retrospect, not necessarily in the future.

- When data are limited, economic foundations become more important.

- Finance data usually do not allow large-scale cross validation, but finance theory can help.

- Models are crude approximation of the real world. Finance is a world of human beings.

## The Winner's Curse

Quant managers are seduced by the data into thinking a model is better than it is. This induces selection biases. Models with strong results will be tested, modified, and retested, while models with poor results will be quickly expunged. It causes good models fail in the test period (false negative) and researches seek a narrative to justify a bad model an reinforce it (false positive or exaggerated positive).

## The protocol to prevent winner's curse

### 1. Research motivation
- 1(a) Establish an ex ante economic foundation

- 1(b) Beware an ex post economic foundation

### 2. Multiple testing and statistical methods

Make multiple comparison adjustment for significance

- 2(a) Keep track of the strategies and correlations. If 20 strategies tested and they are perfectly correlated, it is equivalent to test one strategy for 20 times. 

- 2(b) Keep track of combinations of variables

- 2(c) Beware of parallel universe problem. Suppose in 20 candidate variables we test the one variable and it is significant, it is not a single test, because changing the variable order may make this variable the last variable to be significant.

### 3. Sample choice and data

Determine and keep the choice of data processing before build the model, and do not change after build some models.

- 3(a) Define the test sample range ex ante. Never change the training data once see the model.

- 3(b) Ensure data quality

- 3(c) Choose the transformation at the beginning, not by performance.

- 3(d) Do not arbitrarily exclude outliers.

- 3(e) Select Winsorization level before constructing the model.

### 4. Cross-validation

- 4(a) Out of sample is not really out of sample. They are in-sample given the wisdom today. 

- 4(b) A model does not work for out of sample, but some modification makes it work. This is not out of sample but overfitting.

- 4(c) Do not ignore transactional costs and fees.


### 5. Model dynanmics

- 5(a) Be aware of structural changes. 

- 5(b) The cross-validated relations of the past may seem powerful for reason that no longer apply or dissipate because we are now aware of them and are trading based on them. (Knowledge interferes reality)

- 5(c) Refrain from tweaking the model.

### 6. Model complexity

- 6(a) Curse of dimensionality. More variables easily overfit the data.

- 6(b) Pursue simplicity and regularization.

- 6(c) Seek interpretable machine learning

### Research Culture

- 7(a) Reward qulity research not good results.

- 7(b) Be careful with delegated research. Research assistants have an incentive to please their supervisor by presenting results that support the supervisor’s hypothesis.


---

Paper link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3275654

---
layout: post
title: Paper Reading--Adaptive trading strategies across liquidity pools
---

## Introduction

Cross-listed stocked have a higher potential of arbitrage.

Usually, the trader builds an execution curve targeting, for example, an Implementation Shortfall or volume-weighted average price (VWAP). Then one buys or sells shares of the asset following the execution curve by sending limit and market orders to the different venues. **How to find the best splitting of orders between the venues?** Mainly on **imbalance** and **spread** of the different venues. 

Building a good model for such an optimal trading cross-listed assets requires taking into account the cross dependence between the imbalance and spread, and the probability and the proportion of execution of limit orders. The quality of the model mainly relies on the estimation of the market parameters. Updating the market parameters according to the market dynamic is essential. The paper uses the Bayesian updating to handle it.

The trading problem is formulated as a stochastic control problem. The controls are the splitting of volumes between limit and market orders on each venue, and the limits chosen by the trader. The optima is obtained from a Hamilton-Jacobi-Bellman quasi-variational inequality.


## Market parameter update

The paper uses the output of the control model over a slice of execution and then run the model again with the updated market parameters. 

---

Paper link: https://arxiv.org/pdf/2008.07807.pdf

---
layout: post
title: Paper Reading--Dynamic Risk Management
---


## Introduction
- **Diversification** should play a central role in constructing a protfolio.
- **Systematic risk management** can be used to improve a portfolio's risk-adjusted returns and tail characteristics.
- It is possible to forecast risks much more accurately than returns.
- The goal is to improve expected returns for lower downside risk. 

The approach can be broken down and illustrated in the chart.

![]({{ site.url }}/assets/day2_pic1.PNG)

## Risk Aware
Cap-weigted indices are construsted not reference to its risk, losing the potential benefit from diversification. Textbook finance tells that bearing higher risk is associated with higher expected returns.
Empirical evidence indicates that this relationship is weak (security market line flatter than CAPM). The risk aware approach concentrate on the risk side, rather than the return forecasts. 

It involves estimating the covariance of stock returns. The large set of assets, the estimation has high dimensionality issue. They propose to used **factor model** and **hierarchical clustering** to reduce the dimensionality.

## Leverage
The risk aware approach reduces the risk without compromising expected returns. Leverage could raise the return at the expense of bringing up the risk to a similar level to the cap-weighted portfolio.

The simulated performance showed a increased tail loss (returns in the bad scenario) due to the negative skewness of risk-aware portfolio. 

## Last powerful tool: risk overlays

The tail performance (skewness, expected shortfall, maximum drawdown) after leveraging is not satisfactory. Risk overlays are applied to a long position only portfolio. The goal is to reduce the risk under market stress at least of return reduction. These overlays are done by taking short positions on equity index futures. Four overlays are considered:

- volatility-switching overlay (volatility spikes)
- momentum overlay (protracted nagative trends)
- correlation overlay (joint equity and bond sell-offs)
- diversification-benefit overlay (stock-market breadth)



--- 

Link to the article: https://www.man.com/maninstitute/applying-dynamic-risk-management

A reference for Hierarchical Risk Parity: Advances in Financial Machine Learning, Chapter 16.

A reference for flat sercurity market line: https://www.morningstar.com/articles/946297/why-the-capm-falls-flat

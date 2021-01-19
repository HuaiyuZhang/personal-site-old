---
layout: post
title: Paper Reading--AI in asset management
---

## Portfolio management

### alpha and sigma
The most significant application of AI in fundamental analysis is textual analysis. NLP approaches are capable of extracting economically meaningful information from various sources of text, such as corporate annual reports, news articles, Twitter posts.

LASSO can be used to find factors having highest explanatory power for future returns, investigate which industry return has the most significant contribution to the market returns.

ANN has more accurate out-of-sample predictions in that it could capture complex nonlinear relationships. Ensemble methods also produce good results.

Derivative pricing has long been depending on Black-Scholes with strong assumptions. AI can be used for pricing and hedging using non-prarametric option pricing frameworks and future option prices. AI can be used for improving estimates of variance-covariance matrices in Markowitz framework, for example the hierachical cluster analysis.

Challenges: Some research only tested small samples of assets or emerging markets that lack liquidity and efficiency. Feature engineering can be time-comsuming.

### Portfolio optimization

The mean-variance framework of Markowitz faces difficulty with: 1. Optimal asset weights are sensitive to expected return estimate; 2. Estimating var-cov requires a large time series of data and stationarity assumptions. AI can produce better return and risk estimates and provide alternative portfolio construction approaches.

An ANN model can select portfolios according to a learning criterion that maximizes returns subject to VaR constraints. ANN can help with synthetic repliction and reduce the transaction costs. Evolutionary algorithms can solve more complex optimization problems.


## Trading

Pre-trade and execution are handled mostly by algorithms because they require timely and complex analysis. Post-trade analysis often involves some human supervision or overlay.

**Algo trading**

 Modern technical analysis incorporates information from other sources, including fund flows, investor trades, textual data from news articles.

**Transaction cost**

It is a part of pre-trade analysis. Three main components: bid-ask spread, market impact costs, trading commissions. Among these, market impact is not observable before the trade is initiated. It takes as much as two-thirds of trading gains made by systematic funds. AI methods largely improve the prediction of market impact. Shortcomings include no economic intuition and hard to distinguish permanent and temporary market impact.

**Trade execution**

Large-scale trades are typically broken up into a sequence of smaller orders to reduce the market impact. AI facilitates trade execution modeling by actively learning from real market microstructure data.

## Risk management

Market risk is the likelihood of loss resulting from aggregate market fluctuation. Credit risk refers to the risk of a counterparty not fulfilling its contractual obligations.

A significant disagreement between AI forecasts and standard risk model outputs can highlight potential problems and trigger a more thorogh investigation.

## Challenges

- It is difficult to predict how AI will respond to major events or "black swan". Most companies use the same set of tools. As a result, AI-driven crash could be possible.

- AI can make wrong decisions based on spurious or irrelavent patterns in data. 

- Attributing investment performance become challenging by using AI.

- Regulation challenge

- Data quality and sufficiency


---

Paper link: https://www.cfainstitute.org/-/media/documents/book/rf-lit-review/2020/rflr-artificial-intelligence-in-asset-management.ashx

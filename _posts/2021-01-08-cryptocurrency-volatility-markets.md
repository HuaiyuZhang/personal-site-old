---
layout: post
title: Paper Reading--Cryptocurrency Volatility Markets
---

## Introduction

The dynamic nature of an option replication is directly linked to the volatility during the lifetime of the contract. Option markets can hence also be seen as markets for the exchange of volatility risk.

Risk benchmarks, for example CBOE's volatility index (VIX), are designed to capture the expected volatility. This paper aims to develop benchmarks for cryptocurrency volatility.

Some research believes cryptocurrencies have the potential for hedging, but this is challenged. 

VIX was attempted for BTC (Alexander and Imeraj, 2020), but the market liquidity of BTC options is far inferior to S&P500 options. So this paper considers alternative methods.

## Markets and conventions

Market liquidity is defined as "the readiness of participants to exchange the underlying assets and its derivatives". The liquidity is a big concern for cryptocurrencies. The pricing of derivatives relies on replication. A lag of liquidity leads to unstable price and limits the use of option price for index construction.

To avoid the pricing risk, the underlying of cryptocurrency options is often an average of multiple spot indices.

To reduce settlement risks, a price smoothing procedure is used right before expiry. 

## Index methodology

In order to measure a market price for volatility, we are interested in the implied volatility for an ‘ideal’ at-the-money option with exactly 30 days to maturity. To design such an ideal option, there are three considerations:

1. all meaningful indices should be transparent

2. if one were to trade the index itself or derivatives, the index must be physically replicable through a portfolio of liquid assets.

3. an index must represent the desired information of underlying assets.

### 3.1
The maturity of BTC options are not evenly spaced, linear interpolation does not work. It needs multivariate interpolation. Use inverse distance weighting.

### 3.2 CVX
Britten-Jones and Neuberger (2000) risk-neutral variance forecast. It was applied to variance swap and VIX volatility index family. This section uses the same method and applies to BTC option.

### 3.3 CVX76
The index construction only requires volatility, so the vanilla Black-Scholes model can be used. This paper uses Black (1976) model as an alternative method. A shortcoming is the model assumes normality of log return, but empirical evidence showed the skewness and heavy-tailedness for cryptocurrencies.

## Conclusion
The model-free CVX index should yield a better estimate for markets’ expected volatility than the CVX76. However, due to the assumption of normally distributed log returns in the Black-76 method, the (CVX − CVX76) spread is an interesting indicator of market implied tail risk. 


---

Paper link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3639098

---
layout: post
title: Paper Reading--Did Trading Bots Resurrect the CAPM?
---

Automated trading causes increasing intra-day correlation of returns. The trading bots increases the quoting activities and cause stocks' returns to align with the market. 
The goal of the paper is to show that the bot trading make the returns more reflect systematic risk.


This paper assesses whether bot trading leads to changes in the alignment of stock returns across securities by studying the relationship of bot trading and goodness-of-fit of a market model. 
CAPM implies that a well-diversified portfolio should perfectly be correlated to market returns.
Estimate OLS of intra-day stock returns, record the $$R^2$$, then perform a panel regression with the $$R^2$$s as the response variable. The market model is 

$$
R_{it} = \alpha_i + \beta_i R_{M, t} + \epsilon_{it}
$$

where $$R_{M, t}$$ is the market return, and $$R_{it}$$ is the return of security $$i$$.

The next step is to establish the causal relationship: bot trading leads to higher alignment of returns of the individual security with the market. Consider the event that a security is added to the S&P index. This event is exogenous to bot trading. When a firm gets included in an index, nothing changes of the firm itself, but high frequency traders pay more attention to the stock, change prices accordingly, and this affest the $$R^2$$ of the market model above. 

Three methods to justify the causal relationship. Construct a matched sample for all entry and exit events and apply a difference-in-difference panel regression approach. Three approaches: instrumental variable; mediation analysis; causal random forests.

### Difference-in-difference

For security $$i$$, find a mathcing sample $$j$$ by minimizing the macthing error. Let $$\Delta DV_{it} = R^2_{it} - R^2_{jt} $$, then do a regression:

$$
\Delta DV_{it} = \alpha \dot change_{t} + controls_{it} + \delta_i + \epsilon_{it}
$$

where $$change_{t}$$ is the event indicator.


---

Paper link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3515635

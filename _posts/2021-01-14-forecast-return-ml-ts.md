---
layout: post
title: Paper Reading--Forecasting US Equity Market Returns using a Hybrid Machine Learning - Time Series Approach
---

## Abstract

The paper uses machine learning methods to forecast 10-year-ahead US stock returns. It is better than traditional Shiller regression based forecast in terms of lagged CAPE ratios, but worse than Davis et al(2018) two step approach. Combining the two results in better result.


## Introduction
A high CAPE ratio (Campbell and Shiller [1988, 1998]) has been associated with below average 10-year-ahead US stock returns. This relationship became unstable since 2000s. Valuation does not always predict stock market returns, because the “normal” level of CAPE is non-stationary and will vary with changing economic conditions.

None of the ML methods are statistically better than a naïve forecast based on historical average stock returns. None of the ML algorithms can improve on the forecast accuracy of the two-step approach developed by Davis et al (2018). The paper specifies a hybrid ML-VAR to forecast the
earnings yield (1/CAPE) along with other macroeconomic variables, then calculate future stock returns from the forecasted CAPE ratios, following Davis et al (2018). The accuracy of this hybrid method has much lower error.

We find applying ML techniques within a robust economic framework to be superior to applying such techniques in isolation.

## Literature

ML algorithms suffer from look-ahead bias and data mining, difficulty of interpretability.

## Look-ahead issue
To deal with the issue: 

1. Adjust hyperparameters in-sample. Use the out-of-sample data only once for each ML model.

2. As we train the models, we recursively estimate
models by expanding the training data window one month at a time. Online training.

3. Limit features to relevant ones.

## ML on Shiller's regression

Shiller regression

$$
R_{t+120} = \alpha + \beta CAPE_t + \epsilon
$$ 

The in-sample $$R^2$$ was $$54%$$ for 1926-2018 period. But the model performance degraded in recent time, partly due to the lack of mean reversion in the CAPE. The fair value of CAPE depends on macroeconomics factors not included in the model. The model considered by the paper:

![model]({{ site.url }}/assets/day_9_pic1.PNG)

The performance of ML methods is not different from naive historical average.

## ML-VAR
David et al (2018) two-step method: 

1. Step one estimates a VAR model with 12 monthly lags of 1/CAPE, real 10-year bond yields, CPI inflation rate, realized S&P500 price volatility, and realized volatility of changes in real bond yield.

2. In the second step, stock returns are imputed as a sum of three parts: valuation expansion; earnings growth; and dividend yield,

The benefit:

1. Fair-value CAPE ratio is permitted **vary over time**.
2. More data available compared to directly forecast 10 years.

New method:

1. Change the first VAR model from linear structure to ML based. 

$$
X_t = f(X_{t-1}, X_{t-2}, ..., X_{t-12})
$$

$$X_t$$ is a vector of five variables.

2. Use the same sum-of-parts method as David et al (2018). 

$$
r_{t+1} = \%\Delta PE_{t+1} + \%\Delta E_{t+1} + DP{t+1}  
$$

The $$\%\Delta PE$$ is from the VAR in step 1, $$\%\Delta E_{t+1}$$ and $$ DP_{t+1} $$ are from historical average.

---

Paper link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3497170

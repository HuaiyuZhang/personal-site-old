---
layout: post
title: Paper Reading--Breaking Bad Trends
---

## abstract

We quantify the negative impact of trend breaks on the performance of standard trend following strategies. Repair the strategy at market corrections and rebounds.

## Introduction

Trend following investing is also called time-series momentum strategies. It was successful, but when the trend breaks down, the momentum signals became outdated. Faster signals would bring more noise. Three findings:

1. Define the turning point as a month when slow and fast signals differ. Found a negative relationship between number of turning points and risk-adjusted performance. Turning points reflect distict information not transmitted by return volitility. 

2. Number of breaking points help explain deterioration of trend-following strategies in the most recent decade. Market moves (absolute value of asset annual Sharpe Ratios) are positive associated with trend-following strategies performance.  

3. Intersection of slow and fast momentum signals can provide predictive information about returns on equity indices. This is different from the moving average crossovers, which is equivalent to static blends of momentum strategies.

New approach:

Step 1. partition return history into Bull, Correction, Bear, Rebound by fast and slow signals disagreement

Step 2. look into subsequent return behavior and dynanmically implement trend-following strategy after market corrections and rebounds. 

## Turning points

Slow momentum signal is the average of excess return in the last 12 months.

Fast momentum signal is the average of excess return in the last 1 month.

Turning point is the month when two signals have different signs.

## Static Trend

Static trend following strategy: Static 12-month trend goes long one unit if the asset’s trailing 12-month return is positive; otherwise, it goes short one unit. 

The annual Sharpe ratio and number of turning points shows negative relationship.

Number of turning points is not linearly related to market volitility.

The negative relationship carries over to multi-assets portfolios.

Turning points happened more frequent in recent years.

## Dynanmic Trend

The strategy is a mixed one.

Signs of slow and fast signals ->

determine the market states ->

define returns for fast and slow strategies -> 

dynanmic trend strategy return


---

Paper link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3594888


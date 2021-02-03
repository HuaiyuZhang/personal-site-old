---
layout: post
title: Paper Reading--Quantifying Macroeconomic Risk
---

Multi-factor models decompose asset returns into systematic (factor) and idiosyncratic (specific) components. Fundamental factor models usually include a market factor, industry/country factors, and style factors. The fundamental models lack a view on macroeconomic risk, such as that from interest rate, credit, commodity, and other exposures. The challenge of incorporating macro variables in factor models is that macro factors are often correlated. This paper proposes a method for projecting fundamental factor returns onto macroeconomic factor returns and reformulating the fundamental risk model in terms of macro factors.
It allows for quantifying macro risk without estimating a full model of macro, fundamental and market.


## Framework
The basic factor model
$$
r = Xf + \epsilon 
$$ 
X is the factor exposure, f is the factor return, $$\epsilon$$ is the specific return.

The new model imposes a structure wherein the factor return is a linear function of a set of macro returns g:

$$
f = \beta g + \delta
$$

Then the model can be written as 

$$
f = X\beta g + X\delta + \epsilon
$$

This formulation projects the macro variables to the factor space, then use the same factor models to explain the total variability. This is a hierarchical structure.


## Creating a macro risk model

1. The selection of factors should align with those relevant to the investment strategy.

2. The macro factor should be tradable (daily or weekly observable)

3. If $$\beta$$s are estimated with least squares, it is also important to select factors that are not highly correlated with each other.

This paper selects additional macro factors: **changes in interest rates**, **energy prices**, **precious metal prices**, **high-yield credit spreads**.                                                                 

Market-based factors, such as Global Market, Market Sensitivity, Volatility factors, are better explained by the macro variables than by company-specific factors.

The analysis can perform a total risk decomposition of Market Sensitivity factor-mimicking portfolio (FMP) from the AXWW4 model. An FMP is a long-short portfolio that has *unit exposure to the factor it mimics* and no exposure to the other factors. The macro factors can explain a substantial portion of risk of some of the fundamental factors.


The macro model can be used for exposure analysis, risk analysis, performance attribution, and portfolio construction.

---

Paper link: https://qontigo.com/quantifying-macroeconomic-risk/

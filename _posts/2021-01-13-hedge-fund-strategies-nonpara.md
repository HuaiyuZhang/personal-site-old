---
layout: post
title: Paper Reading--Hedge Fund Strategies A non-Parametric Analysis
---

## Abstract

Top performance hedge funds follow a different strategy than mediocre ones. Holding alpha constant, top funds avoid relying on passive investment in illiquid investments but earn risk premiums by accepting market risk. They are able to exploit fleeting opportunities and close losing strategies thereby avoiding momentum reversal.

## Introduction

The paper examines risk factors accepted by hedge funds to unveil the behavior. Two key questions: do hedge funds perform as well as market benchmarks and does top performance persist?

Bali et al(2013) used an almost stochastic dominance approach and the manipulation proof performance measure (MPPM) to examine the relative performance of hedge fund portfolios. This paper uses non-parametric techniques to conduct reliable tests robust to serial and cross dependence.

The market does not second order stochastically dominate hedge funds. Top performance lasts only for six months. Top performers are driven by different risk profile. They focus on narrower range of risk factors (top quintal, liquidity and lookback volatility) rather than SMB and HML Fama French factors. Momentum reversal is a big contributor to poor performance of mediocre funds.

## Data

MPPM measures teh certainty equivalent excess return for an investor with a risk aversion parameter.

## Stochastic dominance tests

Stochastic dominance analysis is a utility based framework. Stochastic dominance does not require full parametric specification of investor preferences. First order dominance relies on non-satiation assumption and second order dominance relies on risk aversion. If A stochatic dominant B, the expected utility of A is always higher than B for an investor.

The test is conducted in a Kolmogorov-Smirnov fashion. Linton et al. (2005) proposed a method dealing with serially dependent data. The sampling distribution is obtained by overlapping moving block bootstrap.

## Risk profiles
Regress excess hedge fund returns by quintile at six months out of sample on risk factors for the excess market return (MKTRF), size (SMB), value (HML), momentum (MOM), momentum reversal (LTR), liquidity (TRADELIQ) and volatility (LOOKBACK).


---

Paper link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3499492

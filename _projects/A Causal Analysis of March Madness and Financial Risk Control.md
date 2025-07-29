---
layout: page
title: Too Busy for Risk? A Causal Analysis of March Madness and Financial Risk Control
description: Causal inference study on how NCAA March Madness affects financial risk control using VaR violations
img: assets/img/march_madness_risk.png
importance: 2
category: data science
---
## Tools and Methods
**Technologies:** Python, pandas, Value at Risk (VaR), Propensity Score Estimation, AIPW (Augmented Inverse Probability Weighting), Event-Based Causal Inference, Data Visualization  
**Concepts:** Causal Inference · Behavioral Finance · Risk Management · Statistical Modeling

## Overview
I completed this project for the Risk Practice course in the Rutgers MSDS program. I investigated how public attention during NCAA March Madness could affect financial risk control. I used Value at Risk (VaR) violations to measure risk model failures and applied causal inference methods to understand if investor distraction had any effect.

## Research Idea
Inspired by the Rubin Causal Model and behavioral finance research, I treated March Madness game days as a special event that might influence investor behavior. I used Augmented Inverse Probability Weighting (AIPW) to estimate how the chance of risk control failure changed when a company was exposed to this kind of attention shock.

<img src="/assets/img/march_madness_risk_motivate.png" alt="workflow" style="width:125%; display:block; margin:auto;">

## Goals
- Test if investor distraction during March Madness increases the chance of VaR violations
- Measure how violation rates change in the days after game days
- Compare tournament-related companies (treatment group) with unrelated companies (control group) using balanced data

## Methodology
**Treatment:** I labeled a trading day as a "Game Day" if it overlapped with the NCAA tournament schedule

**Outcome:** A VaR violation happened when the actual stock return fell below the predicted 90 percent risk threshold

**Propensity Score:** I used past return and volatility to estimate the probability of treatment for each observation

**Causal Inference:** I applied AIPW to estimate both the probability and intensity of risk model failure after exposure

**Visualization:** I created plots to show return trends, violation timing, and group-level comparisons

## Key Findings
- I found that tournament-related companies had fewer VaR violations on game days. This suggests they may receive more attention or risk oversight instead of being ignored.
- However, violations increased in the days after game days. This supports the idea of a delayed distraction effect.
- My results show that even short-term attention shifts can affect the performance of risk control systems.

## Why It Matters
This project helped me connect causal inference techniques with real-world market behavior. It shows that behavioral factors like attention and emotion can influence financial outcomes. I believe this approach can be applied to other large events and can help risk managers prepare for periods when human focus is limited.

**View Full Report:** [Link to Report](https://github.com/joe8606/Measuring-the-Distraction-Effect-of-March-Madness-on-Financial/blob/main/Measuring-the-Distraction-Effect-of-March-Madness-on-Financial.pdf)

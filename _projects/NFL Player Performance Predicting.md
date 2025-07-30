---
layout: page
title: NFL Player Performance Predicting
description:
img: assets/img/nfl_predict.png
importance: 3
category: data science
giscus_comments: true
---
**Full report and implementation details are available at:**
- [Full Report and Code on GitHub](https://github.com/joe8606/NFL-Player-Performance-Modeling.git)
- [Read the Full Report (PDF)](https://github.com/joe8606/NFL-Player-Performance-Modeling/blob/main/Group%201%20-%20Final%20Report.pdf)
- [Read the Slides(PDF)](https://github.com/joe8606/NFL-Player-Performance-Modeling/blob/main/Data%20Mining%20-%20NFL%20Player%20Performance%20Modeling.pdf)

Tools & Techniques: Python, sklearn, XGBoost, Random Forest, NLP (VADER), Reddit API, PCA, K-Means

## Overview
In this project, we developed a predictive framework to forecast NFL player performance using both in-game statistics and public sentiment. Our target metric was Average Expected Points Added (Avg_EPA), enabling consistent evaluation across multiple positions (QB, RB, WR/TE).

We explored a variety of models:

- Linear Models (OLS, Ridge, Lasso, Best Subset)
- Generalized Additive Models (GAM)
- Random Forest Regressors
- XGBoost with Dart Booster

To examine the psychological side of player performance, we conducted sentiment analysis on 688,000+ Reddit posts, integrating weekly compound sentiment scores using VADER. While sentiment was hypothesized to impact performance, it proved to be statistically insignificant in our models.

## Key Findings
- XGBoost outperformed all other models, achieving R² ≈ 0.78 for quarterback performance.
- Rolling average EPA and in-game stats like passing yards, completions, and interceptions were among the most important predictors.
- Contrary to expectations, online public sentiment had minimal predictive value.
- Players showed more stable performance over time, suggesting early volatility due to inexperience or injury.

## Data Sources
- [nflFastR](https://www.nflfastr.com/) datasets (roster, play-by-play, next-gen stats)
- Reddit submission data (2018–2023, Academic Torrents)
- Web scraping from [NFL.com](https://www.nfl.com/) (limited by infinite scroll)

## Modeling Techniques
- Data preprocessing with one-hot encoding and rolling EPA features
- Dimensionality reduction (PCA) + clustering (K-Means)
- Sentiment integration pipeline: VADER → Aggregation → Modeling

<img src="/assets/img/nfl_player_predict_workflow.png" alt="workflow" style="width:125%; display:block; margin:auto;">


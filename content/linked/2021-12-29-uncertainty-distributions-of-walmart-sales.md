---
title: Approach to Estimate Uncertainty Distributions of Walmart Sales
linktitle: https://arxiv.org/abs/2111.14721
author: Tim Radtke
date: '2021-12-29'
slug: uncertainty-distributions-of-walmart-sales
categories:
  - forecasting
tags:
  - link
---

> We present our solution for the M5 Forecasting - Uncertainty competition. Our solution ranked 6th out of 909 submissions across all hierarchical levels and ranked first for prediction at the finest level of granularity (product-store sales, i.e. SKUs). The model combines a multi-stage state-space model and Monte Carlo simulations to generate the forecasting scenarios (trajectories). Observed sales are modelled with negative binomial distributions to represent discrete over-dispersed sales. Seasonal factors are hand-crafted and modelled with linear coefficients that are calculated at the store-department level.

The approach chosen by this team of prior Lokad employees hits all the sweet spots. It’s simple, yet comes 6th in a Kaggle challenge, and produces multi-horizon sample paths. 

Having the write-up of a well-performing result available in this detail is great—they share some nuggets:

> Considering the small search space, this optimisation is done via grid search.

Easy to do for a two-parameter model and a neat trick to get computational issues under control. Generally neat to also enforce additional prior knowledge via arbitrary constraints on the search space.

> According to the M5 survey by Makridakis et al. [3], our solution had the best result at the finest level of granularity (level 12 in the competition), commonly referred to as product-store level or SKU level (Stock Keeping Unit). For store replenishment and numerous other problems, the SKU level is the most relevant level.

Good on them to point this out. Congrats!
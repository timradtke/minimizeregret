---
title: "'Performance of Zero-Shot Time Series Foundation Models on Cloud Data'"
linktitle: https://arxiv.org/abs/2502.12944
author: Tim Radtke
date: '2025-02-23'
slug: performance-of-zero-shot-time-series-foundation-models-on-cloud-data
categories:
tags:
---

Toner et al. compare time series foundation models such as Chronos, Mamba4Cast, and TimesFM on data from Huawei data centers ([data is available on Github!](https://github.com/sir-lab/data-release)):

> To examine the behaviour of (zero-shot) FMs on cloud time series, we perform experiments on function demand data drawn from real-world usage. Our results show that FMs perform poorly, being outperformed by the simple baselines of a linear model and a naive seasonal forecaster.

If you think about it, the seasonal naive method is the original zero-shot foundation model.

> For example, the naive seasonal forecaster performs better than all the FMs across all datasets and forecast horizons. Moreover, the performance difference is often large; for example, the naive seasonal forecaster incurs a MASE typically half that of TimesFM.

Alas, the authors make little attempt to explain why the foundation models are outperformed by the seasonal naive method beyond the data's spikiness. But perhaps that's just it. Chronos, for example, is known to fail on spiky data due to its mean scaling and quantization (see figure 16 in the [corresponding paper](https://arxiv.org/abs/2403.07815v3)).

> We also present evidence of pathological behaviours of FMs, demonstrating they can produce chaotic (as in Figure 1) or illogical (as in Figure 2) forecasts.

Check out the mentioned plots in figures 1, 2, 4 and 5. They're why I don't trust any paper that doesn't visualize its method's predictions.

---
title: "(Deep) Non-Parametric Time Series Forecaster"
linktitle: https://arxiv.org/abs/2312.14657
author: Tim Radtke
date: '2024-05-06'
slug: npts-paper
categories:
tags:
---

If you read [The History of Amazon's Forecasting Algorithm](https://www.amazon.science/latest-news/the-history-of-amazons-forecasting-algorithm), you'll hear about fantastic models such as Quantile Random Forests, and the MQTransformer. In [GluonTS](https://ts.gluon.ai/stable/getting_started/models.html) you'll find DeepAR and DeepVARHierarchical. But the real hero is the simple model that does the work when all else fails. Tim Januschowski [on Linkedin](https://www.linkedin.com/posts/tim-januschowski_forecasting-amazon-reviewer3-activity-7157725169543700480-JiG7):

> One of the baselines that we’ve developed over the years is the non-parametric forecaster or NPTS for short. Jan Gasthaus invented it probably a decade ago and Valentin Flunkert made it seasonality aware and to the best of my knowledge it’s been re-written a number of times and still runs for #amazon retail (when other surrounding systems were switched off long ago).

Januschowski mentions this to celebrate the [Arxiv paper](https://arxiv.org/abs/2312.14657) describing NPTS and its DeepNPTS variant with additional "bells and whistles". Which I celebrate as I no longer have to refer people to section 4.3 of [the GluonTS paper](https://arxiv.org/abs/1906.05264).


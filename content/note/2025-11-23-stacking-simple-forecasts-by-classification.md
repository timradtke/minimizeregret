---
title: Stacking Simple Forecasts by Classification
author: Tim Radtke
date: '2025-11-23'
slug: stacking-simple-forecasts-by-classification
categories:
tags:
---

[This paper](https://arxiv.org/abs/2511.15350) got me thinking about stacking and ensembling of forecasts again.

Different from what the paper proposes but in the stacking models-sense, consider some multi-class classification model used to predict which base model forecasts a given observation from a set of many time series best. Something more akin to the [FFORMA approach](https://robjhyndman.com/papers/fforma.pdf).

But use simple forecast methods to keep the overhead of first creating base forecasts at a minimum. Use the seasonal lag, the seasonal average, the most recent observation, zero, year-to-date average, etc. as base forecasts. Anything, really, that makes for a strong baseline for part of your dataset and can be calculated "without training". If nothing else, this avoids the need for expensive cross-validation loads (as those described in the [aforementioned paper](https://arxiv.org/abs/2511.15350)).

Then, for each observation of your time series data, derive a label based on the base forecast that comes closest to the observation.[^1] 

Finally, train the classifer model to predict the labels, using the base models as features, but also any other kind of feature. Now well and truly spitballing: Have some features summarize base predictions relative to one another, and relative to recent observations ("The seasonal lag is 190% of the year-to-date average") to help the model distinguish patters.

Given that the classifier model would only pick between simple forecast methods to arrive at the final prediction, the overall forecast accuracy will always be limited. I can imagine scenarios, however, where the prediction ends up being more stable and at the right level compared to models trained to predict the time series directly. Constrained by the quality of the base forecasts, this stacking approach could pay off handsomely if the optimal base learner differs across the set of time series, or frequently changes within the same series. That is, when there is no dominant baseline.

For example, it could work well in scenarios where time series have multi-modal distributions due to zeroes, or frequently exhibit structural breaks.

In a way, the classifier would learn the sort of "item routing" [described here](https://vldb.org/pvldb/vol10/p1694-schelter.pdf). Instead of assigning time series to different forecast models based on rules, the classifier will split the data into subsets and assign the model.

One more nice side effect: There is no need for target scaling when base forecasts are non-trained methods and when the meta learner only needs to classify.

The overall approach is also fairly explainable if not interpretable. Especially if one picks the features for additional context wisely.

Finally, while the base forecasts will limit the overall forecast quality that can be achieved, we can measure the best *possible* forecast quality the stacking approach can reach in the hypothetical case of a perfect classification of every observation. So before putting any effort into training a good classifier, we will know whether the effort could hypothetically be worth it.

Though there is a limit to the number of base forecasts you should use to derive the labels for the classifier. Dare to use the range of real numbers and you'll end up back with a ([discretized](https://arxiv.org/abs/2005.10111)) regression problem.

[^1]: Why not throw in an additional label category indicating that none of the methods came even close to the actual observation? To predict that a data point is not predictable by the base forecasts.

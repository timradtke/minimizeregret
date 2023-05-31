---
title: "In Search of Verifiability: Explanations Rarely Enable Complementary Performance in AI-Advised Decision Making"
linktitle: https://arxiv.org/abs/2305.07722
author: Tim Radtke
date: '2023-05-31'
slug: in-search-of-verifiability
categories:
tags: paper
---

Raymond Fok and Daniel S. Weld in a recent [Arxiv preprint](https://arxiv.org/abs/2305.07722):

> We argue explanations are only useful to the extent that they allow a human decision maker to verify the correctness of an AI's prediction, in contrast to other desiderata, e.g., interpretability or spelling out the AI's reasoning process.

This does ring true to me: Put yourself into the position of an employee of Big Company Inc. whose task it is to allocate marketing budgets, to purchase product inventory, or to perform any other monetary decision as part of a business process. Her dashboard, powered by a data pipeline and machine learning model, suggests to increase TV ad spend in channel *XYZ*, or to order thousands of units of a seasonal product to cover the summer.

In her shoes, if you had to sign the check, what let's you sleep at night: Knowing the model's feature importances, or having verified the prediction's correctness?

I'd prefer the latter, and the former only so much as it helps in the pursuit of verification. Feature importance alone, it is argued however, can't determine correctness:

> Here, we refer to *verification* of an answer as the process of determining its correctness. It follows that many AI explanations fundamentally cannot satisfy this desideratum [...] While feature importance explanations may provide some indication of how much each feature influenced the AI’s decision, they typically do not allow a decision maker to verify the AI’s recommendation.

We want verifiability, but we *cannot* have it for most relevant supervised learning problems. The number of viewers of the TV ad are inherently unknown at prediction time, as is the demand for the seasonal product. These applications are in stark contrast to the maze example the authors provide, in which the explanation method draws the proposed path through the maze.

If verifiability is needed to complement human decision making, then this might be why one can get the impression of [explanation washing](https://hci.social/@upol/110397476968179709) of machine learning systems: While current explanation methods are the best we can do, they fall short of what is really needed to trust a system's recommendation.

What can we do instead? We could start by showing the actual data alongside the recommendation. [Making the data explorable](http://worrydream.com/ExplorableExplanations/). The observation in question can be put into the context of observations from the training data for which labels exist, essentially providing [case-based explanations](https://arxiv.org/abs/2106.02605).

Ideally, any context provided to the model's recommendation is *not* based on another model that adds another layer to be verified, but on hard actuals.

In the case of forecasting, simply visualizing the forecast alongside the historical observations can be extremely effective at establishing trust. When the time series is stable and shows clear patterns, a human actually *can* verify the the forecast's correctness up to a point. And a human easily [spots likely incorrect forecasts](https://minimizeregret.com/note/2023/05/20/two-by-two-of-forecasting) given historical data.

The need for verifiability makes me believe in building data products, not just a model.

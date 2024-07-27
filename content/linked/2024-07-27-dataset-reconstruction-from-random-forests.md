---
title: "Trained Random Forests Completely Reveal Your Dataset"
linktitle: https://arxiv.org/abs/2402.19232
author: Tim Radtke
date: '2024-07-27'
slug: dataset-reconstruction-from-random-forests
categories:
tags:
---

The paper's title is a small portion of clickbait: As of yet not *all* but *some* trained random forests completely reveal your dataset. Still, using constraint programming the authors completely reconstruct the data used to train binary classification random forests without bagging on only binary features.

I imagine a lot of random forests having been trained on sensitive data in the past and their model files been more loosely handeled than the data. What private information could the model possibly reveal? Yeah.

[Watch Julien Ferry present his paper](https://youtu.be/qguwZzLV-eE) in a video recorded [for ICML 2024](https://icml.cc/virtual/2024/poster/33585).
---
title: Be Skeptical of the t-SNE Bunny
linktitle: https://twitter.com/matthen2/status/1539376167257526272
author: Tim Radtke
date: '2022-07-11'
slug: tsne-bunny
categories:
  - forecasting
tags:
  - link
---

Matt Henderson on Twitter ([click through for the animation](https://twitter.com/matthen2/status/1539376167257526272)):

> Be skeptical of the clusters shown in t-SNE plots! Here we run t-SNE on a 3d shape - it quickly invents some odd clusters and structures that aren't really present in the original bunny.

What would happen if every machine learning method would come with a built-in visualization of the spurious results that it found?

Never mind the the answer to that question. I think that this dimensionality reduction of a 3D bunny into two dimensions isn't even all that bad---the ears are still pretty cute. And it's not like the original data had a lot more global and local structure once you consider that the bunny is not much more than noise in the shape of a rectangle with two ears that human eyes ascribe meaning to.

I'm the first to admit that t-SNE, UMAP, and all kinds of other methods will produce clusters from whatever data you provide. But so will k-means always return `k` clusters. One shouldn't trust any model without some kind of evaluation of its results.

If you don't take them at face value, UMAP and Co. can be powerful tools [to explore data quickly and interactively](https://minimizeregret.com/post/2020/06/14/embedding-many-time-series-via-recurrence-plots/). Look no further than the cool [workflows Vincent Warmerdam is building for annotating text](https://www.youtube.com/watch?v=gDk7_f3ovIk).
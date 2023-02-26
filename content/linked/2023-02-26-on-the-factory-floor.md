---
title: On the Factory Floor
linktitle: https://arxiv.org/abs/2209.05310
author: Tim Radtke
date: '2023-02-26'
slug: on-the-factory-floor
categories:
tags:
---

What works at Google-scale is not the pattern most data scientists need to employ at their work. But the paper "[On the Factory Floor: ML Engineering for Industrial-Scale Ads Recommendation Models](https://arxiv.org/abs/2209.05310)" is the kind of paper that we need more of: Thrilling reports of what works in practice.

Also, the authors do provide abstract lessons anyone can use, such as *considering the constraints of your problem* rather than *using whatever is state-of-the-art*:

> A major design choice is how to represent an ad-query pair *x*. The semantic information in the language of the query and the ad headlines is the most critical component. Usage of attention layers on top of raw text tokens may generate the most useful language embeddings in current literature [64], but we find better accuracy and efficiency trade-offs by combining variations of fully-connected DNNs with simple feature generation such as bi-grams and n-grams on sub-word units. The short nature of user queries and ad headlines is a contributing factor. Data is highly sparse for these features, with typically only a tiny fraction of non-zero feature values per example.
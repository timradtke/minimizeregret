---
title: Design a System, not an "AI"
linktitle: https://twitter.com/ryxcommar/status/1569006744059133952
author: Tim Radtke
date: '2022-09-14'
slug: design-a-system-not-an-ai
categories:
tags:
---

Ryxcommar [on Twitter](https://twitter.com/ryxcommar/status/1569006744059133952):

> I think one of the bigger mistakes people make when designing AI powered systems is seeing them as an AI first and foremost, and not as a system first and foremost.

> Once you have your API contracts in place, the AI parts can be seen as function calls inside the system. Maybe your first version of these functions just return an unconditional expected value. But the system is the bulk of the work, the algorithm is a small piece.

To me, this is why regulation of AI (in contrast to [regulation of software](https://ssrn.com/abstract=3230829) generally) can feel misguided: Any kind of function within a system has the potential to be problematic. It doesn't have to use matrix multiplication for that to be the case.

More interestingly though, this is why it's so effective to [start with a simple model](https://developers.google.com/machine-learning/guides/rules-of-ml#rule_4_keep_the_first_model_simple_and_get_the_infrastructure_right). It provides the function call around which you can build the system users care about.

> Some free advice for data scientists-- every time I have seen people treat their systems primarily as AI and not as systems, both the AI and the system suffered for it. Don't make that mistake; design a system, not an "AI."

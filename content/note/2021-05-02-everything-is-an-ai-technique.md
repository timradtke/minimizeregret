---
title: Everything is an AI Technique
author: Tim Radtke
date: '2021-05-02'
slug: everything-is-an-ai-technique
categories:
  - AI Regulation
tags:
  - machine learning
  - Statistics
  - Bayesian Inference
  - inventory optimization
  - AI Regulation
---

Along with their [proposal for regulation of artificial intelligence](https://digital-strategy.ec.europa.eu/en/library/proposal-regulation-laying-down-harmonised-rules-artificial-intelligence-artificial-intelligence), the EU published a definition of AI techniques. It includes *everything*, and that's great!

From the proposal's Annex I:

> ARTIFICIAL INTELLIGENCE TECHNIQUES AND APPROACHES referred to in Article 3, point 1
> - (a) Machine learning approaches, including supervised, unsupervised and reinforcement learning, using a wide variety of methods including deep learning;
> - (b) Logic- and knowledge-based approaches, including knowledge representation, inductive (logic) programming, knowledge bases, inference and deductive engines, (symbolic) reasoning and expert systems;
> - (c) Statistical approaches, Bayesian estimation, search and optimization methods.

Unsurprisingly, this definition and the rest of the proposal made the rounds: [Bob Carpenter quipped about the fact](https://statmodeling.stat.columbia.edu/2021/04/22/eu-proposing-to-regulate-the-use-of-bayesian-estimation/) that according to this definition, he has been doing AI for 30 years now (and that the EU feels the need to differentiate between statistics and Bayesian inference). In his newsletter, [Thomas Vladeck takes the proposal apart](https://tvladeck.substack.com/p/regulating-ai) to point out potential ramifications for applications. And [Yoav Goldberg was tweeting about it](https://twitter.com/yoavgo/status/1382745068407300097/photo/1) ever since a draft of the document leaked.

From a data scientist's point of view, this definition is fantastic: First, it highlights that AI is a marketing term used to sell whatever method does the job. Not including optimization as AI technique would have given everyone who called their optimizer "AI" a way to wiggle out of the regulation otherwise. This implicit acknowledgement is welcome.

Second, and more importantly, as practitioner it's practical to have this "official" set of AI techniques in your backpocket for when someone asks *what exactly* AI is. The fact that one doesn't have to use deep learning to wear the AI bumper sticker means that we can be comfortable in choosing the right tool for the job. At this point, AI refers less to a set of techniques or artificial intelligence, and more to a family of problems that are solved by one of the tools listed above.

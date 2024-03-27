---
title: "Chronos: Learning the Language of Time Series"
linktitle: https://github.com/amazon-science/chronos-forecasting
author: Tim Radtke
date: '2024-03-27'
slug: chronos-forecasting
categories:
tags:
---

[Ansari et al. (2024)](https://arxiv.org/abs/2403.07815) introduce their Chronos model family [on Github](https://github.com/amazon-science/chronos-forecasting):

> Chronos is a family of pretrained time series forecasting models based on language model architectures. A time series is transformed into a sequence of tokens via scaling and quantization, and a language model is trained on these tokens using the cross-entropy loss. Once trained, probabilistic forecasts are obtained by sampling multiple future trajectories given the historical context. 

The whole thing is very neat. The repository can be pip-installed as package wrapping the [pre-trained models on HuggingFace](https://huggingface.co/collections/amazon/chronos-models-65f1791d630a8d57cb718444) so that [the installation and "Hello, world" example](https://github.com/amazon-science/chronos-forecasting?tab=readme-ov-file#usage) just work, and the paper is extensive at 40 pages overall. I commend the authors for using that space to include section 5.7 "Qualitative Analysis and Limitations" discussing and visualizing plenty of examples. The limitation arising from the quantization approach (Figure 16) would not have been as clear otherwise.

Speaking of quantization, the approach used to tokenize time series onto a fixed vocabulary reminds me of the 2020 paper "[The Effectiveness of Discretization in Forecasting](https://arxiv.org/abs/2005.10111)" by Rabanser et al., a related group of (former) Amazon researchers.

The large set of authors of Chronos also points to the NeurIPS 2023 paper "[Large Language Models Are Zero-Shot Time Series Forecasters](https://arxiv.org/abs/2310.07820)", though the approach of letting GPT-3 or LLaMA-2 predict a sequence of numeric values directly is *very* different.

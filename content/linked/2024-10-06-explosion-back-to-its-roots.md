---
title: "Explosion Back to Its Roots"
linktitle: https://honnibal.dev/blog/back-to-our-roots
author: Tim Radtke
date: '2024-10-06'
slug: spacy-back-to-its-roots
categories:
tags:
---

In 2016, Matthew Honnibal presented at [the first PyData Berlin meetup that I attended](https://www.meetup.com/pydata-berlin/events/228773954/). He had already started spaCy and was training models on Reddit comments, whereas I wasn't really into NLP and heard about spaCy for the first time that evening. And while I'm still not really into NLP, I never stopped keeping tabs on what he and Ines Montani were building at [Explosion](https://explosion.ai).

Honnibal recounts [Explosion's history in view of recent changes](https://honnibal.dev/blog/back-to-our-roots):

> For most of Explosion’s life we’ve been a very small company, running off revenues. In 2021 that changed, and we became a slightly less small company running off venture capital. We’ve been unable to make that configuration work, so we’re back to running Explosion as an independent-minded self-sufficient company. We’re going to stay small and not look for any more venture capital. spaCy and Prodigy will continue.

With a focus on "[industrial-strength](https://spacy.io)", Explosion has built [opinionated](https://github.com/explosion/thinc) data science tooling with [beautiful](https://prodi.gy) documentation. SpaCy is beloved open-source software (with the community coming together for [spaCy IRL](https://irl.spacy.io/2019/)---a real treat of a conference) that convinces data scientists to spend company budget on Prodigy. This combination of spaCy and Prodigy is the ingredient to Explosion's unique success as small, self-sufficient company in a venture-funded AI environment. Already familiar with spaCy, data scientists are comfortable with purchasing Prodigy licenses to ease their annotation workflows common to NLP. And being technical expert users, they also are capable of hosting the software *themselves*. Explosion doesn't have to handle customers' data.

License revenues, no hosting, no data: Enablers of a profitable business run by a small team. I wish they continue to thrive!

In his post, Honnibal shares realities of maintaining software that companies and developers rarely admit to, yet which are determinants of a team's success:

> Engineering for spaCy and our other projects was also very challenging to hand over. spaCy is implemented in Cython, and big chunks of the project are essentially C code with funny syntax. We pass around pointers to arrays of structs, and if you access them out of bounds, well, hopefully it crashes. You have to just not do that. And then in addition to this memory-managed code, there’s all the GPU-specific considerations, all the numpy minutiae, and maintaining compatibility with a big matrix of Python versions, operating systems and hardware. It’s a lot.

The infrastructure required for machine learning doesn't make it any easier:

> I’ve been finding the transition back to the way things were quite difficult. I still know our codebases well, but the associated infrastructure isn’t easy to wrangle. Overall I haven’t been very productive over the last few months, but it’s getting better now.

On top come unexpected team dynamics as the previous architect shifts his focus:

> As I became less involved in the hands-on work, I struggled to be effective as a decision-maker. A lot of the bigger questions got deferred, and we had an increasing bias towards whichever approach was least committal.

On a different note, I am fascinated that Hugging Face has the funds to provide a quarter-million grant for open-source developers. How many of these funds do they provide?[^1]

> We considered selling the company, but we weren’t able to find a good fit. Instead, we’re back at the same sort of size we had before the investment. We’re very grateful to Hugging Face for a $250,000 grant to support our open-source work as our funding ran out, and we’ve applied successfully for a German R&D reimbursement grant that will give us up to €1.5m in unconditional funding.

To me, Explosion is one of the coolest exports that Berlin and Germany have to offer. Great to see them receive such grant.

[^1]: At roughly [0.1% of their Series D funding round](https://techcrunch.com/2023/08/24/hugging-face-raises-235m-from-investors-including-salesforce-and-nvidia/), there might be a few.
---
title: AI Act Approved by EU Parliament
author: Tim Radtke
date: '2024-03-14'
slug: ai-act-adopted-by-eu-parliament
categories:
tags:
---

The EU AI Act has finally come to pass, and pass it did [with 523 of 618 votes of the EU Parliament](https://www.europarl.europa.eu/news/en/press-room/20240308IPR19015/artificial-intelligence-act-meps-adopt-landmark-law) in favor. The adopted text ([available as of writing as PDF or Word document](https://www.europarl.europa.eu/doceo/document/TA-9-2024-0138_EN.html)---the latter is much easier to work with!) has seen a number of changes since the [original proposal by the EU Commission in 2021](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52021PC0206). 

For example, the current text reduces the set of systems considered high-risk somewhat by excluding those that are "not materially influencing the outcome of decision making" (Chapter III, Section 1, Article 6, Paragraph 3) except for those already covered by EU regulation such as medical devices and elevators. It also requires providers of any AI systems to mark generated audio, image, video or text content as such in a "machine-readable format and detectable as artificially generated" while also being "interoperable" (Chapter IV, Article 50, Paragraph 2).

And then there is the "right to an explanation" (Article 86). While data scientists and machine learning engineers hear "Explainable AI" and start submitting abstracts to [CHI](https://dl.acm.org/conference/chi), the provision does not appear to ask for an explanation of the AI system's recommendation, but only for a description of the overall process in which the system was deployed:

> Any affected person subject to a decision which is taken by the deployer on the basis of the output from a high-risk AI system listed in Annex III, with the exception of systems listed under point 2 thereof, and which produces legal effects or similarly significantly affects that person in a way that they consider to have an adverse impact on their health, safety or fundamental rights shall have the right to obtain from the deployer clear and meaningful explanations of the role of the AI system in the decision-making procedure and the main elements of the decision taken.

This reading[^1] is confirmed by the references to the "deployer" and not the "provider" of the AI system. The latter would be the one who can provide an interpretable algorithm or at least explanations.

Additionally, this only refers to high-risk systems listed in Annex III such as those used for, for example, hiring and workers management or credit scoring. Therefore, however, it also excludes high-risk systems falling under existing EU regulations listed in Annex I, such as medical devices and elevators.

The devil is in the details.

[^1]: Which is not based on any legal expertise whatsoever, by the way.

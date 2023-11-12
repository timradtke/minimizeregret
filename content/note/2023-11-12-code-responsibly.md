---
title: Code Responsibly
author: Tim Radtke
date: '2023-11-12'
slug: code-responsibly
categories:
tags:
---

There exists this comparison of software *before* and software *after* machine learning.

Before machine learning, code was deterministic: Software engineers wrote code, the code included conditions with fixed thresholds, and at least in theory the program was entirely understandable.

After machine learning, code is no longer deterministic. Instead of software engineers instantiating it, the program’s logic is determined by a model and its parameters. Those parameters are not artisinally chosen by a software engineer but learned from data. The program becomes a function of data, and in some cases incomprehensible to the engineer due to the sheer number of parameters.

Given the current urge to regulate AI and making its use responsible and trustworthy, humans appear to expect machine learning models to introduce an obscene number of bugs into software. Perhaps humans underestimate the ways in which human programmers can mess up.

For example, when I hear *Regulate AI*, all I can think is *Have you seen this stuff*? By [Pierluigi Bizzini for Algorithm Watch](https://algorithmwatch.org/en/algorithm-school-system-italy/)[^1] (emphasis mine):

> The algorithm evaluates teachers' CVs and cross-references their preferences for location and class with schools' vacancies. If there is a match, a provisional assignment is triggered, but the algorithm continues to assess other candidates. If it finds another matching candidate with a higher score, that second candidate moves into the lead. The process continues until the algorithm has assessed all potential matches and selected the best possible candidate for the role.

> […] [E]rrors have caused much confusion, leaving many teachers unemployed and therefore without a salary. Why did such errors occur?

> When the algorithm finds an ideal candidate for a position, **it does not reset the list of remaining candidates** before commencing the search to fill the next vacancy. Thus, those candidates who missed out on the first role that matched their preferences are definitively discarded from the pool of available teachers, with no possibility of employment. The algorithm classes those discarded teachers as “drop-outs”, ignoring the possibility of matching them with new vacancies.

This is not AI gone rogue. This is just a flawed human-written algorithm. At least Algorithm Watch is aptly named *Algorithm* Watch.

Algorithms existed before AI.[^2] But there was no outcry, no regulation of algorithms before AI, no “[Proposal for a Regulation laying down harmonised rules on artificial intelligence](https://digital-strategy.ec.europa.eu/en/library/proposal-regulation-laying-down-harmonised-rules-artificial-intelligence)”. Except there actually *is* regulation in aviation and medical devices and such.[^3] Perhaps because of the extent to which these fields are entangled with hardware, posing unmediated danger to human lives.

Machine learning and an increased prowess in data processing have not introduced more bugs into software compared to software written by humans previously. What they have done is to enable applications for software that were previously infeasible by way of processing and generating data.

Some of these applications are… not great. They should never be done. Regulate those applications. By all means, prohibit them. If a use case poses unacceptable risks, when we can’t tolerate any bugs but bugs are always a possibility, then let’s just not do it.

Other applications are high-risk, high-reward. Given large amounts of testing imposed by regulation, we probably want software to enable these applications. The aforementioned aviation and medical devices come to mind.[^4] Living with regulated software is nothing new!

Then there is the rest that doesn't really harm anyone where people can do whatever.

Regulating software in the context of specific use cases is feasible and has precedents.

Regulating AI is awkward. Where does the if-else end and AI start? Instead, consider it part of software as a whole and ask in which cases software might have flaws we are unwilling to accept.

We need responsible software, not just responsible AI.

[^1]: [I tried to find sources](https://bayes.club/@timradtke/111087876472984305) for the description of the bug provided in the article, but couldn’t find any. I don’t know where the author takes them from, so take this example with the necessary grain of salt.
[^2]: Also, much of what were algorithms or statistics a few years ago are now labeled as AI. And large parts of AI systems are just if statements and for loops and databases and networking.
[^3]: Regulation that the EU regulation of artificial intelligence very much builds upon. See “Demystifying the Draft EU Artificial Intelligence Act” (https://arxiv.org/abs/2107.03721) for more on the connection to the “[New Legislative Framework](https://single-market-economy.ec.europa.eu/single-market/goods/new-legislative-framework_en)”.
[^4]: Perhaps this is the category for autonomous driving?
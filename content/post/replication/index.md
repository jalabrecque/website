---
layout: post
title: "Repliducibustness"
date: 2021-01-29T01:13:14-05:00
published: tru
---

So I've been reading a bunch about replication, reproducibility and robustness and I've concluded there aren't enough words that start with 'R'. I say that half tongue in cheek but half seriously. These terms are used in many different fields sometimes in very different ways. Babra covers the variation in these terms well [here](https://arxiv.org/abs/1802.03311). And there's a lot of it. I feel like it's a lost cause to try and standardize the definitions of these terms. [The Turing Way has tried to categorize these terms](https://the-turing-way.netlify.app/reproducible-research/overview/overview-definitions.html) into a nice 2x2 table:

![](https://the-turing-way.netlify.app/_images/ReproducibleMatrix.jpg)

but you can't fit greater than 4 concepts into a 2x2 table forcing you to merge some of them.

Which brings me to the reason there are more than 4 concepts related to reproducibility. The production of scientific knowledge involves many different pieces, data, how you collected that data, the population the data was collected from, the researchers themselves, the statistical methods, causal methods, software, statistical packages etc. There are many more. The idea behind all of these reproducibility/replication/robustness is to change one aspect of a study and see if your results change. If you get the same results, you know they aren't sensitivity to the aspect of the study you changed. In this way you can eliminate possible explanations for your result.

If you replicate some else's study and find the same results, it becomes very unlikely that the original study p-hacked, HARKed or cherry-picked results. If you analyses the same data with two statistical models that rely on different assumptions and get the same answer, you know your answer doesn't depend heavily of statistical assumptions. So the reason why we need more than 4 terms for all this is because we can consider it a new "reproducibility" concept whenever we're talking about changing a different aspect of a study. And since there are more than 4 aspects of a study, there will be more concepts.

People like [Brian Nosek recognize this and say let's just call everything replication](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3000691) because it's the same underlying principle that underlies all of them. It kind of makes the term useless if we're using the same term to refer to all these different types of replication, no?

To me, I think we just need to be clear about what aspect of the study we're changing and what our goal is in changing that aspect of the study. I don't think we need a different word for all of these different types of replication. But really, however this plays out, I don't really mind as long as we all recognize that there is one underlying idea behind all of this repliducibustness. 


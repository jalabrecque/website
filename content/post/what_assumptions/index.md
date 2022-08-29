---
layout: post
title: "Under what assumptions does your estimate mean anything?"
date: 2022-08-25T01:13:14-05:00
published: false
---

Imagine you've contacted a construction company to come build a dormer in your house. They charge by the hour so you, of course, ask how long it will take. Tony, from the company, says, "somewhere between 7 and 9 hours." You start doing the calculations in your head when the person quickly adds, "but of course, I may be wrong." Uh. What? You prod him to determine how likely the range of 7-9 hours is to be wrong and, if it is wrong, by how many hours could it be off. Tony mumbles something about, "well, you never know, really, sometimes things come up." You ask how often things come up. "Well, basically always." Always?? 

How likely would you be to hire this company? It's ok that they can't be 100\% precise with their estimate, but from what they told you, you cannot make any decisions unless you make some additional information such as " 90\% of the time it's within 7 and 9 hours but it's never more than 12". It's the company's responsibility to explain to you under what conditions the range they gave you could be wrong and some sense of how far off the true time could possibly be. And then ideally, some evidence, maybe from past jobs they've done, to support the range of uncertainty they've given you.

But in epidemiology, many people seem to be ok with statements like those in the first paragraph. 

In epidemiology, it is common to report an estimate of a casual effect (often referred to as an association) with the caveat that there is always a risk of unmeasured confounding. So, what they are essentially saying is, "we estimate a causal risk ratio of 1.2 assuming exchangeability is perfectly satisfied" (i.e. no uncontrolled confounding or selection bias...consistenct and positivity are never mentioned). But then they add, "but there's always some residual confounding." Ok. So the estimate is causal conditional on there being no confounding and the probability of their being no confounding is 0. 

Logically, then, the information is useless. If I want to know something about the value of RR and I tell you E[RR|Exchangeability=True] = 1.2 and then I tell you P(Exchangeability=True)=0, I haven't give you any information at all about the value of of A at all. In order, to give you information about the causal RR, I need to give you information on plausible ranges of RR given that exchangeability is not satisfied which requires me to make statements about how exchangeability is violated. 

I think what most people are doing, some explicitly and some implicitly, is saying, "yeah, there's unmeasured confounding but it's probably not much and it wouldn't change my conclusion." Of course, no further rationale is given for why this would be true but it does have some interesting implications.

The first is that the authors are admitting that their effect is not point identified. They're saying their estimate is only partially identified and sits within a small range around the point identified estimate. As soon as you say there's even a risk of one of the causal assumptions being violated, you are admitting that only partial identification is possible (unless you're willing to make strong assumptions about the source of confounding) and even then, further assumptions are required for partial identification to place bounds on how violations of the assumptions bias the estimate.

The second is that though these authors make statements about the potential for unmeasured confounding, and likely making some assumptions about bounds on the true effect, in other ways they continue to act as though their estimate is point identified. For example, for authors using p-values, they are immediately admitting that all of their p-values are not valid. Particularly if they're using NHST and end up with a result that is p=0.049 and claim this is significant, the only belief that is logically consistent with both 0.049 being significant and that the risk of unmeasured confounding is not 0 is that the risk of confounding multiplied by the potential bias if confounding is present is extremely small. So either the risk of confounding is extremely small or the potential bias is there is confounding is extremely small both of which are very strong assumptions.




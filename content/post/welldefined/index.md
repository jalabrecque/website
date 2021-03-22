---
layout: post
title: "Policies in a world with only causal inference"
date: 2021-03-22T01:13:14-05:00
published: true
---

There are many potential interventions or policies that could greatly increase human well-being that we, currently, cannot generate evidence for using a formal causal inference framework. The direct implication of this is that if we only considered evidence from formal causal inference we would _never_ be able to implement these interventions or policies. Worse still, I've been imagining what an ill-intentioned politician could get away with in a world where we only relied on formal causal inference. They could avoid having their policies evaluated by ensuring that the policy affected everyone at the same time to make sure there was no comparator population (a positivity violation). And if any causal inference smartass wanted to use interrupted time series, all this politician would have to do is implement a second policy at the same time and it would be impossible to disentangle the effect of the two policies.

In this case, would the causal inference community just stand around saying, "Sorry, there's really nothing we can do here." I doubt it. While the causal assumptions we teach in class are the basis of most we do, they aren't the end of our tool bag. We can always make additional assumptions--for example, about how the original assumptions are violated--that help us estimate the effect we're interested in. Or use some other piece of information to help us identify the effect. Or we can use sensitivity analyses to inform ourselves about what bias we would expect from violations of our original assumptions.

Another thing that occurred to me was that if we were trying to study an intervention aimed as reducing health inequalities and we realized the causal assumptions were not satisfied, we might want to employ additional assumptions that err on the side of increased benefit for a historically disadvantaged group. But here we're really getting into mixing the goals of causal inference, which is to estimate unbiased causal effects, with more general societal goals. And there's nothing really wrong with that. As I mentioned [last post](https://www.jeremylabrecque.org/post/political_assumptions/), causal inference is just a tool, we are the ones who decide what our goals are.



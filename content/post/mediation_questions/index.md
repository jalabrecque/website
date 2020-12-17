---
layout: post
title: "Mediate for what?"
date: 2020-12-08T01:13:14-05:00
published: true
---

As time goes by, the clear it becomes to me that most researchers don't know how to ask a clear research question. I'm part of a systematic review right now about mediation in genetics and I find it impossible to read the papers because the question they actually want the answer to is never written clearly. It must be inferred by the methods, results and discussion. And I refuse to blame these researchers themselves, we're terrible at teaching how to ask a good question (I'm trying!). The problem starts with teaching students about regression before teaching them to come up with their question. It results in people who can only think of questions in terms of regression coefficients or in terms of whatever statistical procedure they learned.

More and more I think that mediation is the perfect example of this. Mediation methods are designed to answer generic questions about some combination of changing the exposure by one unit and the mediator by whatever amount it changes by for a change in exposure. Yeah, yeah, I'm being sloppy here. But my point is that many people, particularly in public health, want the answer to variations on mediation parameters, not the parameters that mediation analyses normally give you. 

To use an example from a recent paper I was involved in, [Estimating Reductions in Ethnic Inequalities in Child Adiposity from Hypothetical Diet, Screen Time, and Sports Participation Interventions](https://repub.eur.nl/pub/130528/), we wanted to know how improvements in, for example, screen time could improve ethnic inequalities in adiposity. We weren't actually interested in setting everyone to the same value of screen time. We were interested in knowing how the inequalities change if those above some threshold in daily screen time (we used 2 hours) we brought down to 2 hours, leaving all those who already had daily screen time under 2 hours to whatever value they were observed with. In this way we were mimicking the idealized effect of a policy. 

But there are no out-of-the-box methods to do this. (Aside: I'm hoping to have an out-of-the-box R package to do this coming out soon. In the mean time you can contact me or use the code from that paper which was intended to be easy to use to answer other questions.) The lack of out-of-the-box methods means that most people can't answer the more nuanced question we answered in that paper which leads them to ask questions they can answer such as questions about controlled direct effects or 4-way decomposition, etc. If people were trained to ask good questions, they could recognize that the generic mediation analysis doesn't answer the question they want the answer to and maybe they could seek out someone who could help them answer that question. This actually ties into a previous post about [redeploying methodologists](https://www.jeremylabrecque.org/post/improving_methods/). If more methodologists were available to help applied researchers, maybe they would be better able to answer the questions they're actually interested in.  





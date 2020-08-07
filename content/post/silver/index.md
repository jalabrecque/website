---
layout: post
title: "Nate Silver, confusion between prediction and causation"
date: 2020-09-07
published: true
---



A huge problem I often see in health research is the inability to formulate a clear research question. If you start a project without a clear question it's very easy to apply the wrong methods and misinterpret results. A very common error I see is confusing prediction and causation. A telltale sign of that is when people adjust their prediction model for confounders.

Nate Silver apparently has the same problem:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Yes, I disagree that there&#39;s a difference between &quot;modeling designed to improve forecast accuracy and modeling designed to explore causal theories&quot;. I think the best way to test whether causal theories are true is generally through true out-of-sample prediction.</p>&mdash; Nate Silver (@NateSilver538) <a href="https://twitter.com/NateSilver538/status/1291398402027257861?ref_src=twsrc%5Etfw">August 6, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

The way you run and think about analyses is **ENTIRELY** different depending on whether your goal is prediction or whether your goal is causation. Read [A Second Chance to Get Causal Inference Right: A Classification of Data Science Tasks](https://amstat.tandfonline.com/doi/full/10.1080/09332480.2019.1579578) if you want more clarity on this issue

Another recent example: 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">People are moving around less in states with more COVID-19 deaths, but it&#39;s not a huge effect. Whether a state is formally re-open doesn&#39;t seem to matter that much, but note that openness/closure is correlated with these other variables so that makes it a bit tricky to evaluate.</p>&mdash; Nate Silver (@NateSilver538) <a href="https://twitter.com/NateSilver538/status/1256976450328068101?ref_src=twsrc%5Etfw">May 3, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Here Silver is equating importance with p-values. Rookie mistake. Even p-value advocates (which I am not) will be quick to point out this error. It's hard to tell excatly what is the most important variable here because we'd need to know the scale of the variables but reopening is equivalent to a $\frac{7.27}{0.46}=15.8$ difference in Trump's margin of victory in a state. And also equivalent to a $\frac{7.27}{0.81}=9.0$ swing in temperature (between winter and summer). It's clear that reopening likely does play a large role but it requires the ability to interpret statistics properly to see that. (Disclaimer: this model is ridiculously simplistic and to be able to say any of these things would require a much **MUCH** more careful analysis.)
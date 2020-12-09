---
layout: post
title: "Decision science and causal inference: separated at birth"
date: 2020-08-11T01:13:14-05:00
published: false
---

The [Harvard Center for Health Decision Science](https://chds.hsph.harvard.edu/approaches/what-is-decision-science/) defines decision science as, “the collection of quantitative techniques used to inform decision-making at the individual and population levels,” listing no fewer than 13 such quantitative techniques--including microeconomics, statistical inference and computer science--which all contribute in some way to decision making. Yet there is one conspicuous absence: causal inference.

Causal inference is the study of how to infer causation from data. By using concepts such as counterfactuals--$Y^{A=a}$, defined as the value $Y$ would have taken if we set $A$ to $a$--we can easily compare the change in an outcome had we taken two different courses of action: $Y^{A=a}-Y^{A=a^*}$, where $a^*\neq a$. If this reminds you of the type of information that would be useful for decision making it's because, recognized or not, causal inference is one of the cornerstones of decision making. We can't possibly make decision without knowing the causal consequences of making those decisions.

Ok. Maybe the Harvard Centre for Health Decision Science simply forgot to include causal inference on their list. It's just a website afterall and some of the top experts in causal inference are also in the Harvard T.H. Chan School of Public Health. But I have yet to find a medical decision making textbook that gives _any_ space to causal inference. And it's easy to imagine rewriting many basic concepts in medical decision making in terms of counterfactuals. Cost-effectiveness is often written as $\frac{\Delta C}{\Delta Y}$ where $\Delta C$ is the change in cost (or difference in cost between two decisions) and $\Delta Y$ is the change in some health outcome (or difference in the outcome between two decisions). This can easily be rewritten as counterfactuals comparing decision $A$ and decision $B$: $\frac{C^A - C^B}{Y^A - Y^B}$. 

You might wonder what's the value of simply rewriting these equations with counterfactuals. By doing this we tie this cost-effectiveness parameter directly to all the theory and methods used in causal inference. For example, we can use all the quantitative bias analyses from causal inference on cost-effectiveness parameters and determine, for example, how much bias would be required to change our mind about a decision.





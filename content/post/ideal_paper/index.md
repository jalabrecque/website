---
layout: post
title: "The characteristics of an ideal causal paper"
date: 2022-07-06T01:13:14-05:00
published: true
---

I was daydreaming the other day and was thinking about what would be in an ideal, observational study with a causal goal. I'll update this as I think of things:

1) **A clear causal question** preferably written in counterfactual notation and accompanied by a table outlining the [target trial](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5550532/).       

2) Carefully consider the best method or, ideally, multiple methods to answer this question. Triangulation (see [Lawlor 2016](https://academic.oup.com/ije/article/45/6/1866/2930550) or [Matthay 2020](https://www.sciencedirect.com/science/article/pii/S2352827319301545)) leverages different causal methods to estimate the same quantity to learn more about the potential for bias than you would have learned looking at the results of each study separately.

3) The **causal assumptions** required to interpret the estimates as causal are clearly written in terms of question at hand. So not, for example, "we assumed exchangeability was satisfied," but instead, "after adjusting for age, sex, blood pressure etc, the BMI of those who did and didn't receive my miracle weight-loss drug would be the same on average if they received the same treatment (conditional exchangeability)." And ideally, whenever an estimate is interpreted as causal there is a reference to the previously mentioned assumptions so it's always clear that the statement about causality is conditional on the assumptions being satisfied. I've tweeted about this kind of stuff before:  <blockquote class="twitter-tweet"><p lang="en" dir="ltr">E.g. After adjusting for age, sex, blood pressure etc, the BMI of those who did and didn&#39;t receive my miracle weight-loss drug would be the same on average if they received the same treatment. (conditional exchangeability) <a href="https://t.co/O4YwKFmF0e">pic.twitter.com/O4YwKFmF0e</a></p>&mdash; Jeremy Labrecque (@ja_labrecque_) <a href="https://twitter.com/ja_labrecque_/status/1039951782259118082?ref_src=twsrc%5Etfw">September 12, 2018</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

4) Reports estimate(s), confidence intervals, standard error, and, if you are so inclined, the p-value (being sure to interpret all these quantities correctly). 

5) **Bias analyses.** Show me what happens when your assumptions are violated. Bonus points if you use external knowledge to show me the bias that would result from the most likely violations of the assumptions. Negative controls can also work nicely here.

6) Don't make statements about potential policy impacts. 

7) **Reproducible code and analysis**: All code for the analysis should be included and well-documented. If using a data source that is public or that can be accessed by other researchers (e.g. UK Biobank) include code for downloading and cleaning the data. Even if using a private data source, still include as much code from the data cleaning process as possible. The methods section of the paper should contain a thorough description of the analysis so that no aspects of the analysis are unclear.

This is not a complete list by any means. Feel free to contact me by any of the means below if you have suggestions.






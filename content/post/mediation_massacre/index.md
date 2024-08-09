---
layout: post
title: "How bad do methods have to be for us to take action?"
date: 2023-07-25T01:13:14-05:00
published: true
---

First, I want to strongly state that my goal here is not to demean the authors here in any way whatsoever. If there were some way to present what they wrote that did not allow people to identify the publication I would do so. I sincerely believe they are motivated to improve our knowledge of human health.

My goal here is to ask the question: Is there are threshold at which methods are so bad that action must be taken?

Here is the paragraph from the paper. The topic is whether neighbourhood level deprivation is a mediator of the effect of ethnicity on deaths due to COVID. 

> **Selected confounders**
>
>Age, measured at 16 March 2020, and sex were included as covariates in this analysis due to lower age and proportion of women in the SAB population within UK Biobank. Additional confounders were not considered due to the mediation model and pathway specified.
>
>Specifically, mediation analyses assume that: (i) there is no exposure-outcome confounding; (ii) there is no mediator-outcome confounding; (iii) there is no exposure-mediator confounding and (iv) no mediator-outcome confounder is itself affected by the exposure. When ethnicity is set as the exposure, assumptions (i) and (iii) hold a priori as only unmeasured historical or genetic factors are true potential confounds of the construct of ethnicity. For assumption (ii), traditional confounders such as health behaviour or chronic disease are implausible confounders of deprivation and may further violate assumption (iv) as both can be argued to be influenced by ethnicity.15,16 Implausibility of confounders for deprivation within the model follows from a hypothesis supported by the literature that inequalities in health or health behaviours in people living with high deprivation are, in the most part, the result of high deprivation itself.17,18 The DAG shown in Supplementary figure S2 illustrates this concept in detail.

I want to reiterate here that I sincerely believe the goal of the authors here is to improve an important societal ethnic inequality. But unfortunately, their motivation does not extend to them learning how to properly use and interpret mediation analyses. 

1. **Both ethnicity and deprivation are problematic due to the consistency assumption:** Answering causal questions about poorly-defined exposures can lead to misleading answers. If you want to answer questions about the causal effect of ethinicity or deprivation you have to be able to both precisely define what is meant by those words and how you would change one's ethnicity or deprivation level. Without that level of specificity, it is not possible to really interpret the results of such a study even if the software used will nonetheless give a numerical answer.

2. **Not answering the right question:** There may be times when we are interested in the causal effect of ethnicity (whatever that might mean) but this is not one of them. If they are interested in the causal effect of ethnicity and reducing ethnic inequalities it suggests they want to reduce these inequalities by changing people's ethnicity (I know this is not their real goal but it's implied by their methods). What they want to know is how they can reduce health inequalities between ethnicities by intervening on neighbourhood deprivation. In other words, they want to know how a _descriptive_ measure (the inequality) would change after a _causal_ intervention on neighbourhood deprivation. They need other methods for this like the methods I used in [this paper](https://pubmed.ncbi.nlm.nih.gov/32618712/). And the most frustrating part is that their conclusion (below) clearly demonstrates they are trying to answer the question I think they should answer and NOT the mediation question.

3. **Assumptions (i) and (iii) definitely DO NOT hold a priori:** Either the authors have not thought this through or they don't understand the definition of a confounder. A confounder, roughly speaking, is a risk factor for the outcome that is not equally distributed across categories of the exposure (and is not itself caused by the exposure). If there were truly no confounders, this would mean that there are no historical reasons why different ethnicities might have different risks of the outcome. And we all know that's not true. And I'll also note that these assumptions are not required if they had answered the question I think they were trying to answer (mentioned in the previous point).

4. **If a variable violates assumption iv it definitely DOES NOT MEAN you should not adjust for it:** It means that the variable is both a confoudner AND a mediator and you have to deal with it in a special way. This is just a complete misunderstanding of mediation. 

After all this, I am comfortable saying this paper contains little to no useful information. And yet their conclusion is unabashedly strongly worded:


> **Conclusions**
>
> The excess risk of COVID-19 outcomes in South Asian and black communities could be substantially reduced with population level policies targeting material deprivation.

So now my main point. Is this acceptable? Is this ethical? How do we in the 21st century still allow these type of low-quality publications to exist? To me, it should be 100% unacceptable for something like this to be published and should come with some sort of consequences. These authors are not asking the right question (or at least not using the right method to answer their question) and have clearly put little to no time trying to understand the method they are using. This is dangerous. In the spirit of Doug Altman, we don't let surgeons operate without the proper training. Why do we let people do research without the right qualifications?


---
title: "Conditional vs marginal effects"
date: 2020-02-05T01:13:14-05:00
diagram: true
math: true
image:
  placement: 1
  preview_only: true
header-includes:
- \usepackage{tikz}
- \usepackage{amsmath}
- \usepackage{float}
- \usepackage{cite}
- \usepackage{caption}
- \usepackage{subcaption}
- \usepackage{fixltx2e}
- \usepackage{longtable}
- \usetikzlibrary{shapes, decorations,calc}
- \usepackage{pdflscape}
- \newcommand{\blandscape}{\begin{landscape}}
- \newcommand{\elandscape}{\end{landscape}}
- \usepackage{multirow}
- \usepackage{booktabs}
- \newcolumntype{L}{<{\centering\arraybackslash}m{9cm}}
- \usepackage{float}
- \floatstyle{plaintop}
- \restylefloat{table}
- \usepackage{longtable}
output:
  html_document:
    df_print: paged
    keep_md: TRUE
  pdf_document:
    keep_tex: yes
bibliography: /Users/jeremylabrecque/epidemiology/zotero/zotero.bib
csl: ije.csl
published: false
---





Marginal and conditional are two terms that often cause a lot of confusion in the literature. People use them in different contexts to mean different things and then argue that the other is wrong when they're talking about the same thing. Let's get rid of the more straightforward confusions first.

## Conditional effects

"Conditional effects" can be used in two ways. It would be nice if we could be clearer when speaking and writing to which of these we are referring to. 

#### 1) Effects within a stratum

The first is the effect within a subgroup: 

$$ E[Y^{A=1}-Y^{A=0}|Sex=women] $$

The above estimand is a conditional effect in that it is the effect of $A$ on $Y$ only with in those with $Sex=women$. So, conditional on being a woman, this is the causal effect.


#### 2) Effect estimates from conditional estimators

Conditional effects also refer to the type of estimation used to obtain the estimate. Likely the most common method to estimate causal effects is conditional regression--i.e. including covariates one wishes to adjust for in a regression model and interpreting the coefficient for the exposure as the causal effect. This is:

$$ E[Y^{A=1}-Y^{A=0}|Sex] $$

This is the effect of $A$ on $Y$ while holding $sex$ constant. Conditional estimators are easy to use but require extra assumptions to estimate average causal effects (ACE). This is because the ACE is _by its nature_ a marginal quantity. Conditional estimators attempt to estimate this marginal quantity by holding the covariates constant. But the covariates are not constant in the data set and when there are interactions between variables, the conditional estimator can be biased with respect to the ACE.[@Shrier2019;@Greenland1994]

Therefore, conditional estimators are only valid estimators of the ACE when the effect of the $A$ on $Y$ is homogeneous, the variance of the residuals when regressing the exposure on covariates is the same within all strata of covariates or there is no correlation between the heterogeneity of the effect of $A$ on $Y$ and the variance of the previously-mentioned residuals. The reasons for this can be found in Angrist and Krueger (1999).[@angrist1999]

## Marginal effects

At first I thought there was more confusion about conditional effects but now I think the opposite. People use marginal effects to refer to so many different things.

#### 1) Unadjusted associations

I've seen some use marginal effects to mean "unadjusted". I think it might be mostly among people who work a lot with RCTs where, at least for an ideal RCT, both adjusted and unadjusted estimates can yield unbiased estimates of the ACE. Confounding is omnipresent in non-RCT observational research that one would never refer to an unadjusted estimate as an "effect". 

#### 2) Marginally standardized effects

Particularly when working with non-linear models or interactions, you're stuck with a problem: there's no one estimate to report because your effect estimates depend on the strata you're in. What to do? What economists and people who use Stata love to do is standardize effects. There are different ways to do this as nicely explained by Muller and MacLehose.[@muller2014] I think most often the effects are standardized to the covariates distribution of the sample. For a binary exposure this is equivalent to taking the difference between the predicted average outcome when setting the exposure to 1 and when setting the exposure to 0.

To further confuse things, marginal effects at the means is also a thing. Basically, this is effect in the population when setting all covariates to their mean value. It feels a bit like a conditional effect in the sense of an effect within a stratum but here we're setting everyone's covaraites to the mean, not just looks within the stratum of people with mean values. 

#### 3) Marginal causal effects

Have I mentioned average causal effects are marginal in nature? The average causal effects is the same as the marginal causal effects and is the average causal effect in the population. This might sound a lot like marginally standardized effects but there's an important difference: interactions. Marginal standardization is done with an outcome model meaning you have to model the outcome correctly. If you're missing interactions between exposure and covariates or even between covariates, marginal standardization will not estimate an average causal effect.

There is, however, another way. You can use inverse probability of treatment weighting to balance covariates across levels of exposure. By balancing covariates rather than holding them constant, you make 


## Combinations

Once you understand the concepts of conditional and marginal effects, you can see that you can estimate effects that are both. You can condition on some variables and average across other. You could use IPTW, for example, to estimate the marginal effect of an exposure solely within women. Then you would have the marginal causal effect of the exposure conditional on being a woman. 



## References

<div id="refs"></div>

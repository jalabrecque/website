---
title: "Why do we even bother with conditional estimators anymore?"
image:
  placement: 1
date: 2019-09-04
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
bibliography: V:/HomeDir/495055(J. Labrecque)/Analyses/library.bib
csl: ije.csl
published: true
---

A recent paper by Shrier et al was recently sent to me: [Challenges in interpreting results from ‘multiple regression’ when there is interaction between covariates](https://ebm.bmj.com/content/early/2019/08/22/bmjebm-2019-111225.abstract). If you're not familiar with conditional versus marginal estimates it's a nice review of this concept and even includes a formula in the appendix allowing you to calculate the difference between the conditional and marginal estimates.

Bottomline: when the effect of an exposure or treatment differs across a covariate, conditional estimates (e.g. the coefficient from multiple regression) from models that do no include the interaction between treatment and those covariates will not estimate the population average treatment effect. This means, to correctly estimate the population average treatment effect you have to correctly specify all interactions with treatment in your model (and average over covariates). We already know that measuring and adjusting for all confounders is an impossible goal and now we're being asked to specify all interactions?

As Shrier et al point out, inverse probability of treatment weighting will estimate the population average treatment effect without having to specify treatment-covariate interactions. So why do we even bother with conditional estimators? Well, the difference is unlikely to be very large so maybe it's not worth the bother. Ok, maybe the difference isn't very large but there are other reasons to not use conditional estimators.

First, you're not a slave to your link function. With binary outcomes, people tend to report odds ratios because that's what the exponentiated coefficients gives you. Estimating risk differences or risk ratios is possible but a hassle because of convergence issues, etc. But with inverse probability of treatment weighting (and other methods that estimate marginal effects like g-computation and targeted maximum likelihood estimation), it's easy to choose the parameter you want.

Second, inverse probability of treatment weighting easily lets you check balance in your confounders and whether positivity is satisfied. This is something that should be default behaviour for causal inference.

And last, inverse probability of treatment weighting and other marginal methods like g-computation and targeted maximum likelihood estimation can easily be compared to each other as a modeling check because, if they disagree, you know _at least_ one model is wrong (note _at least_, most likely all are wrong) and you can go back and recheck your models.

So, really, why do we even bother with conditional estimators anymore? 




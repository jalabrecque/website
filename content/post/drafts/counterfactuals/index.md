---
title: "Creative counterfactuals"
diagram: true
math: true
image:
  placement: 1
  preview_only: true
date: 2019-08-02T21:13:14-05:00
header-includes:
- \usepackage{tikz}
- \usepackage{amsmath}
- \usepackage{float}
- \usepackage{bm}
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
published: false
---

We're so lame with how we teach counterfactuals. Ok. I'm so lame. The causal effect of $A$ on $Y$ is:

$$ E[Y^{a^*}-Y^{a}]$$

Great, you've written down how $Y$ changes when you change $A=a$ to $a^*$. This is like teaching people algebra and only teaching them you can add and subtract variables. Well, I guess we also teach about mediation parameters which can get more involved. But there's so much more we can do! And there's so much more that's being done!

**Example 1: Health inequalities.** At some point people looked at mediation analyses and thought, "that looks a lot like trying to reduce a health inequality by intervening on some mediator." It does kind of look like that but, conceptually, the questions are quite different. Sometimes people figure out that they want to know the proportion eliminated when setting some mediator $M$ to $m$: 

$$ 1 - \frac{E[Y^{a^*,m}-Y^{a,m}]}{E[Y^{a^*} - Y^{a}]} $$

But that's not really what you want to know because in a health disparity you're not intrested in intervening on $A$, only $M$. So it makes more sense to write:

$$ 1- \frac{E[Y^m|A=a^*-Y^m|A=a]}{E[Y|A=a^*-Y|A=a]} $$

**Example 2: Explained heritability.** This is a cool one because you ALWAYS see estimands as the expected value of variable. But heritability is the proportion of the variance in a phenotype that is explained by genetics:

$$ 1- \frac{Var(P|G)}{Var(P)}$$

But we might want to know about the pathways through which genetics are explaining the variation in P. Which means we want to know:

$$ \frac{Var(P^m|G)-Var(P|G)}{Var(P)}$$

If you've seen an estimand that is the variance of a counterfactual before, I'd be interested in seeing it.

**Example 3: Predictimands.** Here we estimate the risk of something in a counterfactual world. So, for example: 

$$ P(T^{v=∞}≤ t_{hor}|X)$$

Which is the probability that $T$ occurs within some time horizon $t_{hor}$ in a world where $V$ is set to $∞$ (i.e. the event V never happens, maybe some competing event). 

**Example 4: The causal effect of implementing a prediction algorithm.** Say we have developed some prediction model $P(Y|\boldsymbol{X})$ to predict $Y$ using a set of covariates $\boldsymbol{X}$. But we want to know whether this will prevent $Y$ if we implemented it in the clinic for example. Say we will implement treatment $A$ when the probability of the outcome using the prediction model is greater than $0.8$. The causal effect of this would be:

$$ E[Y - Y^{A=I(P(Y|\boldsymbol{X})>0.8)}] $$
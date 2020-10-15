---
title: "NHST: the answer to a question no one asked"
image:
  placement: 1
date: 2019-11-25
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

The null hypothesis significance testing (NHST) debate continues to churn on. There was a [recent seminar](https://www.niss.org/news/digging-deeper-radical-reasoned-p-value-alternatives-offered-experts-niss-webinar) where Jim Berger, Sander Greenland and Robert Matthews all talked about how to move beyond NHST. I have never been a big user of NHST given that I trained in McGill University's epidemiology department where, and I'm not kidding, you could here a quiet gasp from the audience whenever invited speakers performed a NHST where simple estimation would have sufficed.

Now I'm at Erasmus MC where there is a much more tolerant attitude toward NHST and it has really forced me to dig deeper into what I think about NHST. But instead of pushing me toward some middle ground, I'm now having difficulty finding any situations where you would care about the result of a significance test.

If you're doing causal inference in epidemiology, you're probably doing it for one of two reasons: *etiology* or *decision-making*. 

If you're doing etiology, you don't have a yes/no decision to make at the end of your study so estimation seems much more natural. One might argue that a journal has a binary decision to make about whether to publish your study or you might have a binary decision about whether to continue with this line of research. For the journal, hopefully other considerations about the quality of an article will be much more important and that a high-quality study finding 0.051 will be preferred over a poor-quality study finding 0.049. The same logic applies with whether to continue on the same research line.

If you're estimating causal effects for decision-making, any decision will have many additional costs and benefits which should be factored into the decision. The only thing statistical significance factors in is random error. Therefore, the NHST gives us a yes/no answer to a question nobody asked: what treatment should I take if I want my outcome to be higher, _all else being equal_. People want to know, which treatment would maximize the difference between benefits and costs because all else is never equal.

Imagine you're a policy maker trying to whether drug A or drug B should be on the market. In separate trials, you find similar effect estimate for both drugs but for drug A p=0.049 and for drug B p=0.51. Which do you put on the market? Everyone will answer drug A because we have slightly more precision for that estimate (given equal effect sizes). But what if I tell you that drug B is much cheaper and we can therefore afford to treat more people than if we used drug A? Or what if I told you that drug A has potentially serious side-effects while drug B is almost harmless? In both these cases you've changed your mind right? It's easy to see that random error is only part of your decision and that any decision made on statistical significance alone might ignore important considerations!

So if NHST isn't useful for etiology or decision-making, where is it useful? I can be convinced that it's useful for some modeling decisions such as choosing between models when using fractional polynomials or splines. But even then, I much prefer to make modeling decisions based on substantive knowledge (e.g. like choosing whether or not include an interaction term). 

Some argue that we need it to filter import results from non-important results such as in genome-wide association studies. My answer is that genetic variants on either side of any threshold you use for a NHST will have essentially equal evidence with respect to their "importance". So I suggest simply ranking variants by p-values and acknowledge that evidence for all these variants is on a spectrum. Some would then argue that that is not possible because the results cannot focus on all variants but has to be limited to some. Fine, choose a cutoff for the variants you want to discuss but just be honest that this cutoff is arbitrary and that it isn't the borderline between "true" and "false" variants or "hits" and "misses".





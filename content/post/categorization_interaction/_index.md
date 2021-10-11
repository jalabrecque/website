---
title: "How categorizing variables can induce interactions where there are none"
date: 2021-10-10T01:13:14-05:00
math: true
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
published: true
---


I saw a talk where the speaker found that a continuous biomarker was not related to the outcome but if you interacted it with disease status, which was a binary variable created by taking a specific quantile of a continuous variable. That reminded me of a paper by Thoresen [Spurious interaction as a result of categorization](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-019-0667-2). 

So I tried to replicate the results of the speaker but without an interaction. First I generated two variables $biomarker$ and $disease\\_cont$ that are continuous and correlated by their common ancestor $u$. I binarize variable $disease_\\cont$ at the 75th percentile. Then I make an outcome that is only a function of continuous disease status and not a function of the biomarker. 


```r
n <- 1e5
u <- rnorm(n)
biomarker <- u + rnorm(n)
disease_cont <- u + rnorm(n)
disease_bin <- as.numeric(disease_cont > quantile(disease_cont, 0.75))
outcome <- disease_cont + rnorm(n)
```

If we regress the outcome on the biomarker, continuous disease status and an interaction between the two we find that only disease status is related to outcome and we find no interaction:


```r
(lm(outcome ~ biomarker*disease_cont) |> summary() )$coefficients |> round(2)
```

```
##                        Estimate Std. Error t value Pr(>|t|)
## (Intercept)               -0.01          0   -2.16     0.03
## biomarker                 -0.01          0   -2.06     0.04
## disease_cont               1.00          0  390.24     0.00
## biomarker:disease_cont     0.00          0    0.54     0.59
```

But if we do the same with the binary disease variable we find entirely different results: 

```r
(lm(outcome ~ biomarker*disease_bin) |> summary() )$coefficients |> round(2)
```

```
##                       Estimate Std. Error t value Pr(>|t|)
## (Intercept)              -0.52       0.00 -103.89        0
## biomarker                 0.30       0.00   80.34        0
## disease_bin               2.19       0.01  190.39        0
## biomarker:disease_bin    -0.15       0.01  -19.51        0
```

Now, not only do we find strong evidence of an interaction, we also find strong evidence that the biomarker is related to the outcome which we know it is not! In the paper mentioned above they explained why this comes about.

I have no idea whether this was what happened in the talk I saw but I do wonder how often this happens in the literature. Yet another reason you should (almost) never categorize a continuous variable.

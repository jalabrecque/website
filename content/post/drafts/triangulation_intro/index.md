---
title: "Why is everyone talking about triangulation all of a sudden?"
image:
  placement: 1
date: 2020-07-31
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

Replication is an important part of the scientific process which involves attempting to reproduce a result while changing one or more aspects of a study. If the replication achieves the same result as the original study while only changing one aspect of the study (_e.g._ different sample, different population, different methods, different researchers) this gives us confidence that the result is not sensitive to that aspect of the study. For example, if we replicate a result in another sample of the same population, we can be more confident that the original result was not due to chance. Or if, we were concerned about fraud or inappropriate analyses, we would feel more confident that this was not the case if another research group could independently replicate the original result. By isolating and varying one aspect of a study we can determine whether a result is robust to that change.

The idea behind triangulation is the same except it varies the causal assumptions that are required to give a result a causal interpretation. If we get the same causal effect using a method that requires different assumptions, we might be more confident that the result an unbiased causal effect. In this way, triangulation is simply replication while varying causal assumptions instead of data or researchers. Given the difficulty of inferring causation with observational data, triangulation is an additional tool available to researchers to increase confidence in causation.

Triangulation is still relatively new in the epidemiologic literature[TODO LAWLOR, MATTHAY] but can clearly contribute to helping in inferring causation. Here, we propose a definition for triangulation using counterfactuals. We discuss some key considerations including extra assumptions required for good triangulation as well important obstacles that may prevent or complicate triangulation. Lastly, we 
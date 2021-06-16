---
title: "The tale of triangulation and the car mechanic"
image:
  placement: 1
date: 2021-06-16
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
published: true
---

For the past like 15 years I've been listening to the radio show [Car Talk](https://www.cartalk.com/). Even now that it's only reruns, I listen every week. One of the things I've learned is that, if you are having car troubles and you suspect a specific part is responsible for it, the easiest thing to do is just replace that part. If the car troubles disappear then that part was most likely the cause. Makes sense right?

This is how a lot of science works. We have the results of a scientific study and we want to demonstrate that the only explanation for these results is that the theory we're testing is true. But there are other possible explanations. Maybe we didn't measure some variables well. Maybe we sampled in a way that caused a bias in our results. Maybe we tortured the data until we got the result we wanted. Maybe we just got unlucky (random error) and the results look like they support our theory but in the true population they don't. Maybe we just made up the data!

There are ways we can test each of these explanations. If you think the result is due to random error or data torturing, replace the old sample with a new sample. If the results are the same, then you can eliminate those explanations for the results. If you think one of the variables was measured wrong, measure that variable again. If the results stay the same, then you've eliminated that explanation. If you think the data are made up, ask another, independent research group to run the same study to see if they get the same results. You can do this with any part of a study.

Which brings me to triangulation. All triangulation is is replacing the causal assumptions behind a scientific result. Every study requires causal assumptions which we can't verify. We just have to assume they're true. But if we run the same study (or as similar as possible) using different causal assumptions and get the same result, we can be more confident that our result isn't just due to the causal assumptions used. Well, it's a bit more complicated than that. If you used two methods that might have similar bias, they might agree and both be biased! So triangulation requires some thought, but the basic idea is the same. 
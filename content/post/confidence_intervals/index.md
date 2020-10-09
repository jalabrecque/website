---
title: "Put the horse before the cart"
math: true
date: 2020-10-08T01:13:14-05:00
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
bibliography: /Users/jeremylabrecque/epidemiology/zotero/zotero.bib
csl: ije.csl
published: true
---

So why do we put our estimates directly in the main text but measures of precision such as confidence intervals in parentheses? I think most people would interpret this to mean that the estimate is more important than the confidence interval. Twitter has been angry recently with people rightfully pointing out that the point estimate is only the most likely value, not the true effect: 

<blockquote class="twitter-tweet" data-conversation="none"><p lang="en" dir="ltr">I am willing to forgive epidemiologists for ignoring variance on many occasions, but not this one. The point estimate is not &quot;the effect&quot;</p>&mdash; Maarten van Smeden (@MaartenvSmeden) <a href="https://twitter.com/MaartenvSmeden/status/1311326102195974145?ref_src=twsrc%5Etfw">September 30, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

So I wonder why we don't just do the opposite, e.g.: The data, given assumptions are satisfied, are consistent with a risk difference between $0.05-0.09 (\textrm{point estimate:} 0.07)$.  It will force people to acknowledge the uncertainty directly (to some degree anyway). On the topic of confidence intervals, [Naimi and Whitcomb have a nice paper covering how they should be interpreted](https://pubmed.ncbi.nlm.nih.gov/31994696/). [@naimiCanConfidenceIntervals2020] And I'd also suggest this paper by [Rafi and Greenland to replace the word confidence with compatibility](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-020-01105-9).[@rafi2020]



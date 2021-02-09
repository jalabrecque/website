---
layout: post
title: "Instrumental variables for 'confounder control'"
date: 2021-02-09T01:13:14-05:00
published: true
---

This is maybe one of my more niche pet peeves. I see in a lot of places that people use or suggest instrumental variable (IV) analysis "to control for confounding." 

First, to me it demonstrates a misunderstanding about what it is that IV analysis is doing. Confounder control comes from adjusting for confounder or standardizing across them. In most IV analyses, the majority of the confounders aren't available so how can they be controlled for? IV analysis is a different type of identification strategy whose assumptions don't even require reference to confounders (except for instrument-outcome confounders).

Which brings me to my second point: I think it's perfect demonstration of how we think about methods before research questions. Confounder control has such a privileged position in epidemiology and biostatistics training that we forget, sometimes, that it isn't our goal! Our goal is a specific causal question. When people say they use IV analysis to control for confounding, I see this obsession with confounder control coming through. If we taught students instead to start with a research question and then come up with an identification strategy--in other words, to keep the research question entirely separate from the methods--I don't think you'd see people saying something like this.

Lastly, smallest of the small points, as soon as there are more than two variables of interest in an analysis, _e.g._ mediation analysis (exposure, mediator, outcome), IV analysis (IV, exposure, outcome), we need to be more specific about what we mean by confounding. When it's just a confounder control analysis of the effect of an exposure on an outcome, it's clear the word confounding refers to exposure-outcome confounding. But in mediation analyses it could be exposure-mediator, exposure-outcome or mediator-outcome confounding. In IV analyses if could be exposure-outcome or IV-outcome. Actually, maybe this is why so many people butcher the independence assumption in IV analyses (i.e. no IV-outcome confounding) by saying something like, "the IV is not related to confounders." If we were more specific about which relationship is confounded when we talk about confounding, maybe that sort of confusion wouldn't crop up. 



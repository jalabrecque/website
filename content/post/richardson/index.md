---
layout: post
title: "Causal inference illusions: A review of a chapter 6 of Eugene Richardson's new book Epidemic Illusions"
date: 2020-08-11T01:13:14-05:00
published: false
---

First, I want to say there are a lot of good lessons for epidemiologists and global health researchers in Eugene Richardson's new book, [Epidemic Illusions](https://mitpress.mit.edu/books/epidemic-illusions) about the types of questions we should be asking. But one chapter where he entirely drops the ball is Redescription 6: Not-So-Big Data and Immodest Causal Inference. 

“If Big Data’s impending “monopoly on truth” described in the previous section represents the Scylla of public health’s future epistemic path, then the fetishization of causal inference is its Charybdis.” First, a note on Greek mythology. Scylla and Charybdis were sea monsters on each side of a strait where, to pass through, sailors were forced to face one danger or the other. We, fortunately, aren't required to choose between the two as Odysseus had to. And, in fact, I'd say (and I think almost everyone who works in causal inference would agree) the danger comes in the use of big data _without_ causal inference. I think Richardson would find that "fetishists" of causal inference are just as worried about the uncritical use of big data as he is. 

Richardson entirely botches a section on causal graphs. He starts by mentioning an example from Judea Pearl's book of a causal chain fire → smoke → alarm. If this is the true causal structure we can say P(alarm|smoke)=P(alarm|smoke,fire). In this case, the P(alarm|smoke) is independent of the P(fire). He follows this up with: “then for the example Maafa → Ebola virus (EBOV) transmission → Ebola virus illness (EVI), the Maafa is irrelevant to a West African’s suffering from Ebola virus illness, since a positive Ebola test tells us what caused the patient’s condition,” because P(EVI|EBOV)=P(EVI|EBOV,Maafa). This demonstrates to me that Richardson has zero idea what he's talking about and is criticizing causal inference entirely without understanding it. I'm sure he knows how frustrating it can be when people criticize something without any expertise in it whatsoever but maybe isn't self aware enough to see when he's doing the same. 

 He is right that the causal graph he draws implies that mathematical expression, _if we believe that causal graph is correct_. Nobody except Richardson himself is postulating this graph as a representation of reality! If he thinks Maafa has an independent effect on EVI then he can just draw another arrow directly from Maafa to EVI! . This is the nice thing about causal graphs. 

  He criticizes computer scientist Pearl for failing to know that smoke detectors also work by detecting heat in what is clearly a toy example. He concludes: "Yet if, as in the above example, a Turin Award laureate (Pearl) can omit a confounder in the simplest of causal chains, how can we trust more complex phenomena—like whether any of the Maafa’s legacies were component causes of the Ebola outbreak in West Africa—to “expert knowledge” First, Pearl omitted a _mediator_, not a confounder. 



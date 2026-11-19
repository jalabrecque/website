# The Association Road — story file

How this file works (everything above the first `## ` line is ignored by the page):

- Each scene starts with a line: `## id | type | column,row`
  - **id**: short name that choices point to. Don't rename one without updating the choices that lead to it.
  - **type**: mid (start/crossroads), gate, lesson (loops back), trap (bad ending), end (legitimate ending)
  - **column,row**: position on the map (column 0–10 left to right, row 0–7 top to bottom)
- The next line `### ...` is the scene title.
- Paragraphs are separated by a blank line. *Italic* and **bold** work.
- Choices are list items: `- [What the button says](id-it-leads-to)`
- The source line starts with `> Source:`
- Any text is fine, including apostrophes and quotation marks.


## start | mid | 0,3
### The manuscript

You have just written a paper which you are really excited about and would like to submit it to a high impact journal. The only thing you are worried about is that your research question is “to estimate the association between taking vitamin B supplements and dementia risk.” After spending an entire career avoiding causal language and using associational language instead, you've been hearing some people saying that associational language is not appropriate for a reesearch question! Imagine! Your methods describe how you chose covariates with a causal graph: age, sex, baseline cognition, APOE, education.

Your quest: keep the word “association” in the research question, and have it mean something you can defend.

- [Send the draft to your coauthor](purpose)

> Source: Labrecque & Kezios, BMJ 2026;392:e085749, Box 1

## purpose | mid | 1,3
### What is the answer for?

Your coauthor asks a simple question first: imagine the result is in. What action is it supposed to inform?

- [Tracking how dementia risk differs between users and non-users](desc1)
- [Deciding who should be screened for dementia](pred1)
- [Deciding whether people should take vitamin B](admit)
- [Nothing in particular. I just want the association.](which)

> Source: Labrecque & Kezios, “Why are we still using associational language in research questions?” (forthcoming, EJE)

## which | gate | 2,3
### Which association is “the” association?

There are many associations between supplement use and dementia: crude, adjusted for age and sex, adjusted for your five covariates, adjusted for some other set. Each is a different quantity to estimate, whether or not the numbers differ.

“The association” names none of them. Which one do you mean?

- [The crude one](crude)
- [The one adjusted for my five covariates](spec)
- [The one adjusted for confounders](confof)
- [Any of them; they are all “the association”](many)

> Source: BMJ 2026, “What associations are and how they arise”

## many | lesson | 2,2
### There are as many associations as analyses

Every set of adjustment variables defines a different statistical estimand. A research question that does not say which one it wants has not said what it wants.

- [Back to the gate](which)

> Source: BMJ 2026; CIIG talk, May 2026

## crude | gate | 2,4
### The crude comparison

A crude comparison of dementia risk in users and non-users is a perfectly good thing to want. It is a description.

But your methods adjust for five covariates chosen with a causal graph. Why?

- [Drop the adjustment. I only want the comparison.](desc1)
- [Keep adjusting, otherwise it is confounded](confof)

> Source: BMJ 2026, “Non-causal language in descriptive or predictive research questions”

## confof | lesson | 3,4
### Confounded relative to what?

Confounding is defined only once a causal estimand is defined: a confounder is a problem for an effect. Before you know which confounding to worry about, you need a question that can be confounded.

If you want to remove confounding, your goal is causal.

- [So my question is causal](admit)
- [I will name the covariates in the question instead](spec)

> Source: EJE commentary, Problem 1; talk “What is the causal effect?”, Oct 2026

## spec | gate | 3,3
### Can I just be more specific?

New objective: “the association between vitamin B use and dementia, adjusted for age, sex, baseline cognition, APOE and education.”

Your coauthor: your methods section explains how you chose these covariates. Why choose covariates that are already fixed by your question?

- [I wrote the question after choosing the covariates](ticket)
- [The covariates are part of the question by definition](nobias)

> Source: BMJ 2026, Issue 1: research questions should come before the methods

## ticket | lesson | 3,2
### A ticket to nowhere

The research question is the destination on a train ticket. The destination does not change if the train breaks down in the wrong city.

A question written after the analysis is the question you happened to answer, not the one you wanted to ask. The methods should follow the question, never the reverse.

- [Back to the gate](spec)

> Source: Labrecque, “Epidemiologic research questions are too often a ticket to nowhere”, AJE 2026

## nobias | gate | 4,3
### Biased away from what?

Your discussion warns that unmeasured confounding remains possible. But you adjusted for exactly the variables your question names. By construction, you estimated the association you asked about.

So what could your estimate be biased away from?

- [Delete the limitations paragraph](noLimits)
- [Biased away from the true effect of vitamin B](admit)

> Source: BMJ 2026, Issue 2: questions about associations make it difficult to talk about bias

## noLimits | gate | 5,3
### A consistent, empty paper

Now everything agrees: the estimate, the question, no bias. But your last paragraph still says vitamin B “may protect against dementia” and that a randomized trial is warranted.

- [Keep the conclusion; it is only tentative](dark)
- [Cut it too: “we report this adjusted association”](hollow)

> Source: Stolen causal inference (draft), definition of a causal claim

## hollow | gate | 6,3
### Why go to the trouble?

You selected covariates with a causal graph to block confounding, then interpreted the result as nothing at all. What can anyone use it for?

In a sample of articles from top epidemiology journals, 69% stated “seemingly causal” goals that fit no task cleanly.

- [It is hypothesis-generating: it tells us whether a trial is worthwhile](hypgen)
- [It describes something](desc1)
- [All right. It is causal.](admit)

> Source: Kezios, Epidemiol Rev 2021; Stolen causal inference (draft)

## hypgen | gate | 7,3
### Is an association evidence for a trial?

Suppose you knew an unmeasured confounder could explain the whole association. Then the association would be almost no evidence that vitamin B does anything.

An association counts as evidence for causation only to the extent that confounding, selection and measurement error are argued away: causal assumptions, made silently. The best evidence for a future trial is the best causal study you can do with the data you have.

- [Then I will say “association” and hint at causation](stolen)
- [Then I will do the best causal study I can](admit)

> Source: EJE commentary; CIIG talk, “Are associations evidence for causation?”

## dark | trap | 6,2
### Ending: dark causal inference

You never mentioned causation, yet your conclusion needs it. Like dark matter, the inference is detectable only by its pull on what we can see.

Checklist. Conclusion requires causal evidence: yes. Causal question: no. Causal assumptions: only confounding and selection mentioned. Arguments for them: no.

Epilogue: a guideline cites your paper. In one audit, 27% of diabetes-guideline statements used stronger causal language than the literature they cited.

- [Make the inference observable](admit)
- [Start over](start)

> Source: Labrecque & Wang, Dark causal inference (in prep.); Wang, Wei & Labrecque, BMJ Open 2026; Haber et al., AJE 2022 (60% make action recommendations)

## stolen | trap | 8,3
### Ending: stolen causal inference

Russell said postulating what we want has the advantages of theft over honest toil. A causal claim without a stated question, stated assumptions and arguments for them is stolen in the same way.

In 1928 a set of “new” Van Goghs fooled experts; the missing provenance gave them away. A causal estimate’s provenance is its question, its assumptions and the arguments behind them.

- [Do the honest toil](c1)
- [Start over](start)

> Source: Labrecque & Wang, Stolen causal inference (draft)

## admit | mid | 4,5
### The question was causal

You want to know what would happen to dementia risk if people took vitamin B. That is a causal question. You may still have objections.

- [Causal language claims more certainty than I have](humility)
- [My journal will not allow causal language](journal)
- [There must be an “associational” research task](table2)
- [No objections. Show me the causal road.](c1)

> Source: BMJ 2026, Fig 1

## humility | lesson | 3,6
### Two dimensions, not one

“Associational” and “causal” are often used as if they meant “uncertain” and “certain.” They are different axes: what you ask, and how sure you are of the answer. A causal question can end with a very uncertain answer, or with “we don’t know.”

If a question had to match the certainty of its answer, no trial could be called causal until its loss to follow-up was known. A question is what you want to know, not a promise of what you can deliver.

- [Fair. Back to my objections.](admit)
- [Show me the causal road](c1)

> Source: Labrecque, Separating research questions from uncertainty (draft); Petitti, AJE 1991; BMJ 2026

## journal | gate | 4,6
### The journal rule

Some journals reserve causal language for trials, and sometimes Mendelian randomization, even though MR is observational and rests on strong untestable assumptions. Vocabulary is being assigned by design, as a proxy for certainty.

- [I am a PhD student or early-career researcher](pragmatic)
- [I sit on an editorial board](editor)

> Source: Dahabreh & Bibbins-Domingo, JAMA 2024; Separating research questions from uncertainty (draft)

## pragmatic | end | 4,7
### Ending: play the game, do the work

This is not your battle to fight at the cost of your career. Design the study as a causal one, do the best causal analysis you can, and write it in the language the journal requires.

When you reach an editorial board, push for change.

- [Walk the causal road anyway](c1)
- [Start over](start)

> Source: “What is the causal effect?” talk, Oct 2026; CIIG talk, May 2026

## editor | end | 5,7
### Ending: the ball is in your court

There is no need for anyone to learn causal inference if they are not allowed to use causal language. Ask authors which association is “the” association. Require research questions that are clearly descriptive, predictive or causal.

- [Start over](start)

> Source: Harvard Epidemiology seminar; CIIG talk

## table2 | gate | 5,6
### Fill in the Association column

If association is its own research task, you should be able to define its estimand, estimator, assumptions, covariate selection rule and bias, and they must differ from description, prediction and causation. Start with the estimand.

- [Σₗ (E[Y|A=1,L=l] − E[Y|A=0,L=l]) Pr(L=l), with L the confounders](t2conf)
- [The same formula, with L the variables that define my comparison (e.g., age-standardised)](desc1)
- [Whatever predicts dementia best](pred1)
- [I cannot fill it in](t2conf)

> Source: EJE commentary, Table 2

## t2conf | lesson | 6,6
### The column fills itself in

If L is chosen to control confounding, you have written the causal column’s estimator. You then need consistency, positivity and exchangeability. If you can’t say which of those you need, there is no valid argument for an “associational” question.

The verdict so far: associations are not a fourth research task.

- [Back to my objections](admit)
- [Show me the causal road](c1)

> Source: EJE commentary; Journal club 2026

## desc1 | gate | 2,0
### A descriptive question

For example: “to describe the difference in five-year dementia risk between people who do and do not take vitamin B,” possibly age-standardised.

Check: is any adjustment variable there to remove a nuisance such as confounding?

- [Yes, to remove confounding](confof)
- [No, it is part of the comparison itself](desc2)

> Source: BMJ 2026; Fox et al., AJE 2022; Conroy & Murray, Br J Cancer 2020

## desc2 | gate | 3,0
### The discussion test

Will your discussion suggest mechanisms, say the difference is “explained by” something, or recommend action?

- [Yes: supplements may be protective](dark)
- [No: describe it, then stop](endDesc)

> Source: Stolen causal inference (draft)

## endDesc | end | 4,0
### Ending: a legitimate descriptive question

You found the one place association language is allowed: a descriptive comparison between groups. Even here the word is risky, because readers struggle to tell description from causation once adjustment appears.

The clearest version says describe, differences, distributions or trends, and uses descriptive methods.

- [Start over](start)

> Source: BMJ 2026, Fig 1; e.g., Ahmad et al., Ann Intern Med 2026 (hemoglobin and mortality by age and sex)

## pred1 | gate | 2,1
### A predictive question

“Does vitamin B use improve prediction of dementia beyond established predictors?” How will you choose covariates?

- [By their causal role, to avoid confounding](confof)
- [By predictive performance, with validation](pred2)

> Source: BMJ 2026; Steyerberg, Clinical Prediction Models

## pred2 | gate | 3,1
### The coefficient temptation

Your model gives vitamin B a protective-looking coefficient. Do you interpret it?

- [Yes: supplements protect](dark)
- [No: I report incremental discrimination and calibration](endPred)

> Source: BMJ 2026

## endPred | end | 4,1
### Ending: a legitimate predictive question

Legitimate, and it never needed the word association. Say predict, forecast, classify, discrimination. Predictors are chosen for performance, not for their causal role.

- [Start over](start)

> Source: BMJ 2026, Fig 1

## c1 | gate | 5,5
### 1. State the causal question

The five-year dementia risk if everyone took vitamin B, compared with if no one did: E[Yᵃ⁼¹] − E[Yᵃ⁼⁰]. Which intervention, exactly?

- [“Vitamin B use” is clear enough](cons)
- [Daily B12 and folate from age 65 for five years, versus none](c2)

> Source: Hernán & Robins, What If; Petersen & van der Laan 2014 (Roadmap)

## cons | lesson | 5,4
### The forgotten assumption

Without a well-defined intervention, consistency is unclear. Among papers using g-methods in top epidemiology journals, only 42% mentioned consistency; in an ICU review, 11%.

- [Back](c1)

> Source: Eisenberg-Guyot et al., IJE 2025; Smit et al., npj Digit Med 2023

## c2 | gate | 6,5
### 2. State every assumption

Your identification argument has to take you from the causal estimand all the way to a function of observed data.

- [No unmeasured confounding](invalid)
- [Consistency, positivity, conditional exchangeability, no measurement error, correct model](c3)

> Source: Harvard seminar, “Causal assumptions”

## invalid | lesson | 7,4
### An invalid argument

All humans are mortal; Socrates is human; so Socrates is mortal. Drop the second premise and the conclusion no longer follows: a stolen deduction.

Mentioned in top-journal papers using causal methods: exchangeability 92%, positivity 45%, consistency 42%.

- [Back](c2)

> Source: Harvard seminar; Eisenberg-Guyot et al., IJE 2025

## c3 | gate | 7,5
### 3. Argue for the assumptions

A valid argument is not a sound one. This step is by far the hardest part of causal inference, and the most ignored. How do you support exchangeability?

- [“We adjusted for known confounders; residual confounding is possible”](partial)
- [We assume they hold](stolen)
- [Causal graph from subject knowledge, negative controls, bias analysis, triangulation](c4)

> Source: Causal inference is not sufficient to infer causation (outline); Harvard seminar

## partial | lesson | 7,6
### Consistent with anything

“RR 1.15 (1.04–1.27); unmeasured confounding remains possible.” Without more, those two statements are consistent with any RR from zero to infinity.

The authors know the data best. If they cannot bound the bias, who can?

- [Back](c3)

> Source: CIIG talk (loneliness and CVD); Harvard seminar (coffee and mortality)

## c4 | gate | 8,5
### 4. Use each word for what it means

Causal effect: the true, unknowable quantity (introduction, estimand, what bias is measured from). Association: the number the estimator returns (results). Estimated causal effect: that number read through the assumptions, with a critical look at how violations would bias it (discussion).

- [Write the conclusion](c5)

> Source: BMJ 2026, Table 1

## c5 | gate | 9,5
### 5. The conclusion

What do you conclude?

- [Vitamin B prevents dementia](over)
- [A nuanced sentence on how much causal evidence this study adds; it could be a lot, or none](endCausal)

> Source: “What is the causal effect?” talk, Oct 2026

## over | lesson | 9,6
### Asking is not answering

Asking a causal question does not make your answer more causal. Only stronger arguments for the assumptions can do that.

- [Back](c5)

> Source: BMJ 2026, “Asking a causal question does not mean the estimate will be causal”

## endCausal | end | 10,5
### Ending: honest toil

You set out to keep “association” in your question and discovered that the question was causal all along. Saying so cost you nothing: your answer can still be “we don’t know.”

What it gained you: a destination, a list of premises and a reason to argue for them. Causal inference tells you which premises you need; inferring causation means showing they hold.

- [Start over](start)

> Source: BMJ 2026; Causal inference is not sufficient to infer causation (outline)

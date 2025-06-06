---
title: "Essentials"
summary: EL018
output:
  html_document:
    keep_md: true
    toc: true
    toc_float: true
    css: style.css

---

# Day 2

## Morning (9am-12:30pm): The crucial difference between associations and causation


- 9-10: What is an association? Is it a good research question?
  - [Let's look at the word association in the wild.](https://docs.google.com/forms/d/e/1FAIpQLSeCroltgJ04wRpkZnw3-KeC0q2TDLk9HQqprr3kz36HF72oGQ/viewform?pli=1)
  - What is an association?
- 10-11: Causal inference
  - Gaining intuition for causal questions
  - 



Important points

-   We use the word association in research questions for historical reasons, not for good reasons.
-   It is not clear which association is 'the' association when people ask the question: "what is the association between X and Y". And, in fact, there's no way to be clear about which association is 'the' association.
-   There are 3 types of questions in health research:
    -   Descriptive: what is the state of the world?
    -   Predictive: can I take a guess at something I don't know using data?
    -   Causal: how would the world change if I intervened on it?

## Afternoon: How to know what to adjust for

Important points:

-   Directed acyclic graphs (DAGs) have two components:
    -   Variables: these are nodes that represent the variables related to your causal research question
    -   Arrows: these demonstrate the flow of causation from one variable to another (sometimes also called edges)
-   Directed acyclic graphs :
    -   **Directed**: the arrows must have only one arrow head. Undirected arrows don't give us the information we need and double-headed arrows violate the laws of physics
    -   **Acyclic**: there cannot be cycles in the DAG. In other words, there can be place on the graph where you can start at one variable, follow a path along the direction of the arrows, and arrive back at the same variable.
    -   **Graph**: DAGs use graph theory. But fortunately, by learning the simple rules, you don't have to.
- 




# Day 2, morning

### Questions before answers

- Kaufman and Hernan 2012. [Epidemiologic Methods Are Useless They Can Only Give You Answers](https://journals.lww.com/epidem/Fulltext/2012/11000/Commentary___Epidemiologic_Methods_Are_UselessThey.3.aspx)
- Vanderbroucke and Pearce 2018. [From ideas to studies: how to get ideas and sharpen them into research questions](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5846748/)
- Yanai and Lercher 2019. [What is the question?](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1902-1)
- Snowden, Reavis and Odden 2020 [Conceiving of Questions Before Delivering Analyses](https://pubmed.ncbi.nlm.nih.gov/32501813/)
- Hernan and Robins 2016. [Using Big Data to Emulate a Target Trial When a Randomized Trial Is Not Available](https://pubmed.ncbi.nlm.nih.gov/26994063/)
- [Questions before answers (blog post)](https://www.jeremylabrecque.org/post/questions_before_answers)

### Causal inference

- Hernan and Robins 2020. [Causal Inference: What If?](https://www.hsph.harvard.edu/miguel-hernan/wp-content/uploads/sites/1268/2024/01/hernanrobins_WhatIf_2jan24.pdf)
- Robins 2001. [Data, Design, and Bakground Knowledge in Etiologic Inference](https://pubmed.ncbi.nlm.nih.gov/11338312/)
- Maldonado and Greenland 2002. [Estimating Causal Effects](https://academic.oup.com/ije/article/31/2/422/2951425)

### Causal assumptions

- Labrecque and Swanson 2018. [Understanding the Assumptions Underlying Instrumental Variable Analyses: a Brief Review of Falsification Strategies and Related Tools](https://pubmed.ncbi.nlm.nih.gov/30148040/)
- Labrecque 2024. [A Whirlwind Tour of Causal Assumptions](files/whirlwind.pdf)
- Matthay et al 2020. [Alternative causal inference methods in population health research: Evaluating tradeoffs and triangulating evidence](https://pubmed.ncbi.nlm.nih.gov/31890846/)


# Day 2, afternoon


# Exercise

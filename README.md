# Examining the effects of Facebook ad campaigns on Covid-19 vaccine uptake

## Project description

I seek to assess the effectiveness of different Facebook advertisement campaigns in promoting Covid-19 vaccine uptake. Specifically, I am interested in how the presence of advertisements itself affects vaccine uptake, and also the differential effects of advertisement strategies appealing to logic and to emotion on uptake. Prior to running the actual field experiment, I run a simulated version with Large Language Model (LLM) agents to sense-check the experimental design and obtain an initial idea of the data collected and effect sizes.

This simulated experiment mimics the field experiment, which will sample 5000 individuals living across the US. Participants will answer a baseline survey, then be exposed to their respective treatments, and finally answer an endline survey. There are three treatment groups over which the sample will be randomly assigned to in equal proportions: one which is exposed to no ads (`control`), one which is exposed to ads appealing to reason (`logos`), and one which is exposed to ads appealing to emotions (`pathos`).

At the start of the experiment, participants will indicate their demographic characteristics (gender, race, age, household income, education level, state of residence), usage frequency of social media (including Facebook), and willingness to take the updated 2024-2025 Covid-19 vaccine, and Facebook account identifiers for treatment implementation (de-identified and encoded as unique strings of five numbers in the data set). The treatment groups will be randomly assigned blocking on these covariate data. After a month, over which the ad campaigns will be rolled out, the participants will be invited to take the endline survey asking about their willingness to take the Covid-19 vaccine, and their perceptions of the ad campaigns if they were exposed. Both surveys will be incentivised, with incentives backloaded to reduce attrition. The effects of the ad campaigns on vaccine uptake can then be recovered via a differences-in-differences method.

For this simulation, I also assume that a 10% attrition rate, so out of the 5000 participants who completed the baseline survey and were assigned to treatment, only 4500 subjects complete the endline survey. I assume complete compliance with treatment assignment i.e. no errors in the ad campaign administration to each participant's Facebook account. I also assume no spillover effects, which may or may not be a reasonable assumption in reality depending on the social networks of the participants (they can communicate the ads across groups through likes, shares, or word-of-mouth), though the reasonability of this assumption can be strengthened by restricting the level of social connection across participants in different groups (e.g. not Facebook friends).

After obtaining the simulated experimental data, I analyze it by first verifying internal validity given attrition, then checking for average effects of ad campaign versus no ad campaign on vaccine uptake, and finally for differential effects between the two ad campaign strategies.

## Repository structure

* ads-vaccine-simulation.ipynb: data simulation of experiment using Python code in Jupyter notebook
* ads-vaccine-analysis-manuscript.qmd: analysis of simulated data using R in Quarto document
* ads-vaccine-analysis-manuscript.pdf: analysis report (with code output but not source)
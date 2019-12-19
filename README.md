# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

## Table of Contents
- [Executive Summary](#Executive-Summary)
- [Introduction](#Introduction)
- [Overview](#Overview)
- [Datasets](#Datasets)

--- 

### Executive Summary

An analysis of the SAT and ACT examinations' scores and participation rates in 2017 and 2018, since the new format for the SAT was released in March 2016, and further research were performed. It was done with the goal of advising the College Board on possible measures that would boost the participation rates of the SAT in North Dakota. 

The datasets provided consisted of each test's average total score, section scores, and participation rate for each of the U.S. states in the years 2017 and 2018.  

The analysis of each variable showed that most features of the dataset were not normally distributed and right-skewed. Also, most of the variables' distributions seem to be multi-modal, which implies that there may be multiple groups within the population.

Pairwise analysis of variables revealed that there are moderate to strong negative correlations between participation rates and each of the respective test's scores for both the SAT and ACT in both year 2017 and 2018. Further investigation revealed that states with the highest participation rates do not necessarily have the highest average total score. In fact, such states may have the lowest average total score. Further research showed that these states often mandate either test and even pay for the test, which led me to believe that such state policies and sponsorship may be the likely cause for high participation rates and also lower scores as less academically inclined high-schoolers are required to take the test and therefore may lower the mean scores of these states.

Given that the participation rates are highest in states where the SAT is mandatory and paid for, the College Board could lobby for instance, the state government of North Dakota, which has the lowest SAT participation rates for both years and does not mandate either the ACT or SAT nor pays for either tests, to adopt the SAT as the state's compulsory examination for high-schoolers and perhaps even sponsor the test.

---

### Introduction

This project is an analysis of the SAT and ACT examinations in both year 2017 and 2018, after the new format for the SAT was released in March 2016. It studies and identifies trends in the aggregate SAT and ACT scores and participation rates from each state in the United States, and synthesizes information from outside research with the data analysis. In so doing, it aims to identify likely factors driving participation rates for both tests, so that suggestions can be made to the College Board to boost SAT participation rates in North Dakota. 

---

### Overview

The pipeline:
- Data Cleaning
- Exploratory Data Analysis
- Data Visualization
- Descriptive and Inferential Statistics
- Outside Research
- Conclusions and Recommendations

---

### Datasets

#### Provided Data

For this project, there are four datasets provided:

- [2017 SAT Scores](./data/sat_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 ACT Scores](./data/act_2018.csv)

These data give average SAT and ACT scores by state, as well as participation rates, for the graduating class of 2017 and for that of 2018.

You can see the source for the 2017 SAT data [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/), and the source for the 2017 ACT data [here](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/ACT_2017-Average_Scores_by_State.pdf). 

2018 state-by-state average results and participation for the SAT are available in PDF reports [here](https://reports.collegeboard.org/sat-suite-program-results/state-results). 2018 ACT state-by-state mean composite scores and participation rates are [here](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf).
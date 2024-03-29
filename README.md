# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

## Table of Contents
- [Executive Summary](#Executive-Summary)
- [Introduction](#Introduction)
- [Problem Statement](#Problem-Statement)
- [Overview](#Overview)
- [Datasets](#Datasets)
- [Conclusion and Recommendations](#Conclusion-and-Recommendations)

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

### Problem Statement

To boost participation rates in the SAT examination for the state of North Dakota

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

#### Data Dictionary

|Feature|Type|Dataset|Description|
|:---|:---|:---|:---|
|**state**|*category*|act_2017, act_2018, sat_2017, sat_2018, combined_2017, combined_2018, final|One of the states in America|
|**act_participation_2017**|*float*|act_2017, combined_2017, final|Participation rate (real number from 0 to 1 in two decimal places, i.e. ℝ ∈ [0,1])|
|**act_english_2017**|*float*|act_2017, combined_2017, final|Score for the ACT's English section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36])|
|**act_math_2017**|*float*|act_2017, combined_2017, final|Score for the ACT's Math section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**act_reading_2017**|*float*|act_2017, combined_2017, final|Score for the ACT's Reading section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**act_science_2017**|*float*|act_2017, combined_2017, final|Score for the ACT's Science section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**act_composite_2017**|*float*|act_2017, combined_2017, final|Score for the ACT's Composite section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**sat_participation_2017**|*float*|sat_2017, combined_2017, final|Participation rate (real number from 0 to 1 in two decimal places, i.e. ℝ ∈ [0,1]) |
|**sat_ebrw_2017**|*int*|sat_2017, combined_2017, final|Score for the SAT's Evidence-Based Reading and Writing section (real number from 1 to 36 in two decimal places, i.e. ℤ ∈ [200,800]) |
|**sat_math_2017**|*int*|sat_2017, combined_2017, final|Score for the SAT's Math section (real number from 1 to 36 in two decimal places, i.e. ℤ ∈ [200,800]) |
|**sat_total_2017**|*int*|sat_2017, combined_2017, final|Score for the SAT's Total (real number from 1 to 36 in two decimal places, i.e. ℤ ∈ [400,1600]) |
|**act_participation_2018**|*float*|act_2018, combined_2018, final|Participation rate (real number from 0 to 1 in two decimal places, i.e. ℝ ∈ [0,1])|
|**act_english_2018**|*float*|act_2018, combined_2018, final|Score for the ACT's English section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36])|
|**act_math_2018**|*float*|act_2018, combined_2018, final|Score for the ACT's Math section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**act_reading_2018**|*float*|act_2018, combined_2018, final|Score for the ACT's Reading section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**act_science_2018**|*float*|act_2018, combined_2018, final|Score for the ACT's Science section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**act_composite_2018**|*float*|act_2018, combined_2018, final|Score for the ACT's Composite section (real number from 1 to 36 in two decimal places, i.e. ℝ ∈ [1,36]) |
|**sat_participation_2018**|*float*|sat_2018, combined_2018, final|Participation rate (real number from 0 to 1 in two decimal places, i.e. ℝ ∈ [0,1]) |
|**sat_ebrw_2018**|*int*|sat_2018, combined_2018, final|Score for the SAT's Evidence-Based Reading and Writing section (real number from 1 to 36 in two decimal places, i.e. ℤ ∈ [200,800]) |
|**sat_math_2018**|*int*|sat_2018, combined_2018, final|Score for the SAT's Math section (real number from 1 to 36 in two decimal places, i.e. ℤ ∈ [200,800]) |
|**sat_total_2018**|*int*|sat_2018, combined_2018, final|Score for the SAT's Total (real number from 1 to 36 in two decimal places, i.e. ℤ ∈ [400,1600]) |

### Conclusion and Recommendations

Although the participation rates of either test are negatively correlated with each of the scores of the respective test's section, it does not suggest a causal relationship between these pairs of variables, specifically, reducing the scores by making the test more difficult for example would not necessarily result in an increase in the participation rates.

Given that the participation rates are highest in states where the SAT is mandatory and paid for, the College Board could lobby the state government of North Dakota, which has the lowest SAT participation rates for both years and does not mandate either the ACT or SAT nor pays for either tests, to adopt the SAT as the state's compulsory examination for high-schoolers and perhaps even sponsor the test.

Additional data such as the universities within each state and the ranking of the universities throughout the U.S. might provide additional insight into the participation rate of either test as there may be individuals who take one test over the other with the intention of entering his/her desired college which may require either the SAT or the ACT.
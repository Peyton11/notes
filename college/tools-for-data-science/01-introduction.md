# Math:300 Tools for Data Science Introduction

## Statistical Learning vs. Machine Learning

- ML arose as a subfield of AI.
- SL arose as a subfield of statistics.
- *There is much overlap*- both fields focus on supervised and unsupervised problems:
    - ML has a greater emphasis on *large scale* applications and *prediction accuracy*.
    - SL emphasizes *models* and their interpretability, and *precision* and *uncertainty*.
- But the distinction has become more and more blurred, and there is a great deal of "cross-fertilization".
- ML has the upper hand in *marketing!*

## Philosophy

- It is important to understand the ideas behind the various techniques, in order to know how and when to use them. 
- One has to understand the simpler methods first, in order to grasp the more sophisticated ones. 
- It is important to accurately assess the performance of a method, to know how well or how badly it is working (simpler methods often perform as well as fancier ones!)
- This is a prominent research area, especially in science, industry, and finance. 
- SL is a fundamental ingredient in the training of a modern *data scientist*. 

## The Supervised Learning Problem

Starting point:  

- Outcome measurement Y (also called dependent variable, response, target).
- Vector of p predictor measurements X (also called inputs, regressors, covariates, features, independent variables).
- In the *regression problem*, Y is quantitative (e.g. price, blood pressure).
- In the *classification problem*, Y takes values in a finite, unordered set (survived/died, digit 0-9, cancer class of tissue sample). 
- We have training data $(x_{1}, y_{1})$, ..., $(x_{N}, y_{N})$. These are observations (examples, instances) of these measurements. 

### Objectives

On the basis of training data we would like to:  

- Accurately predict unseen test cases.
- Understand which inputs affect the outcome, and how. 
- Assess the quality of our predictions and inferences.

## Unsupervised Learning

- No outcome variable, just a set of predictors (features) measured on a set of samples.
- Objective is more fuzzy - find groups of samples that behave similarly,  find features that behave similarly. Find linear combinations of features with the most variation. 
- Difficult to know how well you are doing.
- Different from supervised learning, but can be useful as a pre-processing step for supervised learning. 

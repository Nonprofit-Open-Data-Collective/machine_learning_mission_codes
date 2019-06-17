---
layout: home
title: Methods
---

## Creating Machine Learning Classifiers for Nonprofit Mission Statements


Having clear taxonomies or categorical variables that describe nonprofit program activities makes many forms of data more theoretically meaningful and practially useful. They can be used to organize grants, examine collective impact from a set of programs, or find nonprofits with similar purposes. 

This is a set of replication files and vignettes that demonstrate the task of using mission and program service accomplishment text from admistrative tax forms to predict mission activity codes such as the NTEE.

Creating accurate classifier models that are trained on large, readily available archives allow for the models to be used with custom text repositories such as grant data, reports, social media text, etc. 

The goal of this project is to provide a robust set of test data, a reasonable set of text pre-processing steps, and examples of useful classifiers to lower the entry barriers for others that would like to engage with the work and offer some benchmarks for performance. 

As such, we are following an open science model where all data and code used to produce this analysis is accessible and extensible through Creative Commons licensing. 

------------------------

# The Training Dataset

Description of training dataset:

* Nonprofit names
* Mission fields 
* Program service accomplishment fields 
* Taxonomies: NTEE and IRS Purpose Codes
* Comparison to a subset of ICR from 100 human-coded missions

---------------------------

# Replication Files

**Preprocessing Text Data** 

* [Preprocessing Steps](tutorials/Preprocessing.html)
* [Nice Feature Engineering overview](https://youtu.be/9rBc3rTsJsY)  


**Text Analysis Approaches**

* [Semantic Network Analysis](tutorials/semantic_networks.html)  

**Supervised Learning Approaches**  

* [Naive Bayes Classifiers](tutorials/Naive_Bayes.html)
* [Classification Trees](tutorials/Classification_Trees.html)

For reference on some methods mentioned here, try this [nice blog on machine learning](https://vas3k.com/blog/machine_learning/).

-------------------------

## Accuracy

These results are mean to provide a baseline level of performance only. They are preliminary results from a draft white paper on this topic (Lecy, Van Holm & Santamarina 2019). See the replication files above. 


**Accuracy:** Preliminary results using naive bayes classifiers in the `quanteda` package in R on a sample training dataset. Overall accuracy is high, but that is common when a small portion of the sample belongs to the code category (e.g. a small number of cancer tests come back positive, so they are highly accurate but fairly useless if all tests just predict no cancer). See the [model assessment](https://nonprofit-open-data-collective.github.io/machine_learning_mission_codes/accuracy/) tab for more details. 

Sensitivity tells us how often we are able to correctly identify the codes (true positives in model / all positives in sample).

Specificity tells us how often we misclassify cases that do not belong to the code (true negatives in model / all negatives in sample)

**Charitable Purpose Codes from 1023 Forms**
 
| Schema             | Code       | Accuracy | Sensitivity | Specificity |  
|--------------------|------------|----------|-------------|-------------|  
| Tax Exempt Purpose | Charity    | 0.84     | 0.65        | 0.87        |  
| Tax Exempt Purpose | Religious  | 0.92     | 0.94        | 0.76        | 
| Tax Exempt Purpose | Edu        | 0.75     | 0.77        | 0.72        | 
| Tax Exempt Purpose | Scientific | 0.93     | 0.95        | 0.54        | 
| Tax Exempt Purpose | Literary   | 0.96     | 0.97        | 0.41        | 
| Tax Exempt Purpose | Safety     | 0.99     | 0.99        | 0.15        | 
| Tax Exempt Purpose | Sports     | 0.96     | 0.98        | 0.65        | 
| Tax Exempt Purpose | Cruelty    | 0.96     | 0.98        | 0.66        | 

<br>

**Binarized NTEE Codes from Business Master Files**

| Schema             | Code       | Accuracy | Sensitivity | Specificity |  
|--------------------|------------|----------|-------------|-------------| 
| NTEE Major Group   | Art        | 0.95     | 0.97        | 0.75        | 
| NTEE Major Group   | Ed         | 0.91     | 0.94        | 0.67        | 
| NTEE Major Group   | Env        | 0.97     | 0.99        | 0.83        | 
| NTEE Major Group   | Health     | 0.94     | 0.96        | 0.73        | 
| NTEE Major Group   | Human      | 0.82     | 0.86        | 0.75        | 
| NTEE Major Group   | Intern.    | 0.98     | 0.98        | 0.22        | 
| NTEE Major Group   | Public     | 0.87     | 0.91        | 0.58        | 
| NTEE Major Group   | Religion   | 0.95     | 0.97        | 0.72        | 
| NTEE Major Group   | Mutual     | 1.00     | 1.00        | 0.29        | 
| NTEE Major Group   | Unknown    | 0.99     | 1.00        | 0.57        |  
|--------------------|------------|----------|-------------|-------------|  


<br><br>



**Humans vs. Machines:** Comparing human inter-coder reliability to the predictive accuracy of a machine learning approach (naive bayes supervised learning in the `quanteda` package in R).

<br>


| Schema                        | Code       | ICR  | ML Accuracy | 
|-------------------------------|------------|------|-------------| 
| Tax Exempt Purpose            | Charity    | 0.79 | 0.84        | 
| Tax Exempt Purpose            | Religious  | 0.97 | 0.92        | 
| Tax Exempt Purpose            | Education  | 0.81 | 0.75        | 
| Tax Exempt Purpose            | Scientific | 0.99 | 0.93        | 
| Tax Exempt Purpose            | Literary   | 0.98 | 0.96        | 
| Tax Exempt Purpose            | Safety     | 1.00 | 0.99        | 
| Tax Exempt Purpose            | Sports     | 0.96 | 0.96        | 
| Tax Exempt Purpose            | Cruelty    | 0.98 | 0.96        | 
|-------------------------------|------------|------|-------------| 
| **Custom**                    |  Serves Vulnerable Populations   | 0.87 | -           | 
|-------------------------------|------------|------|-------------| 






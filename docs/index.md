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

Description of training dataset...

* Nonprofit names
* Mission fields 
* Program service accomplishment fields 
* Taxonomies: NTEE and IRS Purpose Codes
  * Subset of human-coded activity codes for reliability

---------------------------

# Replication Files

**Preprocessing Text Data** 

* [Preprocessing Steps](tutorials/Preprocessing.html) 


**Text Analysis Approaches**

* [Semantic Network Analysis](tutorials/semantic_networks.html)  

**Supervised Learning Approaches**  

* [Naive Bayes Classifiers](tutorials/Naive_Bayes.html)
* [Classification Trees](tutorials/Classification_Trees.html)
* Support Vector Machines



-------------------------

## Accuracy

These results are mean to provide a baseline level of performance only. They are preliminary results from a draft white paper on this topic (Lecy, Van Holm & Santamarina 2019). See the replication files above. 


 
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
|--------------------|------------|----------|-------------|-------------| 
| NTEE               | Art        | 0.95     | 0.97        | 0.75        | 
| NTEE               | Ed         | 0.91     | 0.94        | 0.67        | 
| NTEE               | Env        | 0.97     | 0.99        | 0.83        | 
| NTEE               | Health     | 0.94     | 0.96        | 0.73        | 
| NTEE               | Human      | 0.82     | 0.86        | 0.75        | 
| NTEE               | Intern.    | 0.98     | 0.98        | 0.22        | 
| NTEE               | Public     | 0.87     | 0.91        | 0.58        | 
| NTEE               | Religion   | 0.95     | 0.97        | 0.72        | 
| NTEE               | Mutual     | 1.00     | 1.00        | 0.29        | 
| NTEE               | Unknown    | 0.99     | 1.00        | 0.57        |  
|--------------------|------------|----------|-------------|-------------|  
| Schema             | Code       | Accuracy | Sensitivity | Specificity |  
 





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
| Serves Vulnerable Populations |            | 0.87 | -           | 
|-------------------------------|------------|------|-------------| 






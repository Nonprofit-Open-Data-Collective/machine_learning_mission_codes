---
layout: home
title: Methods
---

## Creating Machine Learning Classifiers for Nonprofit Mission Statements


<img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHRpdGxlPlNrZXRjaDwvdGl0bGU+PHBvbHlnb24gcG9pbnRzPSI1LjI0IDIuMjEgMTIgMS41MiAxOC43NyAyLjIxIDI0IDguOTkzIDEyIDIyLjQ4IDAgOC45OTMgNS4yNCAyLjIxIiBmaWxsPSIjZmNiMjAwIi8+PHBvbHlnb24gcG9pbnRzPSI0Ljg2IDguOTkzIDEyIDIyLjQ4IDAgOC45OTMgNC44NiA4Ljk5MyIgZmlsbD0iI2U5NmMwMCIvPjxwb2x5Z29uIHBvaW50cz0iMTkuMTQgOC45OTMgMTIgMjIuNDggMjQgOC45OTMgMTkuMTQgOC45OTMiIGZpbGw9IiNlOTZjMDAiLz48cG9seWdvbiBwb2ludHM9IjQuODYgOC45OTMgMTkuMTQgOC45OTMgMTIgMjIuNDggNC44NiA4Ljk5MyIgZmlsbD0iI2ZjYWMwMCIvPjxwb2x5Z29uIHBvaW50cz0iMTIgMS41MiA1LjI0IDIuMjEgNC44NiA4Ljk5MyAxMiAxLjUyIiBmaWxsPSIjZmNkMTMxIi8+PHBvbHlnb24gcG9pbnRzPSIxMiAxLjUyIDE4Ljc3IDIuMjEgMTkuMTQgOC45OTMgMTIgMS41MiIgZmlsbD0iI2ZjZDEzMSIvPjxwb2x5Z29uIHBvaW50cz0iMjQgOC45OTMgMTguNzcgMi4yMSAxOS4xNCA4Ljk5MyAyNCA4Ljk5MyIgZmlsbD0iI2ZjYWMwMCIvPjxwb2x5Z29uIHBvaW50cz0iMCA4Ljk5MyA1LjI0IDIuMjEgNC44NiA4Ljk5MyAwIDguOTkzIiBmaWxsPSIjZmNhYzAwIi8+PHBvbHlnb24gcG9pbnRzPSIxMiAxLjUyIDQuODYgOC45OTMgMTkuMTQgOC45OTMgMTIgMS41MiIgZmlsbD0iI2ZkZWRiNiIvPjxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==" alt="Sketch" title="Sketch" width="20" height="20">

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

These examples are mean to provide a baseline level of performance only. 

We have achieved the following success...



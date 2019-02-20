---
layout: page
title: Model Assessment
---


Machine learning approaches to data analysis are often predictive models, not regression models or causal frameworks common in many social sciences. Model fit is assessed by predictive performance rather than statistical significance. We have included this information as a quick reference for those interested in understanding how to interpret output that is common to many supervised learning algorithms. 

--------------------

## Model Fit

![](../assets/images/four-outcomes-of-classifier.png)  


**THE CONFUSION MATRIX**

```
                              Predicted Group
Actual Group               YES                NO   
         YES    TRUE Positives   FALSE Negatives
          NO   FALSE Positives    TRUE Negatives
```

The confusion matrix organizes the results into a table where the actual classes are represented by row values, and the predicted classes are represented by column values. It is a compact way to represent information regarding algorithm performance. 


<br>

--------------------

## Common Metrics  

Takaya Saito and Marc Rehmsmeier have developed a great website explaining some commmon fit metrics that we present here [WEBSITE](https://classeval.wordpress.com/introduction/basic-evaluation-measures/). 



![](../assets/images/sensitivity.png)  

Sensitivity or Recall is the number of True Positives divided by the number of True Positives and the number of False Negatives. Put another way it is the number of positive predictions divided by the number of positive class values in the test data. It is also called the True Positive Rate. Sensitivity can be thought of as a measure of a classifiers completeness. A low recall indicates many False Negatives.

![](../assets/images/false-positive-rate.png)  

False positive rate (FPR) is calculated as the number of incorrect positive predictions divided by the total number of negatives. The best false positive rate is 0.0 whereas the worst is 1.0. 


![](../assets/images/specificity.png)  

Specificity (SP) is calculated as the number of correct negative predictions divided by the total number of negatives. It is also called true negative rate (TNR). 

![](../assets/images/precision.png)  

Precision is True Positives divided by the number of True Positives and False Positives. Put another way, it is the number of positive predictions divided by the total number of positive class values predicted.



The F1 Score is the 2 * (precision*recall) / (precision+recall) . It is also called the F Score or the F Measure. Put another way, the F1 score conveys the balance between the precision and the recall. [cite](https://machinelearningmastery.com/classification-accuracy-is-not-enough-more-performance-measures-you-can-use/)


--------



| METRIC                 |  FORMULA                     |
|------------------------|------------------------------|
|  Sensitivity           | ![](../assets/images/sens.png)  |
|  Specificity           | ![](../assets/images/spec.png)  |
|  Precision             | ![](../assets/images/prec.png)  |
|  Recall                | ![](../assets/images/sens.png)  |
|  F1                    | ![](../assets/images/f1.png)  |
|  Accuracy              | ![](../assets/images/acc.png)   |
|  Error                 | ![](../assets/images/err.png)   |


<br>

----------------------------


## Sample R Output

```
## Confusion Matrix and Statistics
##
##                 predicted_class
## actual_class       0       1
##            0   0.827   0.041
##            1   0.059   0.071
##
## Sensitivity : 0.933
## Specificity : 0.630
## Pos Pred Value : 0.952
## Neg Pred Value : 0.545
## Precision : 0.952
## Recall : 0.933
## F1 : 0.942
## Prevalence : 0.887
## Detection Rate : 0.827
## Detection Prevalence : 0.869
## Balanced Accuracy : 0.781
```










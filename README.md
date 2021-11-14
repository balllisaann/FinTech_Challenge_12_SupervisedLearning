# FinTech_Challenge_12_SupervisedLearning

Author: Lisa Bailey (balllisaann@yahoo.com)

Date: 11/7/2021

### Purpose

The purpose of this analysis is to classify whether loan borrowers are likely to default on a loan or are a save lending investment.  

## Overview of the Analysis

Logistic regression was used to attemp to classify clients to see if they are likely to default on a loan or not.  Two models were built: one on the original unscaled data and the other model used the Randome Oversampling technique due to the data being very imbalanced.  
In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

An **abusurdly** simple Logisitc Regression model was used to analyze the data.  
* We were not prompted to see if there were any missing values (there were not).
* We were not prompted to see if there was any categorical or ordinal data that needed to be encoded (there was only numeric data).
* We were not promped to **scale** the data.
* We were never even taught about **feature/variable reduction**
* We were never taught to check for basic assumptions for Logistic Regression, like there should be at least 50 test data points per feature/variable.

### Data used 

The data used was loan data with the following characteristics:

```Shape: (77536, 8)```

```
Loan Status: 
0 (Healthy loans): 75036
1 (Unhealthy loans): 2500
```

```
          loan_size  interest_rate  borrower_income  debt_to_income  
count  77536.000000   77536.000000     77536.000000    77536.000000   
mean    9805.562577       7.292333     49221.949804        0.377318   
std     2093.223153       0.889495      8371.635077        0.081519   
min     5000.000000       5.250000     30000.000000        0.000000   
25%     8700.000000       6.825000     44800.000000        0.330357   
50%     9500.000000       7.172000     48100.000000        0.376299   
75%    10400.000000       7.528000     51400.000000        0.416342   
max    23800.000000      13.235000    105200.000000        0.714829   

       num_of_accounts  derogatory_marks    total_debt   loan_status  
count     77536.000000      77536.000000  77536.000000  77536.000000  
mean          3.826610          0.392308  19221.949804      0.032243  
std           1.904426          0.582086   8371.635077      0.176646  
min           0.000000          0.000000      0.000000      0.000000  
25%           3.000000          0.000000  14800.000000      0.000000  
50%           4.000000          0.000000  18100.000000      0.000000  
75%           4.000000          1.000000  21400.000000      0.000000  
max          16.000000          3.000000  75200.000000      1.000000  
```

## Results

### Machine Learning Model 1 (unscaled logistic regression on original data):

  * Accuracy: 95%
  * Confusion Matrix:
     ```
     [18663,   102],
     [   56,   563]
     ```
       
  * Description of Model 1 Accuracy, Precision, and Recall scores.
 ```
          pre       rec       spe        f1       geo       iba       sup
          0       1.00      0.99      0.91      1.00      0.95      0.91     18765
          1       0.85      0.91      0.99      0.88      0.95      0.90       619
 avg / total      0.99      0.99      0.91      0.99      0.95      0.91     19384
 ```

### Machine Learning Model 2 (unscaled logistic regression with random oversampling):

  * Accuracy: 99%
  * Confusion Matrix:
     ```
      [18649,   116],
      [    4,   615]
    ```
* Description of Model 2 Accuracy, Precision, and Recall scores.
```
                   pre       rec       spe        f1       geo       iba       sup
          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619
avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384
```

## Summary

**Answer:** 

The logistic regression model does fairly well with the original data set.  There is a 95% overall accuracy.  However, there is a recall score of 91%, meaning that approximately 9% of loans are being classified as healthy, when in fact, they default.  Yikes!  I would not want to make investments in loads where 9% of the loans that are going to default were given loans.  

The oversampled data gives a much better recall score, of 99%, meaning that of the loans that are going to default, only 1% were classified as healthy and the money loaned out and defaulted. 

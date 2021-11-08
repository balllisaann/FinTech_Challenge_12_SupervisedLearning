# FinTech_Challenge_12_SupervisedLearning

Author: Lisa Bailey (balllisaann@yahoo.com)
Date: 11/7/2021

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

### Purpose


An **abusurdly** simple Logisitc Regression model was used to analyze the data.  
* We were not prompted to see if there were any missing values (there were not).
* We were not prompted to see if there was any categorical or ordinal data that needed to be encoded (there was only numeric data).
* We were not promped to **scale** the data.
* We were never even taught about **feature/variable reduction**
* We were never taught to check for basic assumptions for Logistic Regression, like there should be at least 50 test data points per feature/variable.

### Data used 

The data used was loan data.

Shape: (77536, 8)

Loan Status: 
0 (Healthy loans): 75036
1 (Unhealthy loans): 2500

          loan_size  interest_rate  borrower_income  debt_to_income  \
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


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

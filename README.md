# credit-risk-classification
Credit risk classification using supervised learning

# Credit Risk Report Analysis

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The purpose of the analysis is to train and test two machine learning models using supervised learning to determine if the original data or resampled data is more accurate and precise in making correct predictions on loan health status.

* Explain what financial information the data was on, and what you needed to predict.

The financial information the data was on involved loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, and total debt. I needed to predict whether a loan is healthy or high-risk.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

Value_counts for original data (y)
0    75036
1     2500

Value_counts for resampled data (y_resampled)
0    56271
1    56271

* Describe the stages of the machine learning process you went through as part of this analysis.

For the machine learning process, I read data from a CSV file and made features (columns) and labels (answers). Second, I split the data into training and testing data and created logistic regression models for the original dataset and resampled data to fit the trained data into them. Then, I made predictions with those models using the test data. I evaluated and measured the success of those models by looking at the balance accuracy scores when comparing the actual testing data to the model's testing predictions and creating confusion matrices and classification reports.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The LogisticRegression function was used to create the first model while RandomOverSampler was used to create the second one. train_test_split allowed training and testing data to be made. confusion_matrix and classification_report were needed to make confusion matrix and classification report respectively.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    Accuracy - .99
    Precision - Class 0: 1.00
                Class 1: .85
    Recall - Class 0: .99
             Class 1: .91
             
The ML model using the original dataset has an accuracy of .99, precision for class 0(healthy loans) of 1.00, precision for class 1(high-risk loans) of .85, recall for class 0 of .99, and recall for class 1 of .91.  


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    Accuracy - .99
    Precision - Class 0: 1.00
                Class 1: .84
    Recall - Class 0: .99
             Class 1: .99
  
The ML model using the resampled data has an accuracy of .99, precision for class 0(healthy loans) of 1.00, precision for class 1(high-risk loans) of .84, recall for class 0 of .99, and recall for class 1 of .99.  

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?

The models perform well in making accurate and precise predictions on loan health status. In particular, both have high accuracy and precision for healthy loans.

For high-risk loans, the precision is .84 and .85 for machine learning model 1 and machine learning model 2 while the recall is .91 and .99.

Based on the accuracy, precision, and recall scores, the model using the resampled data performs better.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
The performance does depend on the problem we are trying to solve as the model we are training and testing is learning from the data we give it to make predictions as best as it can.

If you do not recommend any of the models, please justify your reasoning.
Due to the lower precision scores for high-risk loans, I personally wouldn't recommend using the models. I would gather more data to train and test the models and see if the precision improves for high-risk loans specifically.

# credit-risk-classification
Employ supervised machine learning leveraging logistic regression to predict creditworthiness of borrowers.

## Overview of the Analysis
The purpose of this analysis was to train and evaluate the performance of a logistic regression model in predicting the creditworthiness of borrowers based on historical lending activity from a peer-to-peer lending services company.

The dataset....(* Explain what financial information the data was on, and what you needed to predict._

The variables...  (* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).)

The process/approach (* Describe the stages of the machine learning process you went through as part of this analysis. * Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).)


## Results

Below are the results of the two logistic regression models deployed in the analysis.

1. Machine Learning Model on the Original Dataset
  - **Balanced Accuracy Score: 0.952**
  <p>In logistic regression, the balanced accuracy score is a metric that measures the classification performance of a model on imbalanced datasets. This score is calculated as the average of the recall scores for each class. Recall (also known as sensitivity or true positive rate) is a metric that measures the percentage of positive cases that are correctly classified by the model. By taking the average recall score for each class, the balanced accuracy score gives equal weight to each class, even if the classes are imbalanced. 
  <p>A balanced accuracy score of 0.952 means that the average recall for each class in the classification problem is 0.952. In other words, the model correctly identifies 95.2% of the positive cases and 95.2% of the negative cases, on average. This indicates that the model is performing very well at discriminating between the two classes and has a high level of accuracy on the test dataset.
    
  - **Precision Scores: 1.00 for Class 0** ('healthy loan') and **0.86 for Class 1** ('risky loan')
    - Interpretation:  
  
  - **Recall Scores: 1.00 for Class 0** ('healthy loan') and **0.91 for Class 1** ('risky loan')
    - Interpretation:
 
2. Machine Learning Model on the Over-Sampled Dataset
  - Description of Accuracy
  - Precision Scores
  - Recall Scores

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

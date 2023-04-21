# credit-risk-classification
Employ supervised machine learning leveraging logistic regression to predict creditworthiness of borrowers.

<img width="1200" alt="Screen Shot 2023-04-21 at 5 42 11 PM" src="https://user-images.githubusercontent.com/44728723/233739076-9477541d-5d58-46f6-997d-152306236158.png">

## Overview of the Analysis
The purpose of this analysis was to train and evaluate the performance of a logistic regression model in predicting the creditworthiness of borrowers based on historical lending activity from a peer-to-peer lending services company.

The dataset....(* Explain what financial information the data was on, and what you needed to predict._

The variables...  (* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).)

The process/approach (* Describe the stages of the machine learning process you went through as part of this analysis. * Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).)


## Results

Below are the results of the two logistic regression models deployed in the analysis.

### 1. Machine Learning Model on the Original Dataset
  - **Balanced Accuracy Score: 0.952**<p>In logistic regression, the balanced accuracy score is a metric that measures the classification performance of a model on imbalanced datasets. This score is calculated as the average of the recall scores for each class. Recall (also known as sensitivity or true positive rate) is a metric that measures the percentage of positive cases that are correctly classified by the model. By taking the average recall score for each class, the balanced accuracy score gives equal weight to each class, even if the classes are imbalanced.<p>A balanced accuracy score of 0.952 means that the average recall for each class in the classification problem is 0.952. In other words, the model correctly identifies 95.2% of the positive cases and 95.2% of the negative cases, on average. This indicates that the model is performing very well at discriminating between the two classes and has a high level of accuracy on the test dataset.
    
  - **Precision Scores: 1.00 for Class 0** ('healthy loan') and **0.86 for Class 1** ('risky loan')<p>The precision score is the ratio of true positives to the total number of predicted positives. For Class 0, the precision is 1.00, which indicates that all of the instances that were predicted as belonging to Class 0 were actually members of that class. For Class 1, the precision is 0.86, which indicates that 86% of the instances that were predicted as belonging to Class were actually members of that class. In other words, 14% of the Class 1 predictions were incorrectly assigned to this class.
  
  - **Recall Scores: 1.00 for Class 0** ('healthy loan') and **0.91 for Class 1** ('risky loan')<p>The recall is the ratio of true positives to the total number of actual positives. For Class 0, the recall is 1.00 which means that all instances that  belonged to Class 0 were correctly classified by the model. For Class 1, the recall is 0.91, which means that 91% of the instances that belonged to Class 1 were correctly classified by the model.
    
  - **F-1 Scores: 1.00 for Class 0** ('healthy loan') and **0.88 for Class 1** ('risky loan')<p> The F1 score is the mean the combined precision and recall scores. For Class 0, the F1 score os 1.00, which indicates high performance. For Class 1, the F1 score is 0.88, which indicates that the model is not performing as well on this class compared to Class 0.
   
 
### 2. Machine Learning Model on the Oversampled Dataset
  - **Balanced Accuracy Score: 0.994**<p>The balanced accuracy score improves with the oversampled data compared to the original data set (which had a balanced accuracy score of 0.952). This indicates the model more accurately distinguishes between the two classes based on the oversampled data.
    
  - **Precision Scores: 1.00 for Class 0** ('healthy loan') and **0.85 for Class 1** ('risky loan')<p>The precision score remains high for Class 0 at 1.00. For Class 1, the precision score actually decreases slightly to 0.85 based on the oversampled data from 0.86 when run on the original data.
  
  - **Recall Scores: 0.99 for Class 0** ('healthy loan') and **0.99 for Class 1** ('risky loan')<p>The recall score for Class 0 remains high but slighly down at 0.99. For Class 1, the recall score improves to 0.99 from 0.91 based on the original dataset.
    
  - **F-1 Scores: 1.00 for Class 0** ('healthy loan') and **0.92 for Class 1** ('risky loan')<p> The F1 score remains at 1.00 for Class 0 and improves to 0.92 for Class 1 (up from 0.88 based on the original data).

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

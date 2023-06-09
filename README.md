# credit-risk-classification
Employ supervised machine learning leveraging **logistic regression** to predict creditworthiness of borrowers.

<img width="1200" alt="Screen Shot 2023-04-21 at 5 42 11 PM" src="https://user-images.githubusercontent.com/44728723/233739076-9477541d-5d58-46f6-997d-152306236158.png">

## Overview of the Analysis
The purpose of this analysis was to train and evaluate the performance of a logistic regression model in predicting the creditworthiness of borrowers based on historical lending activity from a peer-to-peer lending services company.

### Data Description:
 - The dataset contains 77,536 rows of customer financial loan data across 8 feature columns, including: loan_size,	interest_rate,	borrower_income,	debt_to_income,	num_of_accounts,	derogatory_marks,	total_debt, and	loan_status.

 - The "target" variable for the model was the "loan-status" column.  A value of "0" indicates a healthy loan while a value of "1" indicates that the loan has a high risk of defaulting. The original "loan_status" data were unbalanced with 75,036 values of "0" (healthy loans) and 2,500 values of "1" (high risk of defaulting loans).

### Approach:
 - The data were separated into labels (the predicted target value of "loan_status) and features (or remaining columns).
 - The data were split into training and testing sets using scikit learn train_test_split function.
 - A Logistic Regression model was run on the original data which contained the unbalanced target variables.
 - The data was then resampled/oversampled to produce a balanced target variable with 60,035 values for each loan type.
 - A Logistic Regression model was the run on the oversampled training data and test set.

## Results

Below are the results of the two logistic regression models deployed in the analysis.

### 1. Machine Learning Model on the Original Dataset
**<p>Balanced Accuracy Score: 0.952</p>**
<img width="200" alt="Screen Shot 2023-04-24 at 9 19 10 AM" src="https://user-images.githubusercontent.com/44728723/234008469-6c5a4dca-efa3-48e1-9789-b3f752b7a0f9.png">
<p>In logistic regression, the balanced accuracy score is a metric that measures the classification performance of a model on imbalanced datasets. This score is calculated as the average of the recall scores for each class. Recall (also known as sensitivity or true positive rate) is a metric that measures the percentage of positive cases that are correctly classified by the model. By taking the average recall score for each class, the balanced accuracy score gives equal weight to each class, even if the classes are imbalanced.<p>A balanced accuracy score of 0.952 means that the average recall for each class in the classification problem is 0.952. In other words, the model correctly identifies 95.2% of the positive cases and 95.2% of the negative cases, on average. This indicates that the model is performing very well at discriminating between the two classes and has a high level of accuracy on the test dataset.

**<p>Classification Report</p>**
  <img width="357" alt="Screen Shot 2023-04-24 at 8 44 36 AM" src="https://user-images.githubusercontent.com/44728723/233999851-704fa6d3-af89-436c-9069-76f14dea0c6d.png">
 
 - **Precision Scores: 1.00 for Class 0** ('healthy loan') and **0.86 for Class 1** ('risky loan')<p>The precision score is the ratio of true positives to the total number of predicted positives. For Class 0, the precision is 1.00, which indicates that all of the instances that were predicted as belonging to Class 0 were actually members of that class. For Class 1, the precision is 0.86, which indicates that 86% of the instances that were predicted as belonging to Class 1 were actually members of that class. In other words, 14% of the Class 1 predictions were incorrectly assigned to this class.
  
 - **Recall Scores: 1.00 for Class 0** ('healthy loan') and **0.91 for Class 1** ('risky loan')<p>The recall is the ratio of true positives to the total number of actual positives. For Class 0, the recall is 1.00 which means that all instances that  belonged to Class 0 were correctly classified by the model. For Class 1, the recall is 0.91, which means that 91% of the instances that belonged to Class 1 were correctly classified by the model.
    
 - **F-1 Scores: 1.00 for Class 0** ('healthy loan') and **0.88 for Class 1** ('risky loan')<p> The F1 score is the mean the combined precision and recall scores. For Class 0, the F1 score os 1.00, which indicates high performance. For Class 1, the F1 score is 0.88, which indicates that the model is not performing as well on this class compared to Class 0.
   
 
### 2. Machine Learning Model on the Oversampled Dataset
**<p>Balanced Accuracy Score: 0.994</p>**
<img width="200" alt="Screen Shot 2023-04-24 at 9 19 17 AM" src="https://user-images.githubusercontent.com/44728723/234008532-9941b3b4-0f5b-46a0-a5ef-913733ce88cc.png">
<p>The balanced accuracy score improves with the oversampled data compared to the original data set which had a balanced accuracy score of 0.952). This indicates the model more accurately distinguishes between the two classes based on the oversampled data.

**<p>Classification Report</p>**
  <img width="353" alt="Screen Shot 2023-04-24 at 8 48 14 AM" src="https://user-images.githubusercontent.com/44728723/234000675-e21bdcf7-37c9-48bd-9fdf-64db3c2b46ea.png">
   
  - **Precision Scores: 1.00 for Class 0** ('healthy loan') and **0.85 for Class 1** ('risky loan')<p>The precision score remains high for Class 0 at 1.00. For Class 1, the precision score actually decreases slightly to 0.85 based on the oversampled data from 0.86 when run on the original data.
  
  - **Recall Scores: 0.99 for Class 0** ('healthy loan') and **0.99 for Class 1** ('risky loan')<p>The recall score for Class 0 remains high but slightly down at 0.99. For Class 1, the recall score improves to 0.99 from 0.91 based on the original dataset.
    
  - **F-1 Scores: 1.00 for Class 0** ('healthy loan') and **0.92 for Class 1** ('risky loan')<p> The F1 score remains at 1.00 for Class 0 and improves to 0.92 for Class 1 (up from 0.88 based on the original data).

## Summary

Based on the performance metrics above, the model run on the oversampled dataset appears to perform better. The balanced accuracy score for the oversampled model is higher (0.994) than the original model (0.952), indicating better overall performance in terms of correctly classifying both healthy and risky loans.

Additionally, while the precision score for Class 1 (risky loans) is slightly lower for the oversampled model (0.85 compared to 0.86 for the original model), the recall and F-1 scores are higher for Class 1 in the oversampled model. This indicates that the oversampled model is better at correctly identifying risky loans, which is an important factor in the context of loan classification. Overall, the oversampled model is the recommended model to use for this case. However, it's worth considering other factors such as the computational cost and feasibility of oversampling the data when deciding on the best model for a specific use case.
   

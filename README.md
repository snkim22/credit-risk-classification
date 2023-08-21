# Credit Risk Classification

### Purpose:
  - Develop machine learning models to predict **loan statuses** based on provided financial data.
      - loan_size
      - interest_rate
      - borrower_income
      - debt_to_income
      - num_of_accounts
      - derogatory_marks
      - total_debt

### Stages of the machine learning process
1. Data Preperation: dataset read in and split into training and testing sets using `train_test_split`
2. A `logistic regression` model was applied to the training data and predications were made using the testing data `X_test`
3. Used Random Oversampling with `RandomOverSampler` to address class imbalance in the training data and make new predictions using the testing data
4.  `Logistic regression` was applied to the resampled training data and predictions were recalculated
5.  Evaluation metrics calculated

### Results:
1. Logistic Regression Model 1:
   
    - Balanced Accuracy: 0.9520479254722232
    - Accuracy: 99%
    - Precision: healthy loan = 100%/ high-risk loan = 85%
    - Recall: healthy loan = 99%/ high-risk loan = 91%
      
3. Logistic Regression Model 2 with Resampled Data:
    - Balanced Accuracy: 0.9936781215845847
    - Accuracy: 99%
    - Precision: healthy loan = 100%/ high-risk loan = 84%
    - Recall: healthy loan = 99%/ high-risk loan = 99%
  
### Summary:
  - Based on the evaluation results both models show high precision, recall, and accuracy. However, The second model using oversmpled data has a higher recall for high-loans as well as a higher balanced accuracy score.
  - In this specific case, predicting high-risk loans are more important than healthy loans.
  - The second model using resampled data is the better choise as it is more effective at identifying high-risk loans with a higher recall rate.
  - It identifies high-risk loans more accuratly and mimizes the risk of not detecting loans that are at risk of default. 

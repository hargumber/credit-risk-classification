# Module 20 Report

## Analysis

#### Purpose of the Analysis
* The purpose of the analysis was to look at different features of the data and come up with a model that can preddict whether the loan is high-risk or healthy.
* For this, we used a lending dataset that contained the following features, laon_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt. We had to predict the loan_status i.e. 0 for healthy and 1 for high-risk.

#### Stages of the Machine Learning Process

The stages of the machine learning process were as follows:
* Separate out the target variable/column i.e. loan_status and store is a series (y)
* All the other features(variables) were then stored in a dataframe (X)
* Next, split the features and target variables into training and test tests using the train_test_split from sklearn and we used a random state of 1.
* For this analysis, I used Logistic Regression from sklearn, first i created a LogisticRegression model with random state as 1 and fit the training data to the model.
* Next, I used the trained model to predict the test data and come up with predictions.
* Lastly, used the classification report from sklearn to get the accuracy score, precision score, and recall score using both prediction from the model using test data and also the actual target from the test data (that was saved as y_test original as part of splitting the data).
* I will talk about the results in the next section.

## Results

Following are the details of the model created using Logistic Regression:

* Logistic Regression Model:
    * For healthy loans(0), the model has 97% accuracy, 100% recall and 99% precision.
    * For high-risk loans(1), the model has 92% accuracy, 85% recall and 95% precision.

## Summary

* As part of this module challenge, I only used LogisticRegression model to predict loan status and it seems to doing a ok job at predicting the loan status.
* It is important that it does not predict high-risk loans as healthy loans and I noticed that it did do that for 107 loans out of a total of 692 high-risk ones, percentage wise that is 15% which may seem low but for a financial institution it may not be acceptable.
* Overall, the model did a fair job and I would suggest explroing other models before going ahead and using this model as is.

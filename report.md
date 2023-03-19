# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

In this analysis, we use two different logistic regression models (one with raw data and one with resampled data) to build and train a model that can identify the creditworthiness of borrowers.
By looking at the loan size, interest rate,	borrower's income,	debt to income ratio,	number of accounts,	derogatory marks and current total debt	a borrower has, we predict whether it is risky or not for the bank to provide a loan to a borrower.In our dataset, there are 77,536 loans in total. By using the value_counts function we are able to see the amount of each of these values, with `0` being the customers that paid their loan back, and `1` being the customers that defaulted on their loan.

The data was first split into the loan status column and the data features were then split into training data and testing data. Then we fit a logistic regression model using the training data. Then we used the model to do predictions using the testing data and provide the model's accuracy score, as well as produce a confusion matrix and classification report that better summarize the overall performance of our model.

For our second model, we use random oversampling to rebalance the training data (increasing the amount of loan samples with loan status `1`). We use this method to test our model's prediction capabilities on a non-skewed dataset. This new model is then fit using logistic regression on the resampled data, then we make predictions using the original test data. After the predictions are made, we can provide the model's accuracy score, confusion matrix and classification report from our model's results.


## Results

* Machine Learning Model 1: Logistic Regression using regular data

  * Description of Model 1 Accuracy, Precision, and Recall scores.

Balanced Accuracy Score: 0.9520479254722232


Confusion Matrix

	        Predicted 0	Predicted 1
Actual 0	  18663	      102
Actual 1	    56	      563

Confusion Matrix results
    True positive:  18663   
    False positive: 56
    True negative:  563
    False negative: 102


Low Risk  precision    recall  f1-score
              1           .99     1
High Risk precision    recall  f1-score
              .85         .91     .88

Overall accuracy  0.99

* Machine Learning Model 2: Logicstic regression using random oversampling

  * Description of Model 2 Accuracy, Precision, and Recall scores.

Balanced Accuracy Score: 0.9936781215845847


          Confusion Matrix
          Predicted 0	  Predicted 1
Actual 0	   18649	       116
Actual 1	      4	         615


Confusion Matrix results
    True positive:  18649  
    False positive: 4
    True negative:  615
    False negative: 116


Low Risk  precision    recall  f1-score
              1           .99     1
High Risk precision    recall  f1-score
              .84         .99     .91

Overall accuracy  0.99     


## Summary

Even though the precision (true positive predictions) for high risk loans is slightly higher on the first model, 
the second model (using resampled data) has a better recall (True positive prediction rate) score.The most important 
part to predict is which loans are a risk for a bank to give out (the `1`'s), to prevent the bank from incurring losses 
from giving out loans to high risk customers.


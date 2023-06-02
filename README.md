# Credit-Card-Default-Prediction
![image](https://github.com/shubham-bhadouria/Credit-Card-Default-Prediction/assets/103518257/2fa3bea2-0a59-4a2b-bacd-cb03617a8fe0)


# Problem Description
This project is aimed at predicting the case of customers default payments in Taiwan. From the perspective of risk management, the result of predictive accuracy of the estimated probability of default will be more valuable than the binary result of classification - credible or not credible clients. We can use the K-S chart to evaluate which customers will default on their credit card payments

# Attribute Information:
This research employed a binary variable, default payment (Yes = 1, No = 0), as the response variable. This study reviewed the literature and used the following 23 variables as explanatory variables:
- X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
- X2: Gender (1 = male; 2 = female).
- X3: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
- X4: Marital status (1 = married; 2 = single; 3 = others).
- X5: Age (year).
- X6 - X11: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005; X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
- X12-X17: Amount of bill statement (NT dollar). X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005.
- X18-X23: Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.

## Project Overview

Credit Card Fraud Detection with Machine Learning models is a data investigation process that aims to develop a model capable of effectively identifying and preventing fraudulent transactions. In this project, we perform an in-depth analysis of credit card user data from Taiwan and make predictions regarding whether a customer will be a defaulter or non-defaulter.

## Data Preparation and Exploratory Data Analysis (EDA)

The initial step involves loading the dataset and checking for any null values or duplicate rows. Fortunately, our dataset is clean, with no duplicate or null values present.

Next, we conduct Exploratory Data Analysis (EDA) on the dataset. We examine the relationship between the dependent variable, 'default payment next month,' and various independent variables. Specifically, we explore the relationships between 'Education' and 'Defaulter/Non-defaulter,' 'AGE' and 'Defaulter/Non-defaulter,' 'Married' and 'Defaulter/Non-defaulter,' 'Pay_month' and 'Defaulter/Non-defaulter,' 'Bill_amount' and 'Defaulter/Non-defaulter,' as well as the relationship between 'AGE,' 'LIMIT_BAL,' and 'Defaulter/Non-defaulter.'

Additionally, we introduce a new feature called 'age group' and analyze its relationship with the target variable. Furthermore, we plot a correlation heatmap, revealing that 'LIMIT_BAL,' 'SEX,' 'EDU,' 'AGE,' and 'MARRIAGE' are not highly correlated with each other. Moreover, individuals who consistently pay their bills on time are more likely to pay their future bills on time as well.

## Data Preprocessing and Model Fitting

After extracting valuable insights from the dataset, we perform one-hot encoding and drop unnecessary columns to prepare the dataset for training various machine learning models.

We fit the data into five different models, namely KNN model, Random Forest model, XGBoost model, SVM model, and LGBT model. Among these models, the LGBT model demonstrates superior performance, achieving the highest test accuracy (0.861682), precision score (0.805032), F1 score (0.853379), and ROC score (0.866385) compared to the other models.

## Conclusion

In conclusion, our analysis reveals that most defaulters have a university education and credit limits ranging from 50000 to 200000. Credit cardholders who have no consumption or pay their bills in full each month, or experience a one-month delay, are more likely to be non-defaulters. On the other hand, for those who utilize revolving credit (paying only the minimum amount due), the number of non-defaulters far exceeds the number of defaulters. However, individuals who consistently delay their payments for more than one month exhibit a higher likelihood of defaulting, indicating that longer payment delays correspond to increased default risk.

By leveraging machine learning models, we can effectively predict credit card defaults and implement proactive measures to prevent fraudulent transactions. This project provides valuable insights to financial institutions and credit card companies, enabling them to make informed decisions regarding risk assessment, credit limits, and debt collection strategies.

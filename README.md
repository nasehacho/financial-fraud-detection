# financial-fraud-detection

A basic machine learning pipeline that includes the ensemble classifier (random forest model) that will assess if fraudulent activity has occurred for a transaction in a psuedo-dataset.

<div style="text-align:center">
  <img src="images/image.png">
</div>

## Data Overview

The initial dataset consisted of 6362620 entries and 11 columns.

The columns of the dataset were as follows:

- Step: A unit of time that represents hours in the dataset. Like the timestamp
  of the transaction (e.g. hour 1, hour 2, ... hour 534, ...)
- Type: The type of transaction
- Amount: The amount of money transferred
- NameOrig: The origin account name

- OldBalanceOrg: The origin accounts balance before the transaction
- NewBalanceOrg: The origin accounts balance after the transaction
- NameDest: The destination account name
- OldbalanceDest: The destination accounts balance before the transaction
- NewbalanceDest: The destination accounts balance after the transaction
- IsFlaggedFraud: A “naive” model that simply flags a transaction as fraudulent if it is
  greater than 200,000 (note that this currency is not USD)
- IsFraud: Was this simulated transaction actually fraudulent? In this case, we consider
  “fraud” to be a malicious transaction that aimed to transfer funds out of a victim’s bank
  account before the account owner could secure their information.

## EDA

[Exploratory Data Analysis](https://github.com/nasehacho/financial-fraud-detection/blob/main/notebooks/01-Fraud-Data-Initial-EDA.ipynb)

## Pre-Processing

[Data Pre-Processing](https://github.com/nasehacho/financial-fraud-detection/blob/main/notebooks/02-Fraud-Data-Pre-Processing.ipynb)

## Data Modeling

[Data Modeling](https://github.com/nasehacho/financial-fraud-detection/blob/main/notebooks/03-Fraud-Data-Modeling.ipynb)

The chosen ensemble method used for this dataset had been the Random Forest Model. A random forest is a meta estimator that fits a number of decision tree classifiers on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting.

## Fraud Report

[Data Report](https://github.com/nasehacho/financial-fraud-detection/blob/main/notebooks/04-Fraud-Report.ipynb)

# Lead-Conversion-Prediction

## Project Overview

This project demonstrates a lead conversion prediction workflow using a publicly available dataset. The objective is to predict which customers are most likely to purchase a banking product, showcasing a complete data mining process from data cleaning and feature engineering to modeling and evaluation.

The project highlights skills in R, machine learning, and data analysis, and is designed for demonstration purposes.

## Dataset

The dataset used for this assignment is adapted from Analytics Vidhya: Analytics Vidhya DataHack

Important: The full dataset is not included in this repository due to size and licensing. A small sample CSV may be included for demonstration purposes.

### Dataset structure (16 variables, 220,000 records):
#### Demographic

- Gender, Occupation, Dependent, Marital Status, Region Code

#### Bank Account Information

- Account Type, Vintage (months since account opening), Average Account Balance, Credit Product, Active, Registration

#### Target Variable

- Target – Binary indicator of customer conversion (1 = converted, 0 = not converted)

#### Numerical Variables

- Continuous: Average Account Balance

- Discrete: Age, Years at Residence, Vintage

#### Categorical Variables

- Nominal: Gender, Occupation, Dependent, Marital Status, Region Code, Channel Code, Credit Product, Active, Registration

- Ordinal: Account Type

The dataset contains some missing values and class imbalance, which were handled during data preparation.


### 1. Data Preparation

- Removed irrelevant ID columns

- Factorized and encoded categorical variables

- Imputed missing values using MICE (Multiple Imputation by Chained Equations) with CART

- Corrected abnormal entries in the Dependent variable

- Addressed class imbalance using under-sampling, over-sampling, and combined sampling

### 2. Feature Engineering

- Conducted Information Gain analysis to select informative features

- Features like Registration and Credit Product were highly predictive

### 3. Modeling

Four predictive models were implemented:

- Logistic Regression (LR)

- Support Vector Machine (SVM)

- Decision Tree (DT)

- Random Forest (RF)

Feature selection reduced dataset complexity for large-scale modeling.

### 4. Model Evaluation

- Metrics used: Precision, Recall, F1 Score, AUC-ROC

- Random Forest showed the strongest overall performance:

- F1 Score: 0.6378

- AUC: 0.8963

- Confusion matrices and ROC curves were used to visualize predictive performance

## Key Findings

- Customers who registered or had no existing credit product were more likely to convert

- Random Forest was selected as the optimal model for this project

- Proper handling of missing values and class imbalance significantly improved model performance


## Technologies & Libraries

R, RMarkdown

Key libraries: tidyverse, dplyr, caret, randomForest, ROSE, pROC, e1071, C50, party, mice, FSelector


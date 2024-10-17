# Bank Customer Churn Prediction

## Overview
This project aims to predict customer churn for a bank using machine learning techniques. The dataset includes customer information such as age, balance, number of products used, geography, and more. The objective is to identify key factors that lead to customer churn and build a model to predict churn effectively.

## Dataset
The dataset consists of the following key columns:
- `CustomerId`: Unique identifier for each customer.
- `CreditScore`: Customer's credit score.
- `Geography`: Customer's location (countries such as France, Germany, and Spain).
- `Gender`, `Age`, `Balance`, `NumOfProducts`, etc.
- `Exited`: Target variable (1 = churned, 0 = stayed).

## Project Workflow
1. **Data Cleaning**:
   - Removed unnecessary columns (`CustomerId`, `Surname`) that don't add value to the model.
   - Handled missing values and ensured no NaNs remained in critical columns.

2. **Exploratory Data Analysis (EDA)**:
   - Key insights showed older customers with higher balances are more likely to churn.
   - Regional differences were also observed, especially in Germany, which had a higher churn rate.
   - The number of products a customer uses and active membership status also play a significant role in predicting churn.

3. **Feature Engineering**:
   - Created dummy variables for categorical features such as `Geography`.
   - Applied ordinal encoding to credit score categories.

4. **Modeling**:
   - Used a **Random Forest Classifier** to predict churn.
   - Feature importance identified `Age`, `Balance`, and `NumOfProducts` as key predictors.
   - The initial model achieved an AUC-ROC score of **0.86**.

5. **Hyperparameter Tuning**:
   - Improved model performance using **RandomizedSearchCV** to optimize parameters, achieving a final AUC-ROC score of **0.89**.

## Key Features
- **Age** and **Balance** are crucial in predicting churn.
- Geography-based trends, particularly in Germany, showed higher churn rates.
- Customers with two products are less likely to churn.

## Model Performance
- **Model**: Random Forest Classifier
- **Initial AUC-ROC Score**: 0.86
- **AUC-ROC after Tuning**: 0.89

## Conclusion
This project demonstrates how machine learning can effectively identify at-risk customers and provide valuable insights for banks to retain clients. By understanding the key factors influencing churn, banks can take proactive measures to reduce customer churn and increase retention.



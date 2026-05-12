# Predicting Loan Default Using Random Forest

## Project Goal
The goal of this project is to predict whether a borrower will default on a loan using machine learning techniques. A Random Forest classifier was developed to identify patterns associated with loan default risk. The project also explored class imbalance, threshold tuning, feature importance, and model evaluation metrics to improve predictive performance.

## Dataset
The dataset used in this project comes from Lending Club, a peer to peer lending platform that connects borrowers and investors. The dataset was obtained from Kaggle and contains loan records issued between 2007 and 2015.

The data includes borrower financial information, credit history variables, loan characteristics, and repayment outcomes. During preprocessing, columns with excessive missing values, leakage variables, high cardinality, and highly redundant features were removed to create a cleaner modeling dataset.

## Model Used
A Random Forest classifier was used as the primary machine learning model. The workflow included:

- Exploratory Data Analysis (EDA)
- Missing value analysis
- Leakage detection and removal
- Feature engineering
- One hot encoding of categorical variables
- Train test split
- Baseline model comparison
- Random Forest classification
- Hyperparameter tuning using RandomizedSearchCV
- Threshold tuning for classification performance
- Model evaluation using accuracy, precision, recall, F1 score, ROC curve, AUC, and confusion matrices

The final tuned Random Forest model achieved a balanced performance between identifying defaults and minimizing false predictions.

## Results
The tuned Random Forest model achieved an AUC score of approximately 0.71, indicating moderate ability to distinguish between defaulted and fully paid loans. Different probability thresholds were evaluated to analyze the tradeoff between precision and recall.

The final tuned model achieved:
- Accuracy: 67%
- Precision: 33%
- Recall: 63%
- F1 Score: 0.435

## Key Findings
Several preprocessing decisions substantially impacted model performance. Leakage variables related to repayment activity were identified and removed after feature importance analysis revealed unrealistic predictive behavior. Class imbalance and probability threshold selection also played a major role in model performance.

The most important predictors included:
- Interest rate
- Debt to income ratio
- Installment amount
- Revolving utilization
- Credit limit variables

The project demonstrated that high accuracy alone can be misleading in imbalanced classification problems and highlighted the importance of recall, F1 score, and threshold tuning in credit risk prediction.

**Disclaimer**
Note: The original dataset was excluded from the GitHub repository due to GitHub file size limitations. The dataset can be provided separately if needed to reproduce the analysis.
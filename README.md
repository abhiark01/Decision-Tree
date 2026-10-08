#  Comprehensive Credit Risk & Loan Default Predictor

A Machine Learning project using **Decision Tree algorithms** to analyze loan applications, predict loan default risk, and predict loan interest rates using a LendingClub-style dataset.


## Project Overview

This project covers both **Decision Tree Classification** and **Decision Tree Regression**.

### Classification
Predict whether a loan will be fully paid or **not fully paid**.

- `0` → Fully Paid
- `1` → Not Fully Paid

### Regression
Predict the **loan interest rate (`int.rate`)**.

The project demonstrates:

- Exploratory Data Analysis
- Categorical Encoding
- Train-Test Split
- Decision Tree Classification
- Decision Tree Regression
- Overfitting Detection
- Pre-Pruning
- Post-Pruning
- Class Imbalance Handling
- Hyperparameter Tuning
- Feature Importance
- Model Evaluation


## Dataset

The dataset contains **9,578 loan records** and **14 columns**.

Important features include:

`credit.policy`, `purpose`, `int.rate`, `installment`, `log.annual.inc`, `dti`, `fico`, `days.with.cr.line`, `revol.bal`, `revol.util`, `inq.last.6mths`, `delinq.2yrs`, `pub.rec`, `not.fully.paid`

- **Missing Values:** None
- **Categorical Feature:** `purpose`
- **Encoding:** One-Hot Encoding

The target class is imbalanced:

- Fully Paid: **83.99%**
- Not Fully Paid: **16.01%**


## Classification – Loan Default Prediction

**Model:** `DecisionTreeClassifier`

**Best Parameters:**

- `max_depth = 5`
- `min_samples_split = 10`
- `min_samples_leaf = 1`
- `class_weight = "balanced"`

### Results

| Metric | Score |
|---|---:|
| Accuracy | 61.43% |
| Precision | 22.52% |
| Recall | 57.65% |
| F1-Score | 32.39% |

**Key Finding:** Due to class imbalance, Recall and F1-score are more meaningful than accuracy alone. The balanced model identifies around **58% of risky loans**.


## Regression – Interest Rate Prediction

**Model:** `DecisionTreeRegressor`

**Best Parameters:**

- `max_depth = 7`
- `min_samples_leaf = 5`
- `min_samples_split = 2`

### Results

| Metric | Score |
|---|---:|
| MAE | 0.01087 |
| RMSE | 0.01511 |
| R² | 0.66819 |

**Example Prediction:** The model predicted an interest rate of approximately **11.04%** for a sample loan.


## Important Features

### Classification
- `int.rate`
- `credit.policy`
- `inq.last.6mths`

### Regression
- `fico`
- `installment`
- `purpose_small_business`
- `dti`
- `revol.util`


## Technologies

**Python • Pandas • NumPy • Scikit-learn • Matplotlib • Seaborn • Jupyter Notebook**


## Key Learning Outcomes

- Building Decision Tree Classification and Regression models
- Handling imbalanced datasets
- Detecting and reducing overfitting
- Applying pre-pruning and post-pruning
- Hyperparameter tuning using `GridSearchCV`
- Evaluating classification using Precision, Recall and F1-score
- Evaluating regression using MAE, RMSE and R²
- Understanding feature importance
# Credit Default Prediction and Expected Loss Estimation

## Project Overview

This project builds a credit risk modelling framework to estimate borrower default risk and expected credit loss.

The project uses borrower-level financial and behavioural data to:

1. Understand borrower risk characteristics
2. Identify variables associated with default
3. Build a Probability of Default model
4. Classify borrowers into risk bands
5. Estimate Expected Loss using the credit risk formula

Expected Loss = PD × LGD × EAD

Where:

- PD = Probability of Default
- LGD = Loss Given Default
- EAD = Exposure at Default

## Business Problem

Banks, NBFCs, and fintech lenders need to assess borrower risk before lending. Poor credit decisions can lead to loan defaults, higher provisioning requirements, and portfolio losses.

This project answers the following business questions:

1. Which borrower characteristics are linked to default risk?
2. Can we estimate the probability of default for each borrower?
3. Can borrowers be classified into meaningful risk bands?
4. What is the expected credit loss for the portfolio?

## Dataset

Dataset used: Give Me Some Credit dataset from Kaggle.

The raw dataset is not uploaded to this repository due to data-sharing restrictions. Users should download the dataset separately and place it inside:

data/raw/

Main file used:

cs-training.csv

## Project Structure

```text
Credit-Default-Prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_eda_credit_risk.ipynb
│   ├── 03_pd_model_logistic_regression.ipynb
│   ├── 04_expected_loss_estimation.ipynb
│   └── 05_model_validation_and_scorecard.ipynb
│
├── src/
├── reports/
├── dashboard/
├── requirements.txt
├── .gitignore
└── README.md
```

## Methodology

### 1. Data Understanding

The first notebook examines the dataset structure, target variable, missing values, and baseline default rate.

### 2. Exploratory Data Analysis

The second notebook analyses the relationship between borrower characteristics and default risk.

Key areas analysed include:

- Age group
- Past due behaviour
- 90+ days late behaviour
- Credit utilization
- Debt ratio
- Correlation with default

### 3. Probability of Default Model

The third notebook builds a logistic regression model to estimate the Probability of Default.

Logistic regression was selected because it is interpretable and commonly used as a baseline model in credit risk modelling.

### 4. Risk Band Creation

Borrowers are classified into risk bands based on predicted Probability of Default:

- Low Risk
- Medium Risk
- High Risk
- Very High Risk

### 5. Expected Loss Estimation

The fourth notebook calculates Expected Loss using:

Expected Loss = PD × LGD × EAD

Since the public dataset does not contain actual loan exposure or recovery data, LGD and EAD are assumed for demonstration purposes.

### 6. Model Validation and Scorecard Analysis

The fifth notebook validates the Probability of Default model using credit risk model evaluation techniques.

The notebook includes:

- ROC-AUC
- Gini Coefficient
- KS Statistic
- Risk Decile Analysis
- Threshold Analysis
- Logistic Regression Coefficients
- Scorecard-style Risk Ranking

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- GitHub

## Key Outputs

The project produces:

1. Probability of Default for each borrower
2. Risk band classification
3. Borrower-level expected loss
4. Portfolio-level expected loss
5. Expected loss summary by risk band
6. Model validation metrics
7. Scorecard-style risk ranking

## Business Use Case

This type of model can support:

- Credit underwriting
- Portfolio monitoring
- Risk-based pricing
- Provisioning decisions
- Early warning systems
- Lending policy design

## Current Status

Completed:

- Data understanding
- Exploratory data analysis
- Logistic regression PD model
- Risk band classification
- Expected loss estimation
- Model validation and scorecard analysis

## Future Improvements

- Compare logistic regression with decision tree, random forest, and XGBoost
- Build a Power BI dashboard
- Add stress testing scenarios
- Create a formal model report
- Improve feature engineering
- Add model monitoring metrics such as Population Stability Index
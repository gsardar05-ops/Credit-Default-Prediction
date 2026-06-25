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
│   └── 04_expected_loss_estimation.ipynb
│
├── src/
├── reports/
├── dashboard/
├── requirements.txt
├── .gitignore
└── README.md

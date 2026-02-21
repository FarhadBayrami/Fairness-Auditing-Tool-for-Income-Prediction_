# FarhadBayrami-Fairness-Auditing-Tool-for-Income-Prediction_
A project to develop a fairness auditing tool for detecting and mitigating bias in ML income prediction models using the Adult dataset.

# Fairness Auditing Tool for Income Prediction Models

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Project Overview
This project develops a fairness auditing tool to detect and mitigate biases in machine learning models for income prediction. Using the Adult Income Dataset, we train multiple classifiers (Logistic Regression, Decision Tree, Random Forest, SVM, KNN, AdaBoost, Gradient Boosting, Neural Network) and evaluate them for accuracy and fairness (demographic parity) across sensitive features: race, education, and sex.

Key objectives:
- Identify biases in income predictions related to protected attributes.
- Compare model fairness and performance.
- Explore mitigation strategies (e.g., reweighting, adversarial debiasing).

Inspired by ethical concerns in ML, this addresses questions like sources of bias, algorithmic fairness, and generalizability.

## Files
- `Fairness_Auditing_Income_Prediction.ipynb`: Jupyter notebook with code for data loading (Adult dataset), preprocessing, model training, evaluation (accuracy, demographic parity), and fairness analysis.
- `Fairness and Bias Detection Proposal.pdf`: Project proposal document outlining objectives, methodology (data collection, model development, fairness assessment, bias mitigation, evaluation), and key questions.

## Installation
1. Clone the repo:
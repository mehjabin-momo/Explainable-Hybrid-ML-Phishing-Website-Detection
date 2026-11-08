# An Explainable Hybrid Machine Learning Approach for Phishing Website Detection

A machine learning project that detects phishing websites using hybrid models and explains the predictions with SHAP. Built in Python on Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mehjabin-momo/Explainable-Hybrid-ML-Phishing-Website-Detection/blob/main/Group_08_Phishing_Website_Detection_Project.ipynb)

## What it does

- Classifies a website as **phishing** or **legitimate**
- Compares Logistic Regression, Random Forest, and XGBoost
- Builds two hybrid models: a **soft-voting ensemble** and a **stacking ensemble**
- Explains predictions with **SHAP**, showing which features push a website toward phishing

## Datasets

- **PhiUSIIL Phishing URL dataset:** 235,795 websites, used for data exploration, feature importance, and testing how the model behaves when top features are removed
- **UCI Phishing Websites dataset:** 11,055 websites with 30 features, used to train and compare the hybrid models

## Results (UCI dataset)

| Model | Accuracy |
|---|---|
| Random Forest | 97.5% |
| XGBoost | 96.2% |
| Voting Hybrid | 96.5% |
| **Stacking Hybrid** | **97.6%** |

On the PhiUSIIL dataset, Random Forest reached about 99.98% accuracy even after removing the most influential features, which shows many features carry strong signal.

<img width="863" height="587" alt="Screenshot 2026-11-08 135508" src="https://github.com/user-attachments/assets/f133f210-7c1f-4fab-8a61-510434bed2ab" />


## Tech used

- Python, pandas, NumPy
- scikit-learn, XGBoost
- SHAP
- Matplotlib, Seaborn
- Google Colab

## Course

CSE 437, BRAC University

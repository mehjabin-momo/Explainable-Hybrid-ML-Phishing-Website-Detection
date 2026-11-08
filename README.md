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

| Model | Accuracy | ROC AUC |
|---|---|---|
| Random Forest | 97.5% | 0.9964 |
| XGBoost | 96.2% | 0.9944 |
| Voting Hybrid | 96.5% | 0.9954 |
| **Stacking Hybrid** | **97.6%** | **0.9973** |

On the PhiUSIIL dataset, Random Forest reached about 99.98% accuracy even after removing the most influential features, which shows many features carry strong signal.

### Model performance comparison
<img width="1236" height="605" alt="Screenshot 2026-11-08 140015" src="https://github.com/user-attachments/assets/861490db-3d4b-4f63-84a6-083bd8247436" />

### ROC curve comparison
<img width="863" height="587" alt="Screenshot 2026-11-08 135508" src="https://github.com/user-attachments/assets/f133f210-7c1f-4fab-8a61-510434bed2ab" />
*ROC curve comparison on the UCI dataset. The Stacking Hybrid model scores highest (AUC = 0.9973).*

### Explainability (SHAP)
<img width="1065" height="474" alt="Screenshot 2026-11-08 140549" src="https://github.com/user-attachments/assets/7ef88ba6-59a6-452f-b743-f6b205a7e1ed" />
SHAP shows which features most influence whether a website is predicted as phishing, so the model's decisions can be understood and not just trusted.

## Tech used

- Python, pandas, NumPy
- scikit-learn, XGBoost
- SHAP
- Matplotlib
- Google Colab

## Course

CSE 437, BRAC University

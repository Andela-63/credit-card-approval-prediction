# 💳 Credit Card Approval Prediction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/credit-card-approval-prediction/blob/main/Credit_Card_Approval_Prediction.ipynb)
![Python](https://img.shields.io/badge/Python-3.10-blue)
![scikit--learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![License](https://img.shields.io/badge/License-MIT-green)

An end-to-end machine learning project that predicts whether a bank should
**approve or reject a credit card application**, using a fully interpretable
Logistic Regression model trained on real-world financial data from the UCI
Machine Learning Repository.

> ⚠️ Update `Andela-63` in the badge above (and in the notebook) with
> your own GitHub username after pushing this repo, so the "Open in Colab"
> button works for anyone visiting your profile.

---

## 🎯 Business Problem

Manually reviewing every credit card application is slow, expensive, and
inconsistent. This project builds a model that automates the initial
screening decision, so a bank can:

- Approve/reject applications instantly instead of after days of manual review
- Cut the analyst-hours spent on routine, low-risk applications
- Apply the same decision criteria to every applicant
- Flag risky applications for closer human review

## 📊 Results

| Metric | Score |
|---|---|
| ROC-AUC | **0.88** |
| Accuracy | **0.83** |
| Precision | **0.85** |
| Recall | **0.78** |
| F1-score | **0.82** |

The model reliably separates approved from rejected applicants and is
interpretable enough to explain *why* an application was scored the way it
was — a key requirement in regulated lending decisions.

## 🗂️ Dataset

[UCI Credit Card Approval dataset](http://archive.ics.uci.edu/ml/datasets/credit+approval)
— 690 real (anonymised) credit card applications with a mix of numeric and
categorical features, missing values, and mismatched feature scales,
reflecting the kind of messy data seen in production systems.

## 🛠️ Tech Stack

- **Python** · pandas · NumPy
- **scikit-learn** (Logistic Regression, preprocessing, evaluation metrics)
- **matplotlib** / **seaborn** for visualisation
- **Google Colab** for a zero-setup, shareable execution environment

## 🚀 How to Run

**Option 1 — One-click (recommended):**
Click the *Open in Colab* badge at the top of this README (or of the
notebook itself). Then choose **Runtime → Run all**. No installation needed.

**Option 2 — Locally:**
```bash
git clone https://github.com/YOUR_USERNAME/credit-card-approval-prediction.git
cd credit-card-approval-prediction
pip install -r requirements.txt
jupyter notebook Credit_Card_Approval_Prediction.ipynb
```

## 📁 Repository Structure

```
credit-card-approval-prediction/
├── Credit_Card_Approval_Prediction.ipynb   # Main analysis notebook
├── README.md                               # Project documentation (this file)
└── requirements.txt                        # Python dependencies
```

## 🔍 Project Workflow

1. **Business framing** — define the problem and success metrics
2. **EDA** — visualise missing data, class balance, feature distributions and correlations
3. **Data cleaning** — handle missing values with mean/mode imputation
4. **Preprocessing** — encode categoricals, drop bias-prone features, scale, split
5. **Modelling** — train a Logistic Regression classifier
6. **Evaluation** — ROC-AUC, accuracy, precision, recall, F1, confusion matrix, ROC curve
7. **Interpretation** — read model coefficients to explain approval drivers
8. **Business recommendations** — how a bank could realistically deploy this

## ⚖️ Responsible ML Note

`ZipCode` and `DriversLicense` were deliberately excluded from the model.
Zip code in particular is a well-documented proxy for socio-economic and
racial demographics, and including it risks encoding unfair bias into an
automated lending decision — a real compliance concern under fair-lending
regulation.

## 🔮 Future Work

- Benchmark against tree-based models (Random Forest, XGBoost)
- Tune the decision threshold / use `class_weight` to reflect real business costs
- Run a formal fairness audit across protected attributes
- Wrap the pipeline in a small API (FastAPI/Flask) or Streamlit demo for live scoring

## 📄 License

This project is released under the MIT License — see [LICENSE](LICENSE) for details.

---

*If you found this project useful, consider giving it a ⭐ on GitHub!*

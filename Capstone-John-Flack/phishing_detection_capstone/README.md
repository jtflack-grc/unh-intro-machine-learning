# Phishing Website Detection Capstone

Course 02 - Introduction to Machine Learning for Cybersecurity

## Project Overview

This capstone project applies a supervised machine learning workflow to phishing website detection. The project uses structured website features from the UCI Phishing Websites Dataset to classify websites as either legitimate or phishing.

## Problem Statement

Phishing websites imitate legitimate sites to steal credentials, financial information, or other sensitive data. This project evaluates whether machine learning can support cybersecurity analysts by identifying suspicious websites based on structured website characteristics.

## Dataset

- Dataset: UCI Machine Learning Repository - Phishing Websites Dataset
- Records: 11,055 websites
- Features: 30 integer-coded website characteristics
- Target: phishing vs. legitimate website classification

## Models Used

Two supervised learning models were trained and compared:

1. Logistic Regression - interpretable baseline model
2. Random Forest Classifier - nonlinear ensemble model with feature importance

## Final Results

The Random Forest Classifier was the best-performing model.

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 93.17% | 92.95% | 91.53% | 92.24% | 0.9786 |
| Random Forest | 97.06% | 96.64% | 96.73% | 96.69% | 0.9964 |

Random Forest confusion matrix:

- True Negatives: 1,198
- False Positives: 33
- False Negatives: 32
- True Positives: 948

## Key Predictive Features

The most important Random Forest features were:

- SSLfinal_State
- URL_of_Anchor
- web_traffic
- having_Sub_Domain
- Prefix_Suffix

## Cybersecurity Interpretation

The model can help prioritize suspicious websites for analyst review. In a phishing detection workflow, false negatives are the most serious error type because they represent phishing websites incorrectly classified as legitimate. False positives also matter because they may create unnecessary analyst workload or block legitimate sites.

## Responsible AI Considerations

This type of model should be used as decision support rather than a fully autonomous blocking system. A responsible deployment would include human review, performance monitoring, retraining, threshold tuning, and explainability methods.

## Repository Structure

```text
phishing_detection_capstone/
├── README.md
├── requirements.txt
├── notebooks/
│   └── phishing_detection_capstone.ipynb
├── docs/
│   ├── Project_Documentation_Worksheet.docx
│   └── Project_Documentation_Worksheet_FINAL.pdf
└── data/
    └── README.md
```

## How to Run

1. Install dependencies from `requirements.txt`.
2. Open `notebooks/phishing_detection_capstone.ipynb` in Jupyter.
3. Run all cells from top to bottom.
4. Review the generated metrics, visualizations, and interpretation.

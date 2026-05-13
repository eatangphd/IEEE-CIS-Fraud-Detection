# 🔍 IEEE-CIS Fraud Detection
### Catching Financial Fraud with Machine Learning

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/c/ieee-fraud-detection)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.2+-orange.svg)](https://scikit-learn.org/)

## 📊 Business Problem

**The Cost of Fraud:** Global online payment fraud losses are projected to exceed $48 billion annually. Traditional rule-based systems catch only 30-40% of fraud while flagging 10x more false positives.

**The Challenge:** Build a model that:
- ✅ Catches >85% of fraudulent transactions (High Recall)
- ✅ Flags only 10% of legitimate transactions as suspicious (High Precision)
- ✅ Handles severe class imbalance (only 3.5% of transactions are fraud)
- ✅ Deals with 80%+ missing data across 400+ features

**Real-World Impact:** This model could save a mid-sized e-commerce company $5-10 million annually in fraud losses while reducing customer friction.

## 🎯 Results Summary

| Metric | Score | Industry Benchmark | Interpretation |
|--------|-------|-------------------|----------------|
| **F1-Score** | **0.88** | 0.75 | Balanced performance - beats industry standard |
| **Precision** | **0.92** | 0.80 | 92% of flagged transactions are truly fraudulent |
| **Recall** | **0.85** | 0.70 | Catches 85% of all fraud cases |
| **ROC-AUC** | **0.96** | 0.85 | Excellent discrimination ability |

**Confusion Matrix (on 20% test holdout):**

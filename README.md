# 🔍 IEEE-CIS Fraud Detection
### Catching Financial Fraud with Machine Learning

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/c/ieee-fraud-detection)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.2+-orange.svg)](https://scikit-learn.org/)

## 📊 Business Problem

**The Cost of Fraud:** Fraud costs companies billions annually. This project builds a model to identify fraudulent credit card transactions in real-time, balancing the need to catch fraud (Recall) without annoying customers (Precision).

**The Challenge:** Build a model that:
- ✅ Catches >85% of fraudulent transactions (High Recall)
- ✅ Flags only 10% of legitimate transactions as suspicious (High Precision)
- ✅ Handles severe class imbalance (only 3.5% of transactions are fraud)
- ✅ Deals with 80%+ missing data across 400+ features


## Technical Approach
- **Data Challenge:** Merged `transaction` and `identity` tables (600k+ rows) with 90% missing data in some features.
- **Solution:** Dropped features with >80% nulls, imputed remaining with `median`/`mode`, and used `One-Hot Encoding`.
- **Imbalance:** Applied **SMOTE** to resolve class imbalance where only ~3.5% of transactions were fraud.
- **Model:** `Random Forest Classifier` optimized for Precision/Recall.

## Results
- **F1-Score:** 0.88
- **Precision:** 0.92 (92% of flagged transactions were actually fraud)
- **Recall:** 0.85 (We caught 85% of all fraud cases)

## How to Reproduce
1. Download the data from [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/c/ieee-fraud-detection) or mount the path drive directly from the competition site.
2. Run `pip install -r requirements.txt`.
3. Execute the `fraud_detection.ipynb` notebook.


### 🤝 Contributing
Feel free to fork this project and adapt it for your own use case. Pull requests are welcome!

### 📝 License
This project is open source and available under the MIT License.

### ⭐ Acknowledgments
- Built with **Python** in **Kaggle** and **DeepSeek**
- Dataset from **Vesta** on the **IEEE Fraud Detection** Competition on **Kaggle**
- Visualization powered by **Matplotlib** and **Seaborn**
- Inspired by **credit card fraud detection systems**

### 📧 Contact email: liz21atang@gmail.com
**Elizabeth (Epse Kombe) Atang**: [![LinkedIn](https://upload.wikimedia.org/wikipedia/commons/8/81/LinkedIn_icon.svg)](https://www.linkedin.com/in/elizabeth-atang)

### Project Links: [![GitHub](https://img.shields.io/badge/github-repo-blue?logo=github)](https://github.com/eatangphd/IEEE-CIS-Fraud-Detection)
### [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/code/elizabethatang/catching-financial-fraud-with-machine-learning)

### 📖 References
- IEEE-CIS Competition (https://www.kaggle.com/c/ieee-fraud-detection)
- Synthetic Minority Over-sampling Technique (SMOTE), Chawla et al., 2002. (https://doi.org/10.1613/jair.953)
- Random Forests,  Breiman, 2001. (https://doi.org/10.1023/A:1010933404324)



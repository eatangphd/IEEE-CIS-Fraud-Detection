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

## Challenges and Countermeasures
- **RAM Limitations:** The 30 GB of RAM provided per Kaggle notebook was insufficient to run the full program, and it crashed.
  This was observed primarily when the application of the SMOTE technique was attempted.
- **Down-Sampling:** - To optimize the available space and complete the project, data was downsampled, i.e., not all the data was used.
                    - The parameters for applying the SMOTE technique and Model training were also significantly reduced.
                      For example, k-closest neighbors were reduced to 3 for SMOTE. Model parameters like estimators were reduced to 50, and the depth was set at 10.
## NB: Given the limited memory, the goal of this project was adjusted to complete the project within the available RAM.
To improve results, adjustments to the SMOTE application and model training, together with using all available data, can be made, given there is more RAM to work with.
Because SMOTE creates all these synthetic points to improve class imbalance, there has to be enough memory to accommodate that.
Alternatively, the choice of the Random Forest Classifier can be replaced with an ML model that requires less memory usage like LightGBM or XGBoost

## Results
- **F1-Score:** 0.31
- **Precision:** 0.21 (21% of flagged transactions were actually fraud)
- **Recall:** 0.62 (We caught 62% of all fraud cases)
## Technical Insights for the Metrics
- **Precision (0.21):** Exactly 79% of the fraud alerts are false alarms, meaning investigators will waste nearly 80% of their time reviewing legitimate user accounts.
- **Recall (0.62):** The model leaves a massive security gap by letting exactly 38% of actual fraudsters completely slip through your defenses undetected.
- **F1-Score (0.31):** This heavily penalized score mathematically proves that the model fails to find a healthy, functional compromise between stopping fraud and protecting user experience.

## How to Reproduce
1. Download the data from [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/c/ieee-fraud-detection) or mount the path drive directly from the competition site.
2. Run the preprocessing file from [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/code/elizabethatang/complete-preprocessing-pipeline-function-fraud-dat).
3. Execute the notebook from [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/code/elizabethatang/rf-ml-and-smote-on-limited-ram).


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
### [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/code/elizabethatang/rf-ml-and-smote-on-limited-ram)
### [![Kaggle](https://img.shields.io/badge/Kaggle-IEEE--CIS-20beff.svg)](https://www.kaggle.com/code/elizabethatang/complete-preprocessing-pipeline-function-fraud-dat)


### 📖 References
- IEEE-CIS Competition (https://www.kaggle.com/c/ieee-fraud-detection)
- Synthetic Minority Over-sampling Technique (SMOTE), Chawla et al., 2002. (https://doi.org/10.1613/jair.953)
- Random Forests,  Breiman, 2001. (https://doi.org/10.1023/A:1010933404324)



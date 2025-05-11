# Credit-Card-Fraud-Detection-Using-a-Machine-Learning-Approach

### 1. Introduction

Credit card fraud detection is a critical issue in the financial sector, as fraudulent transactions cause significant financial losses. As technology advances, so do the methods used by fraudsters. Detecting fraudulent transactions has become essential. This project uses machine learning techniques to classify transactions as either genuine or fraudulent based on patterns in the data. We aim to evaluate several machine learning models and determine which performs best on this dataset.

---

### 2. Dataset Description

* **Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
* **Total entries**: 281,167
* **Features**: 31 (including PCA-transformed features V1 to V28)
* **Target column**: `Class`

  * 0 → Genuine transaction (284,315 entries)
  * 1 → Fraudulent transaction (492 entries)

Key features include:

* `Time`: Seconds elapsed between transactions
* `Amount`: Transaction amount
* `Class`: Binary label (0 or 1)

---

### 3. Problem Type

This is a **binary classification problem**, where the goal is to predict whether a transaction is fraudulent (`1`) or not (`0`). As such, classification algorithms are appropriate.

---

### 4. Selected Algorithms

We evaluated and selected the following machine learning algorithms:

#### ✅ Random Forest

* Handles imbalanced data better than simple models
* Reduces overfitting through ensemble learning
* Performs well on both accuracy and recall

#### ❌ Not Selected:

* **Decision Trees**: Prone to overfitting and poor generalization on noisy or imbalanced datasets
* **SVM**: Not suitable for highly imbalanced datasets without significant tuning

---

### 5. Evaluation Summary

| Metric                    | Value    |
| ------------------------- | -------- |
| Train Accuracy            | 100%     |
| Test Accuracy             | 99.98%   |
| Cross-Validation Accuracy | \~80.09% |

> ⚠️ Cross-validation accuracy reveals some overfitting. Improvements can be made by tuning hyperparameters, using resampling techniques (SMOTE, undersampling), or feature engineering.

---

### 6. Related Research paper on this dataset

#### 📚 \[1] Adaptive Machine Learning for Credit Card Fraud Detection (PhD Thesis)
[1] Dal Pozzolo, Andrea, “Adaptive Machine learning for credit card fraud detection” ULB MLG PhD thesis (supervised by G, Bontempi). http://di.ulb.ac.be/map/adalpozz/pdf/Dalpoz-zolo2015PhD.pdf

* Author: Andrea Dal Pozzolo
* Focused on class imbalance handling using undersampling and Random Forest

#### 📚 \[2] Analysis of Credit Card Fraud Detection (2021)
[2] M. K. R. Mallidi and Y. Zagabathuni, "Analysis of credit card fraud detection using machine learning models on balanced and imbalanced datasets," Int. J. Emerging TrendsEng. Res., vol.9, no.7, pp. 846–852, Jul. 2021. https://doi.org/10.30534/ijeter/2021/02972021

* Algorithms tested: LightGBM, AdaBoost, Random Forest
* AdaBoost had highest accuracy (96.13%), LightGBM highest precision (98.68%)

#### 📚 \[3] Credit Card Fraud Detection using ML (IJC-GM 2021)
[3] V. Sellam, P. Tushar, G. Rohit, and S. Sanyam, "Credit card fraud detection using machine learning," Indian Journal of Computer Graphics and Multimedia, vol. 1, no. 1, pp. 16, Feb. 2021. [Online]. Available: www.ijcgm.latticescipub.com. Retrieval Number: A1003011121/2021©LSP.

* Tested Logistic Regression, Random Forest, SVM, Neural Networks
* Random Forest showed the best results

---

### 7. Conclusion

This project demonstrates the effectiveness of machine learning in detecting credit card fraud. Random Forest and Logistic Regression perform well on this dataset, with Random Forest showing high test accuracy. However, the difference between test and cross-validation scores indicates some overfitting, which should be addressed in future work.


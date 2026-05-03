# 🏦 Bank Marketing Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?logo=scikit-learn)
![XGBoost](https://img.shields.io/badge/XGBoost-Ensemble-green)
![SHAP](https://img.shields.io/badge/SHAP-Explainability-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

> Predicting whether a bank customer will subscribe to a **term deposit** using 12 machine learning classifiers — with comprehensive evaluation, statistical testing, and model explainability.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Models Used](#models-used)
- [Evaluation Metrics](#evaluation-metrics)
- [Advanced Analysis](#advanced-analysis)
- [Results](#results)
- [Setup & Installation](#setup--installation)
- [How to Run](#how-to-run)
- [Contributing](#contributing)

---

## 📖 Overview

This project applies **12 machine learning classifiers** to the Bank Marketing dataset to predict term deposit subscriptions. The pipeline includes:

- Data preprocessing and class imbalance handling (SMOTE)
- Training and cross-validation of 12 models
- Multi-criteria model ranking using TOPSIS
- Statistical significance testing via Wilcoxon Signed-Rank Test
- Model explainability using SHAP and LIME

---

## 📊 Dataset

| Property | Detail |
|----------|--------|
| **Source** | [UCI Machine Learning Repository – Bank Marketing](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing) |
| **Instances** | ~45,211 |
| **Features** | 16 (age, job, marital, education, balance, campaign, pdays, etc.) |
| **Target** | `y` — Has the client subscribed to a term deposit? (`yes` / `no`) |
| **Class Imbalance** | ~88% No, ~12% Yes |

---

## 📁 Project Structure

```
Bank_Marketing_Project/
│
├── Code/
│   ├── ML02.ipynb                          # Main ML pipeline (12 classifiers)
│   ├── ML_Result01.ipynb                   # Results analysis & visualization
│   ├── Shap_lime(Best_Models).ipynb        # SHAP & LIME explainability
│   ├── Smote.ipynb                         # Class imbalance handling
│   ├── Topsis_Score_results_of_12_Models.ipynb  # TOPSIS multi-criteria ranking
│   └── Wilcoxon_Signed_Rank_Test.ipynb     # Statistical comparison of models
│
├── Output/
│   ├── mlresult01.xlsx                     # Raw metrics for all models
│   ├── mlresult02.xlsx                     # Extended results
│   ├── Topsis_Score_results_of_12_Models.xlsx   # TOPSIS rankings
│   ├── Smote.xlsx                          # Post-SMOTE results
│   └── Wilcoxon_Signed_Rank_Test_res.xlsx  # Wilcoxon test output
│
├── dataset/                                # Raw and processed data
└── README.md
```

---

## 🤖 Models Used

| # | Model | Type |
|---|-------|------|
| 1 | Logistic Regression | Linear |
| 2 | Decision Tree | Tree-based |
| 3 | Random Forest | Ensemble (Bagging) |
| 4 | Bagging Classifier | Ensemble |
| 5 | Stacking Classifier | Ensemble (Meta) |
| 6 | MLP Classifier | Neural Network |
| 7 | Support Vector Machine (SVC) | Kernel-based |
| 8 | K-Nearest Neighbors | Instance-based |
| 9 | XGBoost | Ensemble (Boosting) |
| 10–12 | Additional variants | Mixed |

---

## 📏 Evaluation Metrics

Each model is evaluated using the following metrics:

- ✅ **Accuracy**
- 🎯 **Precision**
- 🔁 **Recall**
- ⚖️ **F1-Score**
- 📈 **ROC-AUC Score**
- 🧮 **Matthews Correlation Coefficient (MCC)**
- 🤝 **Cohen's Kappa Score**
- 🗂️ **Confusion Matrix**

---

## 🔬 Advanced Analysis

### 🔄 SMOTE (Synthetic Minority Over-sampling Technique)
Addresses the class imbalance problem (~88:12) by generating synthetic samples for the minority class.

### 🏆 TOPSIS (Multi-Criteria Model Ranking)
Ranks all 12 models based on multiple performance metrics simultaneously using the **Technique for Order of Preference by Similarity to Ideal Solution**.

### 📐 Wilcoxon Signed-Rank Test
Non-parametric statistical test to determine if the performance differences between models are **statistically significant**.

### 🔍 SHAP & LIME (Explainability)
- **SHAP** (SHapley Additive exPlanations): Global and local feature importance
- **LIME** (Local Interpretable Model-agnostic Explanations): Individual prediction explanations for the best-performing models

---

## 📋 Results

> Full results are available in the `Output/` directory.

| Model | Accuracy | F1-Score | ROC-AUC | TOPSIS Rank |
|-------|----------|----------|---------|-------------|
| XGBoost | ~91% | ~0.65 | ~0.93 | 🥇 1st |
| Random Forest | ~90% | ~0.63 | ~0.92 | 🥈 2nd |
| Stacking | ~90% | ~0.62 | ~0.91 | 🥉 3rd |
| ... | ... | ... | ... | ... |

> *Exact values available in `Output/mlresult01.xlsx` and `Topsis_Score_results_of_12_Models.xlsx`*

---

## ⚙️ Setup & Installation

### Prerequisites

- Python 3.8+
- pip or conda

### Install Required Libraries

```bash
pip install numpy pandas scikit-learn xgboost imbalanced-learn shap lime matplotlib seaborn openpyxl jupyter
```

Or install all at once:

```bash
pip install -r requirements.txt
```

### Requirements Summary

```
numpy
pandas
scikit-learn
xgboost
imbalanced-learn
shap
lime
matplotlib
seaborn
openpyxl
jupyter
scipy
```

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
Click the **"Open in Colab"** badge inside any notebook file on GitHub.

### Option 2: Local Jupyter

```bash
# Clone the repository
git clone https://github.com/shreyaghora/Bank_Marketing_Project.git
cd Bank_Marketing_Project

# Launch Jupyter
jupyter notebook
```

**Run notebooks in this order:**

1. `Code/Smote.ipynb` — Preprocess & balance data
2. `Code/ML02.ipynb` — Train all 12 models
3. `Code/ML_Result01.ipynb` — Analyze results
4. `Code/Topsis_Score_results_of_12_Models.ipynb` — Rank models
5. `Code/Wilcoxon_Signed_Rank_Test.ipynb` — Statistical testing
6. `Code/Shap_lime(Best_Models).ipynb` — Explain best models

---

## 👥 Contributors
* **Contributor 1 Name** - Shreya ghora
* **Contributor 2 Name** - Abhijit Bera
* **Contributor 3 Name** - Sk Akhmal Hossain
* **Contributor 4 Name** - Purbasa Bhowmick
* **Contributor 5 Name** - Anima Shyamal

---


## 👤 Author

**Shreya Ghora**  
📧 GitHub: [@shreyaghora](https://github.com/shreyaghora)
---


# BACE1 Bioactivity Prediction — Flavonoids

Machine learning pipeline to predict flavonoid compound bioactivity against **BACE1**.

## What this notebook does

1. Data cleaning (missing values, outlier removal, correlated feature removal)
2. Class balancing with **SMOTE**
3. Dimensionality reduction with **PCA**
4. Feature selection with **RFECV**
5. Trains and compares multiple classifiers:
   - Logistic Regression, Decision Tree, Random Forest, XGBoost, SVM, Gradient Boosting
6. Evaluation via ROC/AUC, accuracy, confusion matrices
7. Hyperparameter tuning (**Optuna**) and K-fold cross-validation
8. Screens an external compound database, ranking and exporting top 20/50/100/200 candidate hits

## How to run

### Option 1 — Google Colab (recommended, no setup)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
https://colab.research.google.com/github/praveenpharmaco-gif/betasecretase-flavanoid-bioactivity/blob/main/flavanoids_bace_1.ipynb

### Option 2 — Run locally

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
pip install -r requirements.txt
jupyter notebook
```

## Data files required

- `bsbioactivity_prediction_data1.csv` — included in this repo
- `external_flavonoids_bioactivity_prediction_data.csv` — **too large for GitHub (475 MB)**. Download it from Google Drive here: [external_flavonoids_bioactivity_prediction_data.csv](https://drive.google.com/file/d/1CagFn3YZ9P7HrSmKtNNoswUeorEaohaA/view?usp=sharing), then place it in the same folder as the notebook before running the external-screening section.

## Repository structure

```
├── flavanoids_bace_1.ipynb
├── bsbioactivity_prediction_data1.csv
├── external_flavonoids_bioactivity_prediction_data.csv
├── requirements.txt
└── README.md
```

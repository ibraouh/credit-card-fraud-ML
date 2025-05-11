# credit-card-fraud-ML

**Author:** Ibrahim (Abe) Raouh
**Affiliation:** Fordham University  
**Date:** May 2025

## Overview

This repository contains the code and report for a project on detecting credit-card fraud using supervised ensemble methods and synthetic oversampling. We perform a comprehensive exploratory data analysis (EDA), compare four classifiers (Bagging, Decision Tree, Random Forest, AdaBoost) with and without SMOTE, and identify the best-performing pipeline.

## Data

- **Source:** [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data)
- **Size:** 284,807 transactions, 31 features (28 PCA components, Time, Amount, Class)
- **Class Balance:** 0 = legitimate, 1 = fraud (≈0.17 % fraud)

## Usage

1. **Clone the repo**

   ```bash
   git clone https://github.com/your-username/creditcard-fraud-detection.git
   cd creditcard-fraud-detection
   ```

2. **Install dependencies**
   ```
   pip install -r requirements.txt
   ```
3. **Explore the data**
   Open and run `notebooks/01_data_exploration.ipynb` to reproduce all EDA figures and tables.

4. **Train & evaluate models**
   Open and run `notebooks/02_model_selection.ipynb` to train classifiers with and without SMOTE, view metrics, PR-curves, confusion matrices, and feature importances.

5. **Read the report**
   See `report/creditcard_fraud_report.pdf` for methodology, results, discussion, and conclusions.

6. **View slides**
   See `slides/presentation.pdf` for the 5-minute presentation slides.

## Key Findings
- Best pipeline: RandomForest + SMOTE achieves F1 = 0.878 (Precision 91.2 %, Recall 84.7 %).

- Top features: PCA components V3 and V1, followed by log-Amount and Time.

- EDA insights: Fraud peaks at 02:00–05:00; V3 outliers capture 63 % of fraud in 1.2 % of data.

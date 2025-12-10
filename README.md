# Hybrid-Intrusion-Detection-System-on-UNSW-NB15-Dataset


[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.5-orange)]
[![XGBoost](https://img.shields.io/badge/XGBoost-2.1-brightgreen)]
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)]
[![Dataset](https://img.shields.io/badge/Dataset-UNSW--NB15-success)]()

## Project Overview (Resume & Research Highlights)

- Developed hybrid ML models combining supervised (XGBoost, Random Forest, KNN) and unsupervised (Isolation Forest, KMeans) techniques  
- Integrated feature selection (Mutual Information, RFE, PCA) to handle high-dimensional data and reduce overfitting  
- Addressed class imbalance with SMOTE and balanced sampling for robust generalization  
- Evaluated on UNSW-NB15 dataset, achieving high performance metrics across models  
- Demonstrated significant improvements in attack detection, with top models reaching near-perfect scores (note: perfect 100% may indicate overfitting on training data or specific subsets; further cross-validation recommended)  
- Full pipeline: Data Preprocessing → Feature Engineering → Hybrid Training → Evaluation  

## Model Performance Metrics (UNSW-NB15 Dataset)

| Model                            | Accuracy | Recall   | Precision | F1-Score |
|----------------------------------|----------|----------|-----------|----------|
| **XGBoost**                      | 1.0000   | 1.0000   | 1.0000    | 1.0000   |
| **XGBoost + KMeans**             | 1.0000   | 1.0000   | 1.0000    | 1.0000   |
| Random Forest                    | 0.9999   | 1.0000   | 0.9999    | 0.9999   |
| XGBoost + KNN + KMeans           | 0.9997   | 0.9996   | 0.9999    | 0.9997   |
| RF + KNN + IsolationForest       | 0.9987   | 0.9982   | 0.9992    | 0.9987   |
| KNN                              | 0.9964   | 0.9956   | 0.9972    | 0.9964   |
| RF + IsolationForest             | 0.9411   | 0.8830   | 0.9993    | 0.9375   |
| Isolation Forest                 | 0.5168   | 0.1170   | 0.5886    | 0.1952   |
| KMeans                           | 0.4992   | 0.0000   | 0.0000    | 0.0000   |

**Key Insights:**  
- Supervised models like XGBoost and Random Forest excel with near-perfect metrics, but 100% scores suggest potential overfitting—recommend testing on unseen data.
- Hybrid models enhance generalizability, especially in multi-class attack scenarios.  
- Unsupervised baselines (Isolation Forest, KMeans) underperform alone but boost ensembles when combined.

## ML Pipeline Overview
<img width="602" height="342" alt="image" src="https://github.com/user-attachments/assets/eb2c8efa-a0ef-4854-9b0c-b6c926703814" />

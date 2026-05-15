# Software Quality Analysis Using Machine Learning Models

> **CSE422: Artificial Intelligence** | BRAC University | Fall 2025  
> Section 11 | Group 02
---

## 👥 Group Members

| # | Name | Student ID |
|---|------|------------|
| 1 | Anindita Mahjabin Sristy | 23201073 |
| 2 | Tasmiah Ahmed | 23201517 |

---

## Overview

As software systems grow in size and complexity, manually evaluating code quality becomes increasingly costly and error-prone. This project explores an **automated, data-driven approach** to software quality classification using multiple machine learning techniques.

We analyzed a dataset of software development metrics to classify code quality into three categories- **High**, **Medium**, and **Low** and compared supervised and unsupervised learning approaches.

**Project Report:** https://docs.google.com/document/d/1WvQ2j0TfRAjTFcPs7Wke8g6hrgZ-NuxKndkoa2wUqu8/edit?usp=sharing

---

## Dataset
| Property | Details |
|---|---|
| Total Datapoints | 1,600 |
| Features | 8 |
| Target Variable | `Quality_Label` (High / Medium / Low) |
| Class Distribution | Balanced |

---

## Methodology

- **EDA:** Correlation heatmap, density plots, class distribution analysis
- **Preprocessing:** Null removal, label encoding, MinMaxScaler normalization
- **Supervised:** KNN, Gaussian Naive Bayes, Neural Network (MLP)
- **Unsupervised:** K-Means Clustering (Elbow Method for optimal K)

## Results
| Model | Accuracy | F1 Score |
|---|---|---|
| KNN | 0.32 | Highest |
| Gaussian Naive Bayes | 0.32 | Moderate |
| Neural Network | **0.34** | High |

Evaluation metrics used: Accuracy, F1 Score, Confusion Matrix, ROC Curve & AUC Score

---

## Key Findings

- **Neural Network (MLP)** achieved the highest accuracy, benefiting from its multi-layer architecture with ReLU and Softmax activations
- **KNN** achieved the best F1 score, performing well due to the smaller dataset size
- **Naive Bayes** performed moderately. The feature independence assumption limited its effectiveness on this dataset
- K-Means clustering revealed meaningful natural groupings independent of labels

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)

- **Language:** Python
- **Notebook:** Jupyter Notebook
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn

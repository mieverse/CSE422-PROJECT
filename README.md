# Software Quality Analysis Using Machine Learning Models

**CSE422: Artificial Intelligence** | BRAC University | Fall 2025  
---

## 👥 Group Members
**Group 2 | Section 11**  

| # | Name | Student ID |
|---|------|------------|
| 1 | Tasmiah Ahmed | 23201517 |
| 2 | Anindita Mahjabin Sristy | 23201073 |

---

## Overview

As software systems grow in size and complexity, manually evaluating code quality becomes increasingly costly and error-prone. This project explores an **automated, data-driven approach** to software quality classification using multiple machine learning techniques.

We analyzed a dataset of software development metrics to classify code quality into three categories — **High**, **Medium**, and **Low** — and compared supervised and unsupervised learning approaches.

---

## Dataset

| Property | Details |
|---|---|
| Total Datapoints | 1,600 |
| Features | 8 |
| Target Variable | `Quality_Label` (High / Medium / Low) |
| Class Distribution | Balanced |

**Features include:**
- `Lines_of_Code`, `Cyclomatic_Complexity`, `Number_of_Functions`
- `Code_Churn`, `Comment_Density`, `Number_of_Bugs`
- `Has_Unit_Tests` *(binary: Yes/No)*
- `Code_Owner_Experience`

---

## Methodology

### 1. Exploratory Data Analysis (EDA)
- Visualized class distribution via bar plots and density plots
- Plotted correlation heatmap across numerical features
- Confirmed dataset is balanced and approximately normally distributed

### 2. Data Preprocessing
- Train/Test split: **1,120 / 480** datapoints
- Handled null values in `Lines_of_Code`, `Code_Churn`, `Comment_Density` by dropping incomplete rows
- Encoded categorical features via label mapping
- Applied **MinMaxScaler** for feature normalization
- No features dropped after correlation analysis (no high multicollinearity detected)

### 3. Model Training & Evaluation

#### Supervised Learning
Three classifiers were trained and evaluated:

| Model | Accuracy | Notes |
|---|---|---|
| K-Nearest Neighbors (KNN) | 0.32 | Highest F1 Score |
| Gaussian Naive Bayes | 0.32 | Assumes feature independence |
| Neural Network (MLP) | **0.34** | Best overall accuracy |

Evaluation metrics used: Accuracy, F1 Score, Confusion Matrix, ROC Curve & AUC Score

#### Unsupervised Learning
- Applied **K-Means Clustering** to explore natural groupings in the data
- Used the **Elbow Method** (SSE vs. K) to determine optimal cluster count
- Visualized clusters with centroids across two key features

---

## Key Findings

- **Neural Network (MLP)** achieved the highest accuracy, benefiting from its multi-layer architecture with ReLU and Softmax activations
- **KNN** achieved the best F1 score, performing well due to the smaller dataset size
- **Naive Bayes** performed moderately — the feature independence assumption limited its effectiveness on this dataset
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

---

## Repository Structure

```
📦 software-quality-ml
 ┣ 📓 422_project_Group2.ipynb   # Main notebook (EDA + Models + Evaluation)
 ┣ 📊 dataset/                   # Dataset files
 ┣ 📄 report.pdf                 # Full project report
 ┗ 📄 README.md
```

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/yourusername/software-quality-ml.git
cd software-quality-ml

# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook 422_project_Group2.ipynb
```

---

## Authors

| Name | Student ID |
|---|---|
| Tasmiah Ahmed | 23201517 |
| Anindita Mahjabin Sristy | 23201073 |

> BRAC University, Department of Computer Science and Engineering

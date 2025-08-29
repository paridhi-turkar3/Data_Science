# Exploratory Data Analysis (EDA) - Credit Card Fraud Detection

## 📌 Project Overview
This project focuses on performing **Exploratory Data Analysis (EDA)** on the [Credit Card Fraud Detection dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud).  
The dataset contains transactions made by European cardholders in September 2013, with highly imbalanced classes: fraudulent transactions account for only **0.172%** of all transactions.  

The goal is to analyze, visualize, and summarize the dataset to identify **patterns, trends, and anomalies**.

---

## 📂 Dataset
- File: `creditcard.csv`  
- Rows: 284,807  
- Columns: 31  
- Target column: `Class`  
  - `0` → Non-Fraud  
  - `1` → Fraud  

---

## 🚀 Steps to Reproduce in Google Colab

### 1. Upload Dataset
```python
from google.colab import files
uploaded = files.upload()
```
Upload `creditcard.csv` from your system.

### 2. Import Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
sns.set(style="whitegrid")
```

### 3. Load Dataset
```python
df = pd.read_csv("creditcard.csv")
df.head()
```

### 4. Data Exploration
- Dataset info: `df.info()`
- Statistics: `df.describe()`
- Missing values: `df.isnull().sum()`
- Class distribution: `df['Class'].value_counts(normalize=True)`

### 5. Visualizations
- **Fraud vs Non-Fraud Count**  
- **Transaction Amount Distribution**  
- **Fraud by Time Distribution**  
- **Correlation Heatmap**  
- **Boxplot for Outlier Detection**

### 6. Key Analysis
- Check dataset imbalance  
- Distribution of `Amount` and `Time`  
- Correlation among features  
- Outlier detection in `Amount`  
- Summary statistics grouped by `Class`

---

## 📊 Key Findings
- **Imbalanced Data**: Fraud transactions are less than 0.2%.  
- **No Missing Values**: Dataset is clean.  
- **Fraud Timing**: Fraudulent transactions occur at specific times more frequently.  
- **Correlations**: Features like `V14`, `V17`, etc. show strong correlation with fraud.  
- **Outliers**: Transaction amounts contain extreme values.  

---

## 📁 Deliverables
1. **Jupyter/Colab Notebook** (`EDA_CreditCardFraud.ipynb`)  
2. **EDA Report** (PDF/DOCX)  
3. **README.md** (this file)  

---

## 📌 References
- Kaggle Dataset: [Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- Python Libraries: Pandas, Matplotlib, Seaborn, Plotly  

---

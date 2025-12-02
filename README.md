# 📊 Unlocking Customer Insights: A Statistical Investigation

This repository contains a **Python-based statistical mini-project** performed in **Google Colab**, aimed at uncovering key behavioral patterns from customer transaction data. Using **Pandas, NumPy, Matplotlib, SciPy, and Statsmodels**, this project covers **exploratory data analysis (EDA), visualization, and hypothesis testing** to derive actionable business insights.

> 📁 Data Source: `stats.csv` (10,675 records × 12 columns)  
> 🔧 Environment: Google Colab (Python 3)

---

## 📋 Project Overview

### 🔍 Objective
Understand customer behavior through:
- Descriptive statistics  
- Data visualization  
- Bivariate analysis  
- Statistical hypothesis testing  

### 🧾 Key Questions Answered
- Who is the typical customer?
- How much do they spend?
- Are they active or dormant?
- Do demographics (gender, education, state) influence spending?
- Is there any meaningful relationship between marital status and lifestyle (e.g., pet ownership)?

---

## 🗃️ Dataset Summary

| Feature | Type | Description |
|--------|------|-------------|
| `CustomerID`, `Name` | Categorical | Unique identifiers |
| `Gender`, `Married`, `Education`, `State` | Categorical | Demographic attributes |
| `Age`, `NumPets` | Numeric (Integer) | Lifestyle & personal info |
| `MonthlySpend` | Numeric (Float) | Key metric for analysis |
| `JoinDate`, `TransactionDate` | Datetime | Time-based behavior |
| `DaysSinceLastInteraction` | Numeric | Engagement metric |

- **Total records**: 10,675  
- **No missing values**  
- **High spending variance** → diverse customer segments  

---

## 🔬 Key Statistical Insights

### 1. **Customer Profile**
- Average age: **49 years**  
- Most common: **Male**, **Master’s degree**, **Unmarried**  
- Average monthly spend: **\$331.61** (std = \$225.80)  
- Average last interaction: **538 days ago** → **low engagement**

### 2. **Hypothesis Testing Results**

| Hypothesis | Test Used | Result |
|-----------|----------|--------|
| **Males vs Females spend differently?** | Independent t-test | ❌ Not significant (`p = 0.735`) |
| **Education affects spending?** | One-way ANOVA | ❌ Not significant (`p = 0.922`) |
| **Marital status ↔ Number of pets?** | Chi-square test | ✅ **Significant** (`p < 0.001`) |
| **Older customers less active?** (Age vs DaysSinceLastInteraction) | Pearson correlation | ❌ No correlation (`r = -0.004`) |
| **Spend differs by State?** | One-way ANOVA | ❌ Not significant (`p = 0.346`) |

> 🎯 **Only one significant relationship**: **Marital status is strongly linked to pet ownership**.

---

## 📈 Visualizations Included
- **Histograms**: Age, Monthly Spend  
- **Boxplots**: Outlier detection  
- **Bar Charts**: Gender, Education, State distributions  
- **Scatter Plot**: Age vs Monthly Spend  
- **KDE Plots**: Spending behavior by Education  

*(All visualizations generated using `matplotlib`)*

---

## 🧪 Tools & Libraries Used
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats
import statsmodels.api as sm
from statsmodels.formula.api import ols
```
📌 Business Recommendations
Re-engagement Campaigns Needed
→ 1.5 years average inactivity is a red flag.
Segment by Lifestyle, Not Just Demographics
→ Since gender, education, and state don’t predict spend, focus on behavioral clusters (e.g., unmarried pet owners).
Personalized Offers for High-Variance Spenders
→ Wide spending range ($0–$1500+) suggests room for tiered loyalty programs.

👤 Author
Sonu Kumar
Data Analysis Learner
Affiliated with  Career247 Institute

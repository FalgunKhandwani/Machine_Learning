# Fire Response Time Analysis - EDA and Data Preprocessing

## Project Overview
This project presents an analysis of fire department response times through data preprocessing and exploratory data analysis (EDA).  
The purpose is to understand the key factors that affect how quickly emergency teams respond to incidents.  
Studying these factors helps improve operational planning, allocate resources efficiently, and strengthen public safety systems.

### Problem Statement
Response time is one of the most important performance indicators for emergency services.  
Delays in fire response can lead to higher property damage and increased risk to life.  
The objective of this project is to identify variables that influence response time and to prepare the data for further modeling or prediction tasks.

---

## Dataset Details

| Attribute | Description |
|------------|-------------|
| **Dataset Name** | 2019 Fire Response Time Dataset |
| **Source** | Public Safety / Open Government Data Portal |
| **File Format** | CSV |
| **Size** | Several thousand rows after cleaning |

### Data Cleaning and Preprocessing
- Removed empty or irrelevant rows and columns (`_id`, `Dec`).
- Cleaned the `Response Times` column by replacing inconsistent symbols and text (for example, `<` replaced with “Under”).
- Handled missing values appropriately.
- Converted categorical data into numeric form using One-Hot Encoding.
- Applied the Backward Elimination technique to identify significant variables for analysis.

---

## Methodology

### 1. Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Studied distributions of individual features to understand overall data patterns.  
- **Bivariate Analysis:** Examined relationships between pairs of variables to detect possible dependencies.  
- **Multivariate Analysis:** Used correlation heatmaps and pair plots to explore interactions among multiple features.

### 2. Feature Encoding
Categorical features were encoded using One-Hot Encoding to make them suitable for regression-based or statistical analysis.

### 3. Feature Selection
The Backward Elimination method was used to remove features that did not have a statistically significant impact on response time.  
This step simplifies future modeling while maintaining analytical reliability.

---

## Workflow
```
Raw Data
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Encoding
   ↓
Feature Selection
   ↓
Insights
```

---

## Steps to Run the Code

### Requirements
Install the following Python packages before running the notebook:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

### Execution
1. Download or clone this repository.  
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook ML_assginment.ipynb
   ```
3. Run all cells in sequence to reproduce the analysis.

---

## Experimental Findings

| Analysis Type | Purpose | Observation |
|----------------|----------|--------------|
| Univariate Analysis | To understand individual variable behavior | Identified uneven distributions in response times |
| Bivariate Analysis | To check relationships between variables | Some areas consistently showed longer response durations |
| Multivariate Analysis | To examine combined effects | Found correlations between incident location and response time |
| Backward Elimination | To select significant features | Reduced the number of predictors without losing key information |

### Visualization Outputs
- Distribution plots for response times and incident types.  
- Correlation heatmaps highlighting relationships between variables.  
- Pair plots showing interactions among multiple features.

---

## Conclusion
This analysis demonstrated a structured approach to preparing and exploring fire response data.  
The main findings are:
- Data cleaning and preprocessing are essential for reliable analysis.
- Certain geographic and operational factors strongly influence response times.
- Feature selection using Backward Elimination simplifies the dataset and improves model readiness.

Future work may include developing predictive models for response time estimation and integrating geospatial analysis for location-based insights.

---

## References
- City Open Data Portal – Fire Department Response Records  
- Python Documentation: Pandas, NumPy, Matplotlib, Seaborn, Statsmodels  
- Draper, N. R., & Smith, H. (1998). *Applied Regression Analysis.*

---

### Author
**Falgun Khandwani**  
Machine Learning Assignment – 2025  
Department of Computer Science

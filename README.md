# 👋 Hi there, welcome to my HR Employee Attrition Analysis!

I’m excited you stopped by. This repository walks through a complete exploration of IBM’s HR Employee Attrition dataset from cleaning and visualizations to a predictive model and employee clustering. Feel free to poke around!

---

# HR Employee Attrition Analysis

## Project Overview
This repository contains an end-to-end analysis of the IBM HR Employee Attrition dataset. The goals are to

1. Clean and encode the raw HR data  
2. Explore key factors and visualize relationships  
3. Train and evaluate a predictive model for employee turnover  
4. Uncover natural employee segments via clustering  
5. Outline a deployable machine-learning pipeline and monitoring plan  

## Skills Demonstrated
- Data cleaning and feature engineering (binary encoding, one-hot encoding)  
- Exploratory data analysis and visualization (histograms, boxplots, heatmaps)  
- Supervised learning with logistic regression (model training, cross-validation, ROC/AUC)  
- Unsupervised learning with K-Means clustering (Elbow method, silhouette scores, cluster profiling)  
- Use of Scikit-Learn pipelines for reproducible preprocessing and inference  
- Report writing and business-focused interpretation of results  

## Dataset
The analysis uses the IBM HR Employee Attrition dataset:

- **Filename**: `WA_Fn-UseC_-HR-Employee-Attrition.csv`  
- **Source**: IBM HR Analytics repository on Kaggle  
- **Key columns**:  
  - `Attrition` (Yes/No target)  
  - Demographics: Age, Gender, DistanceFromHome  
  - Job factors: Department, JobRole, BusinessTravel, OverTime  
  - Compensation: MonthlyIncome, PercentSalaryHike  
  - Satisfaction/Engagement scores: JobSatisfaction, EnvironmentSatisfaction, WorkLifeBalance, etc.  
  - Tenure: YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion  

Place the CSV file in a `data/` folder at the root of this repository before running the analysis.

## How to Run
1. **Clone** this repository:
   ```bash
   git clone https://github.com/YourUsername/HR-Attrition-Analysis.git
   cd HR-Attrition-Analysis

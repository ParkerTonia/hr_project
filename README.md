# 👋 Hi there, welcome to my HR Employee Attrition Analysis!

I’m excited you stopped by. This repository walks through a complete exploration of IBM’s HR Employee Attrition dataset—from cleaning and visualizations to a predictive model and employee clustering. Feel free to poke around!

---

## Project Structure


- **data/**  
  Raw CSV file downloaded from IBM’s HR Analytics repository.

- **notebooks/hr_attrition_analysis.ipynb**  
  Jupyter notebook with all steps: cleaning, encoding, EDA, model training & evaluation, clustering, and deployment notes.

- **Parker_Final.pdf**  
  Formatted report that combines code listings, tables, charts, and written interpretation.

## Dataset Overview

| Column                   | Description                                                      |
|--------------------------|------------------------------------------------------------------|
| Attrition                | Target variable: “Yes” if the employee left, “No” otherwise      |
| Age                      | Employee age                                                    |
| BusinessTravel           | Frequency of travel (e.g. “Travel_Rarely”)                       |
| Department               | Department name (Sales, R&D, HR)                                |
| DistanceFromHome         | Distance to office in miles                                      |
| MonthlyIncome            | Monthly salary                                                   |
| OverTime                 | “Yes”/“No” indicator                                             |
| …                        | …                                                                |

Full schema in the notebook.

## Methodology

1. **Data Cleaning & Encoding**  
   - Converted “Yes”/“No” to binary (1/0).  
   - One-hot encoded categorical fields (JobRole, Department, etc.).

2. **Exploratory Data Analysis**  
   - Histograms and boxplots for numerical variables.  
   - Bar charts of attrition rates by gender, department, and overtime status.  
   - Correlation heatmap to identify strong predictors.

3. **Predictive Modeling**  
   - Split data (70% train / 30% test).  
   - Trained Logistic Regression to predict attrition.  
   - Evaluated with accuracy, confusion matrix, precision, recall, F1, and ROC AUC.

4. **Unsupervised Clustering**  
   - Scaled selected features (satisfaction, involvement, etc.).  
   - Used Elbow Method and silhouette scores to choose k.  
   - Fitted K-Means and profiled each cluster’s demographics and attrition rates.

5. **Deployment Plan**  
   - Built a Scikit-Learn `Pipeline` for preprocessing + prediction.  
   - Recommended quarterly retraining and drift monitoring.

## Key Results

| Metric    | Score |
|-----------|-------|
| Accuracy  | 0.85  |
| Precision | 0.62  |
| Recall    | 0.78  |
| F1 Score  | 0.69  |
| AUC       | 0.90  |

Confusion matrix and ROC curve are in the notebook. Clustering uncovered three segments:
1. Highly engaged, low-risk  
2. Moderately engaged, medium-risk  
3. Low engagement, high-risk  

## How to Reproduce

1. Clone this repo.  
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn notebook

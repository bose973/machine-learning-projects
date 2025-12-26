# Employee Turnover Analytics

## 📌 Project Overview
Portobello Tech aims to predict employee turnover using machine learning. The HR Department owns the data and leverages it to identify patterns in employee satisfaction, evaluation, workload, and promotions. This project builds predictive models, evaluates them, and suggests retention strategies based on risk zones.

## 🎯 Objectives
- Perform data quality checks (missing values, anomalies).
- Conduct exploratory data analysis (EDA) to identify turnover drivers.
- Visualize correlations and distributions of key features.
- Cluster employees who left based on satisfaction and evaluation.
- Handle class imbalance using SMOTE.
- Train and evaluate models with 5‑fold cross‑validation.
- Compare Logistic Regression, Random Forest, and Gradient Boosting.
- Select the best model using ROC/AUC, confusion matrix, and classification metrics.
- Suggest retention strategies based on predicted turnover risk zones.

## 📊 Dataset
Source: [Kaggle HR Dataset](https://www.kaggle.com/liujiaqi/hr-comma-sepcsv)

### Columns
- **satisfaction_level**: Employee job satisfaction (0–1).
- **last_evaluation**: Last performance evaluation score (0–1).
- **number_project**: Number of projects handled.
- **average_montly_hours**: Average monthly working hours.
- **time_spend_company**: Years spent in the company.
- **Work_accident**: Accident occurrence (0/1).
- **left**: Employee turnover (0 = stayed, 1 = left).
- **promotion_last_5years**: Promotions received in last 5 years.
- **Department**: Employee department.
- **salary**: Salary level.

## 🛠️ Methodology
1. **Data Quality Checks**: Identify missing values and inconsistencies.
2. **EDA & Visualization**:
   - Heatmap of correlations.
   - Distribution plots for satisfaction, evaluation, monthly hours.
   - Bar plots for project count vs. turnover.
3. **Clustering**:
   - K‑Means clustering of employees who left (3 clusters).
   - Analysis of satisfaction vs. evaluation patterns.
4. **Preprocessing**:
   - Encode categorical variables with `get_dummies()`.
   - Stratified train/test split (80:20).
   - Apply SMOTE to balance classes.
5. **Model Training**:
   - Logistic Regression
   - Random Forest Classifier
   - Gradient Boosting Classifier
   - 5‑fold cross‑validation applied to each.
6. **Evaluation**:
   - Classification reports
   - ROC/AUC curves
   - Confusion matrices (focus on Recall vs. Precision trade‑off).
7. **Retention Strategy**:
   - Predict turnover probabilities.
   - Categorize employees into zones:
     - **Safe Zone (Green)**: <20%
     - **Low‑Risk Zone (Yellow)**: 20–60%
     - **Medium‑Risk Zone (Orange)**: 60–90%
     - **High‑Risk Zone (Red)**: >90%
   - Suggest tailored retention strategies for each zone.

## 📈 Results
- Identified key drivers of turnover (satisfaction, evaluation, workload).
- Best model selected based on ROC/AUC and Recall emphasis.
- Risk zones defined for actionable HR strategies.

## 🚀 How to Run
1. Clone the repository:
   git clone https://github.com/bose973/machine-learning-projects.git
2. Make sure python 3.12.1 is installed in your system
3. Navigate to the project folder:
   cd machine-learning-projects/Employee_Turnover_Analytics
4. Create the virtual env - run these two commands step by step:
   1)python -m venv ML_ENV
   2)pip install -r ./machine-learning-projects/Employee_Turnover_Analytics/required_packages.txt
5. Update the python interpretor of your IDE to ML_ENV
6. Run the project-code file using jupyter editor in your IDE:
   analytics_model.ipynb

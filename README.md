# Employee-Attrition-Prediction-Using-Machine Learning

This project applies machine learning techniques to predict employee attrition and uncover key drivers behind employee turnover. By leveraging historical HR data, the model empowers organizations to implement proactive, data-driven retention strategies.

---

## 👨‍💼 Project Overview

**Objective:**  
Predict whether an employee is likely to leave ("Attrition: Yes") based on demographic, compensation, and job-related features.

**Business Goals:**
- Reduce recruitment and training costs due to turnover
- Retain top-performing employees
- Use data to guide HR interventions
- Improve employee satisfaction and productivity

---

## 🧰 Tools & Technologies Used

- 📊 **Tools:** Orange Tool, Microsoft Excel
- 🐍 **Languages & Libraries (under the hood):** Python, Pandas, Scikit-learn (assumed)
- 📈 **ML Models:** Logistic Regression, Random Forest, Decision Tree, SVM, k-NN, Neural Network
- 📚 **Dataset Source:** [Kaggle - HR Employee Attrition Dataset](https://www.kaggle.com/datasets/patelprashant/employee-attrition)

---

## 📦 Dataset Description

- **Records:** 1470 employee records
- **Target Variable:** `Attrition` (Yes / No)
- **Features:** 35, including:
  - Demographics (Age, Gender, MaritalStatus)
  - Compensation (MonthlyIncome, StockOptionLevel)
  - Job & Performance (JobRole, EnvironmentSatisfaction, OverTime)
  - Work-Life Balance (DistanceFromHome, YearsAtCompany, etc.)

---

## 🔍 Key Insights (EDA)

- Attrition rate: 16.1%
- Higher attrition among:
  - Younger employees (28–39)
  - Employees with frequent travel
  - Those working overtime
  - Lower income and long commute
- OverTime was a top predictive feature

---

## 🧹 Data Preprocessing

- ✅ No missing values
- 🔠 Categorical Encoding: One-hot + Binary
- 📏 Normalization: Min-Max scaling for numerical features
- ⚖️ Class Imbalance handled via:
  - Stratified splitting
  - Emphasis on Recall, F1-Score, and ROC-AUC during evaluation
- 🧼 Dropped uninformative features like `Over18`, `EmployeeCount`, etc.

---

## 🤖 Machine Learning Models & Results

| Model              | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Logistic Regression| 83%      | 76%       | 71%    | 73%      | 0.82    |
| Random Forest      | 86%      | 79%       | 76%    | 77%      | 0.88    |
| SVM                | 84%      | 77%       | 74%    | 75%      | 0.84    |
| Neural Network     | 85%      | 78%       | 75%    | 76%      | 0.87    |
| Decision Tree      | 82%      | 74%       | 70%    | 72%      | 0.79    |
| k-NN               | Poor     | Low       | Low    | Low      | < 0.75  |

🏆 **Best Model:** Logistic Regression  
✅ High interpretability  
✅ Balanced metrics  
✅ Suitable for real-world deployment in HR dashboards

---

## 📤 Deployment Strategy

- Input: Employee attributes (e.g., Age, OverTime, MonthlyIncome)
- Output:
  - `Attrition (Yes/No)`
  - Risk probability
  - Top contributing factors
- Deployment options:
  - Web dashboard
  - Excel plugin for HR
  - API integration with internal HR tools
- Monitoring: Ongoing model evaluation + retraining

---

## 📈 CRISP-DM Methodology Followed

1. **Business Understanding**
2. **Data Understanding**
3. **Data Preparation**
4. **Modeling**
5. **Evaluation**
6. **Deployment**

---

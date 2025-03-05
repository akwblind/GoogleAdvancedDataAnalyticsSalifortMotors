# **Google Advanced Data Analytics: Salifort Motors**
## **Predictive Modeling Employee Retention Project for Salifort Motors**

### **Project Overview**
In this capstone project, I assumed the role of a **data analytics professional** at **Salifort Motors**, a fictitious large consulting firm, tasked with predicting **employee attrition**. Employee retention is a key concern for Salifort Motors, as high turnover rates can lead to significant financial and operational disruptions.

The primary objective of this project was to develop a **predictive model** that accurately identifies employees at risk of leaving the company. Utilizing a dataset provided by the **HR department** (originally sourced from Google's capstone data), I conducted a thorough analysis to uncover the underlying factors contributing to employee attrition.

---

### **Business Understanding**
The primary stakeholder for this project is the **HR department**, who has tasked me with developing a predictive model. In a real-world scenario, additional stakeholders would include individuals from the **data department** (e.g., managers, directors, and senior analysts) and key **leadership positions** within the company.

---

### **Business Problem & Objective**
As a **data specialist** at Salifort Motors, I was provided with the results of a recent **employee survey**. The senior leadership team tasked me with analyzing the data to identify strategies for increasing employee retention. To support this goal, I was asked to design a **predictive model** that forecasts whether an employee will leave the company based on factors such as:
- **Department**
- **Number of projects**
- **Average monthly hours**

---

### **Data Understanding**
This dataset, provided by **Google** as part of their **Advanced Data Analytics program**, is sourced from [Kaggle](https://tinyurl.com/bdz53xa4). It consists of:
- **15,000 rows**
- **10 columns**
Containing a mix of **numeric variables** and **two categorical ones**.

---

#### **Data Limitations**
- **Dataset Size**: The relatively small sample size limited the ability to train a highly accurate machine learning model.
- **Duplicate Rows**: The dataset contains **3,008 duplicate rows**, accounting for roughly **20%** of the total dataset. This redundancy impacts the quality and accuracy of the model.

---

### **Modeling and Evaluation**
For this project, I chose to use a **random forest model** instead of a **logistic regression** or **decision tree**. Random forest models (and **XGBoost**) tend to offer greater accuracy by capturing complex patterns and reducing overfitting. I performed an **80/20 train/test split**.

#### **Metrics (Including Confusion Matrix):**
- **Accuracy**: 0.9712
- **Precision**: 0.9439
- **Recall**: 0.8803
- **F1 Score**: 0.9110
- **AUC**: 0.9666

<img src="https://github.com/user-attachments/assets/c5b2b341-5ea4-4bb6-a712-4740ca3ee10e" width="500"/>

#### **Feature Importance:**
The most important features contributing to the model's performance were as follows:
- **average_monthly_hours**: 0.278368
- **number_project**: 0.273847
- **tenure**: 0.194619
- **last_evaluation**: 0.190324
- **salary**: 0.018632
- **work_accident**: 0.011036
  
<img src="https://github.com/user-attachments/assets/25789879-95a0-469e-bc07-a98925d0a5e8" width="600"/>

#### **Analysis:**
The model performed well across all metrics, with the lowest being recall. Specifically, the model:
- Correctly predicted **97.12%** of employees who stayed and left.
- Identified **94.39%** of those likely to leave.
- Flagged **88.03%** of actual departures.

The most important features influencing these results were:
- **average_monthly_hours** (hours worked per month)
- **number_project** (number of projects an employee worked on)
- **tenure** (years at the company)
- **last_evaluation** (evaluation score)

---

### **Conclusion**
Given the model's performance, I recommend several strategies to improve employee retention:
- **Manage Work Hours**: Assess the necessity of long working hours and consider reducing expectations for employees to improve work-life balance.
- **Offer Flexible Working Arrangements**: Provide more options for flexible work arrangements to reduce time spent at the office and improve overall satisfaction.
- **Adjust Compensation Structure**: Establish a clearer and more transparent compensation structure to enhance employee retention.
- **Limit Project Load**: Restrict the number of projects assigned to each employee, as those involved in **seven projects** had all left the company.
- **Leadership Development for Tenured Employees**: Offer long-tenured employees opportunities for leadership development to foster loyalty and growth within the company.

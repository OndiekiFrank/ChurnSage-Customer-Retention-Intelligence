# ChurnSage: Customer Retention Intelligence



![Threshold Tuning](images/WhatsApp%20Image%202025-07-21%20at%2012.38.10%20(1).jpeg)

## 📌 Project Overview

ChurnSage is a machine learning-powered solution designed to **predict customer churn** with high accuracy and provide **data-driven strategies** to improve customer retention. This project leverages Python, Scikit-learn, and visual analytics to turn raw customer data into actionable business insights.

---

## 🎯 Objectives

- Predict which customers are likely to churn.
- Understand the key factors driving churn.
- Tune model performance using statistical methods and machine learning best practices.
- Provide actionable insights and recommendations for retention.

---

## 📊 Business Context

Customer churn significantly impacts profitability. Proactively identifying customers likely to leave helps businesses focus their efforts on retention, which is **5–25 times cheaper** than acquiring new customers. This project serves as an analytical foundation for a **Churn Prediction System**.

---

## 🧠 Machine Learning Workflow

### 1. Data Understanding
- Loaded and explored telecom customer data.
- Conducted completeness checks and assessed class distribution.

### 2. Data Preparation
- Handled missing values and outliers.
- Encoded categorical variables and scaled numerical features.

### 3. Exploratory Data Analysis (EDA)
- Analyzed customer demographics, service usage, and churn trends.
- Created visualizations to discover patterns.

### 4. Statistical Analysis
- Performed t-tests and correlation analysis to assess feature relevance.
- Tuned decision thresholds for optimal performance.

### 5. Modeling
- Trained and evaluated multiple models:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - Gradient Boosting (Best Performing)
- Used pipelines and cross-validation for robust results.

### 6. Threshold Tuning
- Tuned classification thresholds to improve F1-score.
- Optimized for both **business impact** and **model sensitivity**.


---

## 🏆 Final Model Performance (Gradient Boosting)

- **Accuracy**: 94%
- **Precision (Churn)**: 84%
- **Recall (Churn)**: 74%
- **Best Threshold**: 0.30

> Balanced performance ensures both **reliable churn detection** and **minimal false positives**, which is crucial in a business setting.

---

## 📈 Key Insights

![Churn Insight](images/WhatsApp%20Image%202025-07-21%20at%2012.38.10.jpeg)

- Customers on **month-to-month contracts**, **without tech support**, or with **high monthly charges** were more likely to churn.
- Contract type, internet service, and tenure length were significant predictors.
- Optimizing the threshold to 0.30 improved the detection of churners with minimal drop in precision.

---

## 💡 Recommendations

- **Offer loyalty incentives** for customers on month-to-month plans.
- Promote **bundled packages** that include tech support and longer contracts.
- Create **targeted marketing campaigns** based on churn risk segments.
- Establish a **churn dashboard** using these insights to monitor trends in real time.

---

## 📁 Project Structure

ChurnSage-Customer-Retention-Intelligence/
│
├── data/ # Raw and cleaned datasets
├── images/ # Visuals used in notebook and README
├── notebooks/ # Main Jupyter Notebook
├── models/ # Saved models (if applicable)
├── requirements.txt # Project dependencies
└── README.md # Project documentation


---

## 🛠️ Tools & Technologies

- Python, NumPy, Pandas
- Scikit-learn, Matplotlib, Seaborn
- Jupyter Notebook
- Git & GitHub

---

## 📚 How to Run

```bash
git clone https://github.com/OndiekiFrank/ChurnSage-Customer-Retention-Intelligence.git
cd ChurnSage-Customer-Retention-Intelligence
pip install -r requirements.txt
jupyter notebook

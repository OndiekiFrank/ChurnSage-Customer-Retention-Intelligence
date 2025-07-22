# ChurnSage: Customer Retention Intelligence



![Threshold Tuning](images/WhatsApp%20Image%202025-07-21%20at%2012.38.10%20(1).jpeg)

##  Project Overview

ChurnSage is a machine learning-powered solution designed to **predict customer churn** with high accuracy and provide **data-driven strategies** to improve customer retention. This project leverages Python, Scikit-learn, and visual analytics to turn raw customer data into actionable business insights.

---

##  Objectives

- Predict which customers are likely to churn.
- Understand the key factors driving churn.
- Tune model performance using statistical methods and machine learning best practices.
- Provide actionable insights and recommendations for retention.

---

##  Business Context

Customer churn significantly impacts profitability. Proactively identifying customers likely to leave helps businesses focus their efforts on retention, which is **5–25 times cheaper** than acquiring new customers. This project serves as an analytical foundation for a **Churn Prediction System**.

---
##  Project Structure

```plaintext
ChurnSage-Customer-Retention-Intelligence/
│
├── data/ # Raw and cleaned datasets
├── images/ # Visuals used in notebook and README
├── notebooks/ # Main Jupyter Notebook
├── models/ # Saved models (if applicable)
├── requirements.txt # Project dependencies
└── README.md # Project documentation
```

---

##  Machine Learning Workflow

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

##  Final Model Performance (Gradient Boosting)

- **Accuracy**: 94%
- **Precision (Churn)**: 84%
- **Recall (Churn)**: 74%
- **Best Threshold**: 0.30

> Balanced performance ensures both **reliable churn detection** and **minimal false positives**, which is crucial in a business setting.

---

## Key Insights

![Churn Insight](images/WhatsApp%20Image%202025-07-21%20at%2012.38.10.jpeg)

###  Final Insights

After thorough preprocessing, feature engineering, and model experimentation, the following key insights emerged from my churn analysis:

---

###  1. Churn Behavior is Influenced by Key Features:
- **Customer Service Calls**: Customers with **4 or more service calls** have a high churn rate.
- **International Plan**: Subscribing to an international plan is strongly associated with churn.
- **Total Day Minutes** and **Total Charge Metrics** show strong predictive power.

---

###  2. Model Performance Summary:

| Model                     | Accuracy | Recall (Churn) | Precision (Churn) | F1 Score (Churn) |
|---------------------------|----------|----------------|-------------------|------------------|
| Logistic Regression       | 86%      | 0.42           | 0.60              | 0.49             |
| K-Nearest Neighbors       | 88%      | 0.22           | 0.67              | 0.33             |
| Decision Tree             | 91%      | 0.52           | 0.80              | 0.63             |
| Random Forest             | 92%      | 0.56           | 0.86              | 0.68             |
| Gradient Boosting         | 93%      | 0.61           | 0.88              | 0.72             |
| Voting Classifier         | 88%      | 0.20           | 0.95              | 0.33             |
| **Gradient Boosting (Threshold = 0.30)** | **94%** | **0.74**       | **0.84**         | **0.79**         |

 **Gradient Boosting with Threshold Tuning** provided the best balance between sensitivity (recall) and specificity.

---

###  . Threshold Tuning Enhanced Churn Detection:
- Default thresholds (0.5) underperform for the minority churn class.
- Lowering the threshold to **0.30** improved recall from **0.61 to 0.74** while maintaining high accuracy (94%).

---

##  Final Recommendations

Based on my comprehensive analysis, I recommend the following strategic actions:

---

###  1. **Focus on Customer Service Experience**
- Implement proactive retention campaigns targeting customers with **frequent customer service interactions**.
- Use sentiment analysis on support interactions to detect churn signals early.

---

###  2. **Review International Plan Offering**
- The **international plan** is a red flag for churn.
- Investigate whether pricing, quality, or satisfaction issues exist with this plan.
- Consider offering personalized plans or incentives to improve satisfaction.

---

###  3. **Monitor High-Usage Customers**
- Customers with **high day-time call minutes** and **charges** tend to churn more.
- Consider targeted loyalty programs for these high-value customers.

---

###  4. **Deploy the Optimized Gradient Boosting Model**
- Integrate the **GBM with threshold tuning (0.30)** into the company’s CRM.
- Monitor its predictions weekly and continuously refine based on new data.

---

###  5. **Address Class Imbalance**
- Future modeling efforts should explore:
  - **SMOTE (Synthetic Minority Over-sampling Technique)**
  - **Class weight adjustments**
  - **Ensemble models optimized for imbalance**

---

### 6. **Continue Model Monitoring and Re-training**
- Churn behavior may evolve over time.
- Retrain models quarterly with updated data to retain accuracy and relevance.


---
## Interactive Dashboard

Explore the interactive Tableau dashboard for more churn insights and visualizations:

🔗 [View on Tableau](https://public.tableau.com/app/profile/frankline.ondieki/viz/Customerchurn_17531429110990/Dashboard1?publish=yes)

---

## Environment Setup (with Conda)

This project uses Conda environments for reproducibility across platforms. To replicate the setup:

### Step-by-Step Instructions

1. **Install Conda**:  
   [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution)

2. **Clone the repository**:
   ```bash
   git clone https://github.com/OndiekiFrank/ChurnSage-Customer-Retention-Intelligence.git
   cd ChurnSage-Customer-Retention-Intelligence
   ```

## ⚙️ Setup Instructions with Conda

### Choose the Right Conda Environment File

Inside the `churnsage-envs/` folder, select the appropriate environment file based on your operating system:

| Operating System      | YAML File                     |
|-----------------------|-------------------------------|
| Ubuntu/Linux          | `ubuntu_environment.yml`      |
| Windows               | `win_environment.yml`         |
| macOS (CPU only)      | `mac_environment.yml`         |
| macOS (GPU support)   | `mac_environment_tf.yml`      |

---

### Create and Activate the Conda Environment

```bash
conda env create -f churnsage-envs/ubuntu_environment.yml
conda activate learn-env
```
Launch the notebook:
```bash
jupyter notebook
```
---

### Option 2: Using conda (recommended)

```bash
git clone https://github.com/OndiekiFrank/ChurnSage-Customer-Retention-Intelligence.git
cd ChurnSage-Customer-Retention-Intelligence
pip install -r requirements.tx
```
## Tools & Technologies

- Python, NumPy, Pandas
- Scikit-learn, Matplotlib, Seaborn
- Jupyter Notebook
- Git & GitHub

---

##  Author

**Frankline Ondieki Ombachi**  
*Machine Learning Engineer | DevOps Engineer | Data Scientist*  
[LinkedIn](https://www.linkedin.com/in/frankline-ondieki-39a61828a/) | [GitHub](https://github.com/OndiekiFrank)

---

##  License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for full details.

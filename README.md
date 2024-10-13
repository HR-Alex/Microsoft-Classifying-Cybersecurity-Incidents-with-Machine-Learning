# Microsoft-Classifying-Cybersecurity-Incidents-with-Machine-Learning

## 📂 Project Overview

This project aims to assist Security Operations Centers (SOCs) by developing a machine learning model to predict triage grades for cybersecurity incidents. The model classifies incidents into **True Positive (TP)**, **Benign Positive (BP)**, and **False Positive (FP)** categories using the **GUIDE** dataset from Microsoft. The model helps SOC analysts make quicker, data-driven decisions, improving threat detection and response times.

---

## 🎯 Project Scope

Our machine learning pipeline consists of:

1. **Data Exploration & Preprocessing**: Conduct exploratory analysis, handle missing data, and apply feature engineering.
2. **Model Development**: Build classification models, starting with baselines and advancing to models like Random Forest and XGBoost.
3. **Evaluation & Interpretation**: Assess performance using metrics like **Accuracy**, **Macro-F1 score**, **Precision**, **Recall**, and the **Confusion Matrix**.

---

## 🧠 Problem Statement

The project seeks to automate the triage process by building a model that accurately classifies cybersecurity incidents, aiming to reduce false positives and ensure that critical threats are prioritized.

---

## 💡 Dataset Overview

The dataset contains more than 9.5 million rows, divided into **70% training** and **30% test data**. The data is structured into **three levels**: 

1. **Evidence Level** (IP, email, user info),
2. **Alert Level** (potential incidents), and 
3. **Incident Level** (comprehensive threats).

---

## 📊 Metrics

We evaluate the model using the following metrics:

- **Accuracy**: Measures overall correctness.
- **Macro-F1 Score**: Balances performance across all classes.
- **Precision**: Evaluates correct positive predictions.
- **Recall**: Measures the ability to capture relevant positive cases.
- **Confusion Matrix**: Visualizes classification performance.

---

## 🛡️ Business Use Cases

- **SOCs**: Automate incident triage for faster, data-driven responses.
- **Incident Response Automation**: Suggest actions based on classification.
- **Threat Intelligence**: Enhance detection accuracy using historical data.
- **Enterprise Security**: Improve response to true threats while reducing false positives.

---

## 🛠️ Approach

### 1. Data Exploration and Preprocessing
- **EDA**: Investigated feature distributions, target class balance, and correlations.
- **Missing Data Handling**: Applied imputation, removal, and model-based techniques.
- **Feature Engineering**: Created new features, such as timestamps, and encoded categorical variables.
  
### 2. Model Selection and Training
- **Baseline Models**: Logistic Regression and Decision Tree classifiers provided a performance benchmark.
- **Advanced Models**: Random Forest and XGBoost were explored for improved accuracy, although the tuned Decision Tree outperformed them.
  
### 3. Model Evaluation and Tuning
- **Performance Metrics**: Evaluated using accuracy, macro-F1, precision, and recall. Decision Tree showed the best results.
- **Hyperparameter Tuning**: Applied grid search to optimize model performance, with the tuned Decision Tree offering slight improvements.

---

## 🔍 Model Comparison

| **Model**                       | **Accuracy** | **Macro-F1** | **Precision** | **Recall** |
|----------------------------------|--------------|--------------|---------------|------------|
| Random Forest                    | 0.498        | 0.347        | 0.679         | 0.411      |
| XGBoost                          | 0.621        | 0.571        | 0.694         | 0.563      |
| Logistic Regression              | 0.433        | 0.239        | 0.272         | 0.352      |
| Decision Tree (Before Tuning)    | 0.807        | 0.790        | 0.797         | 0.786      |
| **Decision Tree (After Tuning)** | **0.808**    | **0.791**    | **0.798**     | **0.787**  |

The **Decision Tree Classifier** (after tuning) achieved the best accuracy and overall performance across all metrics.

---

## 📚 Recommendations

1. **Integration into SOC Workflows**: Embed the model into SIEM systems for automated alert prioritization.
2. **Future Improvements**: Address class imbalance, explore additional features, and improve model interpretability.
3. **Deployment Considerations**: Ensure model scalability, security, and operational readiness.

---

## 🏆 Results

The **Decision Tree Classifier**, after hyperparameter tuning, achieved an **accuracy of 80.8%** with strong performance across other metrics. This machine learning model offers a powerful tool for automating cybersecurity incident triage, ensuring quicker, more accurate decisions in threat management.

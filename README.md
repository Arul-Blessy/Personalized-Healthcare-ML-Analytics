# 🏥 Personalized Healthcare Recommendations System

## 📌 Project Overview
This project leverages **Machine Learning** to provide automated healthcare advice based on blood transfusion history and hematological indicators. By analyzing patient patterns, the system identifies individuals who may require medical follow-ups or specific lifestyle interventions.

* **Domain:** Healthcare Data Analytics
* **Technologies:** Python, Scikit-Learn, Random Forest
* **Level:** Advanced

---

## 📊 Data Insights & Visualizations

### 1. Feature Correlation
Understanding how different health metrics relate to each other is crucial. The heatmap below shows the relationship between Recency, Frequency, Monetary, and Time.

<img width="1000" height="600" alt="heatmap" src="https://github.com/user-attachments/assets/433d2ba5-839c-4548-b187-325aa01be967" />

### 2. Recommendation Distribution
The following chart displays the balance of our target classes within the dataset, helping us understand the frequency of healthcare recommendations generated.

<img width="800" height="500" alt="distribution" src="https://github.com/user-attachments/assets/3637fb07-405c-49df-9cf0-c31cdf70a4ce" />

---

## ⚙️ Methodology

### Data Preprocessing
To ensure model accuracy, I implemented a robust preprocessing pipeline:
* **Data Cleaning:** Checked for null values and verified data types.
* **Feature Scaling:** Applied `StandardScaler` to normalize features like 'Monetary' and 'Time', preventing larger values from dominating the model logic.

### Machine Learning Model
I utilized a **Random Forest Classifier**. Unlike simple models, Random Forest creates multiple decision trees and merges them together to get a more accurate and stable prediction, which is vital in a healthcare context.

### Performance Evaluation
The model was tested using a 20% data split. Key metrics include:
* **Precision:** How accurate the "Recommendation" predictions are.
* **Recall:** How well the model catches all patients needing advice.
* **F1-Score:** The balance between Precision and Recall.

---

## 💡 Personalized Recommendations Logic
The system maps the model's numerical output into actionable human-readable advice:

| Prediction | Status | Healthcare Advice |
| :--- | :--- | :--- |
| **Class 0** | Normal | No immediate action needed. Continue routine monitoring. |
| **Class 1** | Follow-up | **Recommendation:** Scheduled health check-up or blood screening is advised. |

---

## 🚀 How to Run the Project
1. Clone this repository.
2. Ensure you have the following libraries installed: `pandas`, `seaborn`, `matplotlib`, `scikit-learn`.
3. Open `Healthcare_recommendation.ipynb` in VS Code or Jupyter Notebook.
4. Run all cells to see the analysis and prediction engine in action.

---
*Developed for the Unified Mentor Internship Program.*

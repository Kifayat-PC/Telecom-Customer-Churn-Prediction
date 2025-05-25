# 📉 Telco Customer Churn Prediction  
## 💡 Smart Churn Risk Modeling for Telecom Businesses

A machine learning project focused on predicting customer churn in the telecom sector. The aim is to help businesses proactively identify customers at risk of leaving and take early retention action.

---

### 🌟 Project Highlights

#### 🔍 Business Context  
In the competitive telecom industry, retaining existing customers is far more cost-effective than acquiring new ones. This project builds a churn prediction system using machine learning to:  
- Detect early signs of churn  
- Enable targeted retention campaigns  
- Reduce customer loss and revenue drop  

---

### 📂 Dataset Overview  
- **Source:** Telco Customer Churn Dataset  
- **Size:** 7,043 customer records with 21 features  
- **Target Variable:** Churn (Yes / No)  

---

### 🧠 Machine Learning Pipeline

#### 🔹 Preprocessing & Feature Engineering  
- Removed irrelevant columns (e.g., `customerID`)  
- Cleaned invalid entries in `TotalCharges`  
- Engineered meaningful features:  
  - `AvgMonthlySpend`  
  - `HasStreaming`  
  - `EngagementScore`  
  - `IsLongTermContract`  
- Label encoded all categorical variables  

#### 🔹 Sampling Strategy  
- Applied **SMOTE + Tomek Links** to balance the dataset and reduce bias  

#### 🔹 Modeling Techniques  
Trained multiple classifiers:  
- Decision Tree  
- Random Forest (**Best baseline model**)  
- XGBoost  
- Soft Voting Ensemble  

#### 🔹 Evaluation Metrics  
- Accuracy  
- Recall (with a special focus on churners)  
- ROC-AUC, PR-AUC  
- Confusion Matrix  
- Classification Report  

---

### 🧪 Performance Summary

| Model                      | Accuracy | Recall (Churn) | ROC-AUC |
|----------------------------|----------|----------------|---------|
| Random Forest (default)    | ~78%     | ~63%           | ~0.84   |
| Weighted RF Classifier     | ~79%     | ~66%           | ~0.86   |
| Threshold Tuned Model (0.35) | ~74%  | 78%            | ~0.88   |
| Soft Voting Ensemble       | ~78%     | ~68%           | ~0.85   |

---

### 🛠 Improvements Implemented  
- 🔁 SMOTE + Tomek for balancing  
- ⚖️ Cost-sensitive learning with class weights  
- 🎯 Threshold tuning for optimizing recall  
- 🔗 Ensemble voting classifier for robustness  

---

### 📈 Visual Insights  
- Correlation Heatmaps  
- Boxplots & Histograms for numeric distributions  
- Confusion Matrices  
- ROC and Precision-Recall Curves  
- Recall vs Threshold tuning plots  

---

### 💾 Model Artifacts  
- `final_model.pkl`: Default Random Forest model  
- `improved_churn_model.pkl`: Recall-optimized Random Forest (weighted)  
- `encoders.pkl`: Label encoders for categorical features  

All models saved using pickle for deployment ease  

---

### 🚀 Deployment Options  
This churn model can be deployed via:  
- Flask/FastAPI for REST APIs  
- Streamlit or Gradio for interactive dashboards  
- Integration with CRM systems to automate retention strategies  

---

### 📚 What I Learned  
- Effective use of feature engineering and domain insights in churn prediction  
- Advanced techniques like SMOTE, class weights, and ensemble voting  
- Model evaluation beyond accuracy: Recall, ROC-AUC, PR-AUC  
- Business-driven optimization using threshold tuning to reduce false negatives  

---

### ✅ Business Value  
This model can help telecom companies:  
- Identify 78% of potential churners early  
- Improve customer retention strategy  
- Reduce revenue loss and increase customer lifetime value  

---

### ✍️ Author  
**Kifayat Sayed**  
M.Sc. AI & ML | Data Science Enthusiast  
📧 [kifayatsayed301@gmail.com](mailto:kifayatsayed301@gmail.com)  
🌐 [LinkedIn](https://www.linkedin.com/in/kifayat-sayed-9614a9244?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) | [Portfolio](#)  

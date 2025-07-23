# 📡 Telco Customer Churn Intelligence with GPT-Driven Personalization and BI Visualization

This project presents a full-stack **Customer Segmentation-Driven Churn Modeling and GPT-Based Retention Strategy** for a telecom provider—developed entirely in **Azure Machine Learning Studio**.

It features an integrated ML pipeline that:
- Applies **KMeans clustering** to segment over 7,000 customers into 4 distinct behavioral personas,
- Uses **LightGBM/XGBoost** for churn prediction per segment,
- Leverages **SHAP** to uncover segment-specific churn drivers, and
- Utilizes **Azure OpenAI GPT-3.5 Turbo** to auto-generate **personalized retention messages** (emails and short offers) tailored to each segment.

The solution simulates a marketing A/B test and visualizes customer uplift, churn reduction, and revenue impact using a **Power BI dashboard**—delivering data-driven storytelling for strategic marketing, CX, and leadership teams.

> 🔷 A cloud-native, marketing-intelligent AI solution built for real-world deployment and CRM personalization.

---

## 🎯 Business Objective

To identify churn-risk segments within the telecom customer base, uncover their behavioral triggers, and generate AI-personalized, data-backed retention messages—empowering marketing and CRM teams to design **hyper-targeted engagement strategies** and **simulate campaign ROI** before deployment.

---

## 🔁 Workflow Summary

### 🧹 1. Data Preparation
- Cleaned and preprocessed `7,000+` customer records
- Converted billing totals, encoded categorical fields

### 🎯 2. Customer Segmentation
- **KMeans clustering (k=4)** on scaled features
- Visualized clusters using PCA
- Segment naming derived from **SHAP churn drivers** + behavioral personas

### 🔮 3. Churn Prediction (Per Segment)
- Trained **LightGBM classifiers** with stratified sampling
- Hyperparameter tuning via **RandomizedSearchCV**
- Evaluated using **ROC AUC** and classification reports

### 🧠 4. Explainability (SHAP)
- Used SHAP to identify **top churn drivers per cluster**
- Mapped drivers back to real-world behaviors (e.g., low tenure, high bills)

### 🤖 5. GPT-3.5 Campaign Generation (Azure OpenAI)
- Prompted GPT with persona + churn drivers
- Auto-generated segment-wise:
  - Email retention messages
  - Short marketing hooks / offer pitches
- Saved in `cluster_retention_messages.json`

### 🧪 6. A/B Simulation
- Simulated uplift via randomized A/B groups
- “A” receives baseline offer, “B” receives GPT-personalized offer
- Churn simulated using realistic churn probabilities
- Resulting output: `telco_churn_ab_summary.csv`

### 📊 7. Power BI Dashboard
- Executive-ready visualization of:
  - Churn by customer segment
  - Customers saved vs. lost
  - Revenue saved vs. churned
  - Segment-wise offer effectiveness

---

## 🧠 Personas (Segment Overview)

| Cluster | Segment Name                    | Top Churn Drivers                        |
|--------:|----------------------------------|-------------------------------------------|
| 0       | Price-Sensitive Flexi Churners  | Month-to-month plan, high bills, low tenure |
| 1       | Underserved Essentials Churners | No TechSupport, low security, short contract |
| 2       | Premium Experience Expecters    | High expectations, no support, new users |
| 3       | Newcomer Value Skeptics         | High initial bills, unsure value, low tenure |

---

## ☁️ Azure-Based Tech Stack

| Category            | Tools & Services Used                                  |
|---------------------|---------------------------------------------------------|
| Development         | Python (Jupyter in **Azure ML Studio**)                |
| Machine Learning    | LightGBM, XGBoost, SHAP                                 |
| Segmentation        | KMeans (Scikit-learn)                                   |
| LLM Integration     | **Azure OpenAI (GPT-3.5 Turbo)**                        |
| BI & Storytelling   | **Power BI** for campaign uplift visualization          |
| Simulation Engine   | NumPy, pandas logic within Azure                        |
| Deployment Ready    | Azure ML Pipelines, Streamlit, Fabric-ready structure   |

---

## 🧪 Results Snapshot (Power BI)

| Metric                  | Value       |
|--------------------------|-------------|
| Customers Analyzed       | 7,032       |
| Base Churn Rate          | 26.6%       |
| Simulated Campaign Uplift| 3.67%       |
| Revenue Lost (Churn)     | $2.86M      |
| Revenue Saved (Offers)   | $0.08M      |
| Top Segment Saved        | Newcomer Skeptics – 11 customers |

> 📂 See `dashboard/Telcom_Insights.pdf` for the full dashboard

---

## 🧭 Future Enhancements

### 📈 For Telecom Companies
- **Plug into CRM Platforms** (e.g., Salesforce, Zoho): Push GPT messages directly to campaign builders
- **Integrate with SMS/Email APIs**: Automate trigger-based retention messaging
- **True A/B Test with Clickstream Data**: Replace simulation with real-time response behavior
- **Customer Journey Graphs (GNNs)**: Model temporal churn paths with network science
- **Real-time LLM Campaign Engine**: Auto-deploy custom GPT offers based on updated SHAP outputs

### 🧠 For Microsoft / Enterprise Use Cases
- **Modular Azure ML Designer Build**: Convert into componentized Azure ML pipeline
- **Deploy via Streamlit or Power BI Embedded** for CX Ops & Marketing Teams
- **Adaptable to Microsoft Fabric** for large-scale enterprise reporting
- **Scalable AI Architecture**: Reusable ML+LLM stack for other verticals (Retail, Insurance, Banking)

---


## 👩‍💼 Author

**Gargi Mishra**  
AI + Data Science | Customer Intelligence | Power BI | Azure ML  
🔗 [LinkedIn](https://www.linkedin.com/in/gargi510) | 💼 Open to Data Science/AI roles in Cloud

---

## 📜 License

MIT License – Use, modify, and improve with credit.

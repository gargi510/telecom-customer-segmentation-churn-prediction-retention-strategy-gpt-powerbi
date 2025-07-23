# 📡 Telco Customer Churn Intelligence with GPT-Driven Personalization and BI Visualization

This end-to-end telecom churn intelligence solution blends **AI-powered customer segmentation**, **LightGBM churn modeling**, **SHAP explainability**, and **GPT-3.5 campaign generation**, deployed through **Power BI insights**. The project simulates A/B testing on offers and models their revenue impact—making it ready for **real-world marketing orchestration** and **cloud deployment on Azure**.

---

## 🎯 Business Objective

To **identify churn-risk customer segments**, understand their behavioral drivers, and design **AI-personalized retention campaigns**—simulating uplift and providing **executive-level dashboards** for strategic decision-making.

---

## 🔁 Workflow Summary

### 🧹 1. Data Preparation
- Cleaned Telco dataset (`7,000+` customers)  
- Handled missing values, converted data types, and encoded categorical variables

### 🎯 2. Segmentation
- **KMeans clustering** on scaled features (k=4)
- PCA used for cluster visualization
- Segments named via SHAP + persona insights

### 🔮 3. Churn Modeling (Per Cluster)
- **LightGBM classifiers** with `RandomizedSearchCV` hyperparameter tuning
- Evaluated via **ROC AUC** and **classification report**

### 🧠 4. Explainability
- **SHAP analysis** to identify top churn drivers **per segment**
- SHAP visual summaries saved for transparency

### 🤖 5. GPT-3.5 Campaign Generation (Azure OpenAI)
- Segment-wise marketing prompts created using churn insights
- Generated **email content** and **short retention messages** per persona
- Stored as `cluster_retention_messages.json`

### 🧪 6. A/B Simulation
- Assigned groups A (control) and B (personalized) randomly
- Simulated churn based on realistic assumptions
- Output captured in `telco_churn_ab_summary.csv`

### 📊 7. Power BI Dashboard
- Visualized key metrics:
  - Churn by segment
  - Campaign effectiveness
  - Revenue lost vs. saved
  - Customers saved by cluster

---

## 🧠 Personas (Segment Overview)

| Cluster | Segment Name                    | Top Churn Drivers                        |
|--------:|----------------------------------|-------------------------------------------|
| 0       | Price-Sensitive Flexi Churners  | Month-to-month plan, high bills, low tenure |
| 1       | Underserved Essentials Churners | No TechSupport, low security, short contract |
| 2       | Premium Experience Expecters    | High expectations, no support, new users |
| 3       | Newcomer Value Skeptics         | High initial bills, unsure value, low tenure |

---

## 💡 Tech Stack

| Category            | Tools Used                                  |
|---------------------|----------------------------------------------|
| Programming         | Python, Pandas, Scikit-learn, SHAP, Seaborn |
| Machine Learning    | LightGBM, Hyperparameter Tuning              |
| LLM Integration     | Azure OpenAI GPT-3.5                         |
| Visualization       | Power BI, Matplotlib                        |
| A/B Simulation      | Custom logic in NumPy + Pandas              |
| Deployment Ready    | Azure ML, Streamlit (future), Databricks-ready structure |

---

## 🚀 Future Prospects

### 🧭 For Telecom Companies
- **Productionized Campaign Engine**: Trigger real-time LLM-generated offers for high-risk users
- **Cloud Deployment**: Serve through **Azure ML Pipelines** or **Databricks Workflows**
- **True A/B Testing**: Integrate with **email clickstream/response data** for uplift validation
- **Churn Prevention Playbooks**: Auto-recommend pricing/plan changes based on churn risk
- **Graph-Based Customer Journeys**: Using GNNs to model and predict churn paths

### 🌐 For Microsoft/Enterprise Use-Cases
- **Azure-native Build**: Can be modularized into Azure ML Designer + GPT integration pipeline
- **Demo-Ready BI App**: Ready for executive presentations or demo day at Microsoft/Azure bootcamps
- **Scalable ML+LLM Pattern**: Represents modern AI stack with ML model + LLM business logic
- **Use in Fabric**: Adaptable to Microsoft Fabric or Azure Synapse workflows with minimal refactor

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

> 📂 See `dashboard/Telcom_Insights.pdf` for complete visuals

---

## 👩‍💼 Author

**Gargi Mishra**  
AI + Data Science | Customer Intelligence | Power BI | Azure ML  
🔗 [LinkedIn](https://www.linkedin.com/in/gargi510) | 💼 Open to Data Science/AI roles in Cloud

---

## 📜 License

MIT License – Use, modify, and improve with credit.

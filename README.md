# Predicting Truck Component Failure: A Behavioral vs Technical Approach

**Author:** Petros Venieris  
**Affiliation:** Sandia National Laboratories & Georgia Tech 

---

## 📖  Overview

Heavy‑duty trucks underpin modern supply chains, yet unexpected component failures impose significant economic and safety risks. Traditional predictive maintenance focuses on machine‑derived signals only. This project introduces a **behavioral vs technical** paradigm explicitly modeling both driver behaviors (e.g., harsh braking, acceleration events) and mechanical indicators (e.g., temperature, pressure, vibration) to forecast component failures more accurately and cost‑effectively.
This project will be furtherly investigated with Sandia labs and georgia tech and might result in a research paper or stronger conclusions.
---
> 🔒 **Note:**  The code available on this rep is permitted for my portofolio showcase, It isn't the complete pipeline and the project had a lot of research, analysis, preperation and communication with SCANIA and truck drivers to come to results.

## 🎯 Key Achievements

- **End‑to‑End Pipeline**  
  - Ingested and merged **1.1 million** time‑step measurements from **23,550** vehicles  
  - Rigorous data cleaning: missing‑value filtering, outlier capping, rate conversion, and standardization  
  - Vehicle‑level feature engineering: distilled **105** raw channels into **533** aggregated features  

- **Behavioral vs Technical Partition**  
  - **Behavioral (24 features):** driver‑interaction metrics from sensor prefixes `167_`, `291_`, `837_`  
  - **Technical (81 features):** machine‑health signals from prefixes `397_`, `459_`, `158_`, etc.  
  - Combined set to evaluate hybrid model performance  

- **Advanced Modeling & Evaluation**  
  - Classifiers: Logistic Regression, Random Forest, Gradient Boosting, MLP, XGBoost  
  - Imbalance handling: bootstrap up‑sampling of failure cases & cost‑sensitive learning  
  - Metrics: ROC‑AUC, precision‑recall curves, cost reduction using SCANIA’s cost model (FP = 100 units, FN = 3,500 units)  

- **Business Impact**  
  - **Random Forest (combined features):** AUC = 0.705, **15%** cost reduction  
  - **Gradient Boosting (technical features):** AUC = 0.732, **20%** cost reduction  
  - Behavioral insights drive targeted driver training, reducing safety incidents  

---

## 🛠️ Technologies & Libraries

- **Data Manipulation & Visualization:** `pandas`, `NumPy`, `matplotlib`, `seaborn`  
- **Machine Learning & Evaluation:** `scikit-learn` (pipelines, imputation, metrics), `XGBoost`  
- **Imbalanced Data Techniques:** Bootstrap up‑sampling, cost‑sensitive thresholding  
- **Reproducibility:** Custom pipeline classes to prevent data leakage; fixed random seeds  

---

## 💼 Business Value

- **Cost Savings:** Minimizes expensive unplanned repairs by optimizing decision thresholds  
- **Safety Improvements:** Early detection of risky driving behaviors enables proactive training  
- **Operational Efficiency:** Combines predictive scheduling with real‑time driver advisories  
- **Scalability:** Designed for large‑scale telematics; adaptable to any heavy‑equipment fleet  

---

## 🚀 Next Steps

1. **Hyperparameter Tuning:** further optimize model AUC and cost metrics  
2. **Driver Coaching Module:** build real‑time feedback system based on behavioral flags  
3. **Production Deployment:** integrate with SCANIA’s fleet‑management platform  


---

## 📫 Contact

**Petros Venieris**  
✉️ pgvenieris@outlook.com
 


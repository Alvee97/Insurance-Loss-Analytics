# 📊 Insurance Loss Analytics – Group 21  (DSO 530)

### 📖 Project Story  
This project was developed as part of **DSO 530: Applied Modern Statistical Learning Methods** at USC Marshall.  
Our group (Team 21) chose to focus on the **insurance industry**, where mispriced policies and unpredictable claims often result in financial losses. We wanted to explore how **machine learning** could improve both **pricing fairness** and **risk management**.  

By predicting **Loss Costs (LC/HALC)** and **Claim Status (CS)**, our models not only achieved strong predictive performance but also provided **transparent, interpretable insights** using SHAP values. The end goal was to build something that insurers could trust and use in practice: a system that balances **accuracy, fairness, and business value**.  

---

## 📂 Files in this Repository  

### 1. 📘 `group_21_report.pdf`  
**Content:** Full project report.  
- **Models Used:** GLM (Tweedie), Random Forest, Gradient Boosting, LightGBM, Neural Network.  
- **Best Model:** LightGBM (LC RMSE = 283.37, HALC RMSE = 545.27, CS AUC = 0.76):contentReference[oaicite:0]{index=0}.  
- **Key Tools:** Feature engineering, SHAP for interpretability, class imbalance handling, hyperparameter tuning.  
- **Business Impact:** Improves pricing fairness, risk segmentation, and fraud detection.  

---

### 2. 🎥 `group_21_presentation.mp4.pdf`  
**Content:** Final presentation slides.  
- Summarizes problem, dual-solution approach, methodology, and key findings.  
- Explains SHAP insights (top features: **time since last renewal, policy duration, driving experience**).  
- Business implications:  
  - Fairer premium adjustments  
  - Avoid adverse selection  
  - Better risk segmentation & portfolio balance:contentReference[oaicite:1]{index=1}  

---

### 3. 💻 `DSO_530_PROJECT_PUBLIC.ipynb`  
**Content:** Jupyter Notebook (public version).  
- Contains data cleaning, feature engineering, and model-building code.  
- Implements LightGBM pipelines with cross-validation and hyperparameter tuning.  
- Includes SHAP visualizations for interpretability.  

---

## ⚙️ Methodology Overview  

1. **Data Cleaning & Feature Engineering**  
   - Derived Vehicle Age, Driver Age, Driving Experience, Policy Duration, Time Since Last Renewal.  
   - Removed outliers (top/bottom 0.1% for LC/HALC).  
   - One-hot encoded categorical features:contentReference[oaicite:2]{index=2}.  

2. **Task 1 – Loss Cost (LC) & HALC Prediction**  
   - Baseline: GLM with Tweedie distribution.  
   - Best: **LightGBM** with tuned hyperparameters.  
   - Performance: RMSE = **283.37 (LC)**, **545.27 (HALC)**.  
   - Innovation: SHAP-based **Risk Profile Cards** for customer-level insights.  

3. **Task 2 – Claim Status (CS) Prediction**  
   - Models tested: Logistic Regression, RF, XGBoost, Neural Net, LightGBM.  
   - Best: **LightGBM** (Test AUC = **0.76**).  
   - Class imbalance handled with scaled weights & threshold tuning (F1-based).  
   - Top features: **time since last renewal, policy duration, driving experience**.  

---

## 📌 Business Insights  

✔️ **Pricing Accuracy:** Improves fairness by aligning premiums with actual risk.  
✔️ **Risk Management:** Detects high-risk customers early for intervention.  
✔️ **Portfolio Balance:** Reduces adverse selection & enhances profitability.  
✔️ **Explainability:** SHAP ensures transparency for regulators & stakeholders.  

---

## 👥 Team Members (Group 21)  
- Romina Fareghbal  
- Carla Francois  
- Fangdi (Flora) Zhai  
- Weiqi Huang  
- Shahriar Rahman  
- Mansour Almubaraki

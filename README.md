# 📈 Predicting E-commerce Customer Spend

**Linear Regression Project**  
Use case: Predict annual customer spend using session behavior and membership data.

---

## 🧠 Motivation

- **Business goal:** Help e-commerce platforms understand which customer behaviors (app usage, membership duration, etc.) drive higher spending.
- **Why it matters:** Insights support better retention and app-driven marketing strategies.

---

## 📦 Dataset

- **Source:** `Ecommerce Customers.csv` (500 rows, 8 columns) from https://www.kaggle.com/datasets/iyadavvaibhav/ecommerce-customer-device-usage
- **Columns:**
  - `Avg. Session Length`: Avg. in-store session duration (minutes)
  - `Time on App`: Daily app usage (minutes)
  - `Time on Website`: Daily website usage (minutes)
  - `Length of Membership`: Customer tenure (years)
  - `Yearly Amount Spent`: Annual customer spending (USD)
- **Note:** No personal data included; values are fictional.

---

## ⚙️ Methodology

1. **Data Exploration:**
   - Visualized feature relationships using scatterplots and regression lines.
   - Identified strong correlation between membership length and spending; moderate correlation with app time.

2. **Model Setup:**
   - Features: Session length, app time, website time, membership length.
   - Target: Yearly Amount Spent.
   - Train/test split: 70% train, 30% test (random_state=0).

3. **Linear Regression Model:**
   - Trained on the training set.
   - Intercept and feature coefficients extracted for interpretation.

4. **Evaluation Metrics:**
   - R² score (overall fit on full data).
   - MAE, MSE & RMSE on test set.
   - Visualized predicted vs. actual values.
   - Assessed residual distribution for model validity.

---

## 📊 Results

### Model Coefficients
- Intercept: **-1037.826**  
- Avg. Session Length: **+25.768**  
- Time on App: **+38.800**  
- Time on Website: **–0.018**  
- Length of Membership: **+61.853**

### Performance Metrics
- **R²:** 0.984 (model explains 98.4% of spending variance)
- **MAE:** ≈ \$7.85  
- **RMSE:** ≈ \$9.72  
- Residuals are roughly normal—good model fit.

### Key Insights
- Membership duration and app usage are the strongest spending drivers.
- Session length adds some impact.
- Website usage has negligible effect.

---

## 💡 Business Takeaways

- **Invest in the mobile app** to boost customer interaction and income.
- **Retain long-term users**—they spend more over time.
- **Reevaluate website strategy**, since it doesn't influence spending significantly.

---

## 🔍 Future Work

- Test non-linear models (e.g., Random Forest, XGBoost).
- Engineer new features (e.g., session frequency).
- Run cross-validation for more robust performance metrics.
- Segment customers for personalized modeling.

---

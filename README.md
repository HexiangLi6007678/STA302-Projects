# STA302 – Academic Reputation Modeling Project

## Project Overview
This project investigates **which institutional factors most strongly influence the Academic Reputation Score** in the QS World University Rankings 2025.

Using a dataset of **1,500+ universities** and **10+ institutional indicators**, we developed a full statistical modeling workflow:

- Data cleaning & preprocessing  
- Exploratory data analysis  
- Multiple linear regression  
- Lasso variable selection  
- Stepwise AIC model refinement  
- Box–Cox transformation  
- Influential point diagnostics (Cook’s Distance, DFFITS, leverage)  
- Final model inference and interpretation  

**Full report:** [final project report (1).pdf](final%20project%20report%20(1).pdf)
**Full R code:** [STA302(FINAL_CODE__).Rmd](STA302(FINAL_CODE__).Rmd)
**Dataset:** [QS World University Rankings 2025 (Top global universities).csv](QS%20World%20University%20Rankings%202025%20(Top%20global%20universities).csv)

---

### **Most Influential Predictors of Academic Reputation**
From the final cleaned regression model, the strongest predictors are:

| Predictor | Effect | Interpretation |
|----------|--------|----------------|
| **Employer Reputation Score** | Strongest | Universities viewed favorably by employers have significantly higher academic reputation. |
| **International Research Network Score** | Strong positive | Cross-border collaboration and co-authorship boost visibility and reputation. |
| **Citations per Faculty** | Positive | Research impact and productivity correlate with higher reputation. |
| **Employment Outcomes Score** | Positive | Schools with stronger graduate outcomes gain reputational advantage. |
| **Sustainability Score** | Positive | Social responsibility increasingly shapes institutional perception. |
| **SIZE (Large, XL)** | Positive | Larger institutions benefit from visibility and resources. |

### **Not significant predictors**
- **International Student Score**  
- **Medium-size institutions (SIZEM)**  
- **Faculty–Student Ratio**

These variables show **no statistically meaningful effect** once other factors are controlled for.

---

## Final Model Performance
After Lasso selection, AIC stepwise refinement, Box–Cox transformation (λ ≈ 0.222), and removal of 10 influential observations:

| Metric | Value |
|--------|--------|
| **R²** | 0.8150 |
| **Adjusted R²** | 0.8132 |
| **10-fold CV MSE** | **0.585** (improved from 0.735 pre-cleaning) |
| **AIC** | 2207.10 |
| **BIC** | 2260.63 |

These metrics reflect a model that is **statistically robust**, **interpretable**, and satisfies most regression assumptions after refinement.

---

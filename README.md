# 🚀 From Black Box to Insights
### Explainable AI for Early-Stage VC Dealflow — Pre-Series A Snapshot

This dataset and notebook power a hands-on session where you build a simple ML model on a synthetic startup dataset and use SHAP to explain predictions.

## Dataset
**File:** seed_pre_series_a_with_eda.csv (6 000 rows)

- **Target:** `success_36m` = 1 if a company raised a Series A or exited (M&A/IPO) within 36 months and did not shut down.  
- **Scope:** All inputs describe the company **before Series A** (Pre-Series A).  
- **Pitfall field:** `current_employee_count` is intentionally included to illustrate **data leakage** — don’t use it in the baseline model.

## Notebook flow
1. **EDA**: quick overview, class balance, sector/stage/location context, traction & burn patterns  
2. **Model**: Random Forest + one-hot encoding  
3. **Pitfall**: add `current_employee_count` → AUC spike  
4. **Global SHAP**: interpretable drivers (traction ↑, efficiency ↑, hype ↓) — personality excluded from visuals  
5. **Local SHAP**: two narrative cases  
6. **Learning curve + Slices**: stability and fairness checks

**Attribution:** Synthetic educational dataset for workshops by HPI Ventures.

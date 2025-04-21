
# HubSpot Prospect Conversion Analysis

This repository contains a full analysis and predictive model to determine which HubSpot free-tier prospects are most likely to convert into paying customers.

## Project Objective

Identify key differentiators between prospects who convert and those who don’t, and build a machine learning model to predict future conversions. This enables weekly scoring of active prospects to guide Sales, Marketing, and Customer Success strategies.

---

## Datasets Used

- **customers.csv** — Sample of paying customers
- **noncustomers.csv** — Free-tier users who haven’t converted
- **usage_actions.csv** — CRM usage logs for all users (Contacts, Companies, Deals, Emails)

---

## Features Engineered

- Total CRM actions per object
- Total users per object
- Days active, activity span, recency
- Employee range and industry
- Aggregated into per-company features

---

## Model Summary

- Model: `RandomForestClassifier`
- Metrics:
  - ROC AUC ≈ 0.96
  - Precision ≈ 0.85 (for class 1)
  - Recall ≈ 0.59
- Top Features:
  - CRM Contacts activity
  - Deal activity
  - Recency
  - Total actions

---

## Files

- `Hubspot Analysis.ipynb` — Full Jupyter Notebook with step-by-step code and markdown explanations
- `engineered_dataset.csv` — Final dataset used for modeling
- `Hubspt Analysis.csv` — Additional result file (if applicable)

---

## Business Recommendations

- Target high-activity and recently active free-tier users for conversion campaigns
- Focus outreach on mid-sized companies in high-converting industries like SaaS and E-Learning
- Use model scores weekly to guide Sales and CS teams

---

## Future Enhancements

- Add deal stage and pipeline features
- Build an automated scoring pipeline with Airflow or Cron
- Explore NLP on email content or notes
- Extend to revenue prediction via regression

---

## Author

**Muhammad Ibrahim**  
Powered by Python, pandas, scikit-learn, and seaborn.

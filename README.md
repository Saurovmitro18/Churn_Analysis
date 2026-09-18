# 📊 Customer Churn & Retention Analysis

An end-to-end data analytics and business intelligence project investigating customer churn patterns across subscription tiers, geographic regions, and support interactions. 

This project extracts relational data from a SQLite database, cleanses and merges disparate tables (demographics, subscriptions, and support tickets), engineers churn indicators, and evaluates key financial metrics (ARPU, Revenue at Risk, and Escalation Correlation).

---

## 📌 Key Insights & Business Metrics

* **Overall Churn Rate:** `28.57%` (Retention Rate: `71.43%`)
* **Average Revenue Per User (ARPU):** `18.85`
* **Total Revenue at Risk:** `73.94K`
* **Average Customer Tenure:** `1,539 days`
* **Support Escalation Correlation:** Strong positive correlation (`r = 0.77`) between unresolved/escalated support tickets and customer cancellations.
* **Churn by Plan Tier:**
  * **Basic Plan:** `60.00%` churn (Highest risk tier)
  * **Standard Plan:** `22.22%` churn
  * **Premium Plan:** `14.29%` churn

---

## 🗂️ Data Architecture

The raw relational data is sourced from `customer_churn.db` across three primary entities:

| Table | Description | Key Features |
| :--- | :--- | :--- |
| **`db_customer`** | Demographic profiles | `customerid`, `customer_name`, `country`, `state`, `gender`, `dob` |
| **`db_subscription`** | Billing & contract lifecycle | `plan_type`, `contract_type`, `monthly_charges`, `cltv`, `churn_score`, `cancellation_date` |
| **`db_support`** | Service & ticketing logs | `complaint_date`, `escalations`, `csat_score`, `complaint_count` |

---

## ⚙️ Data Pipeline & Workflow

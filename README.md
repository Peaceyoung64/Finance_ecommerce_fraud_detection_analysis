# Finance E-Commerce Fraud Detection Analysis

##  Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset Overview](#dataset-overview)
3. [Technologies Used](#technologies-used)
4. [Business Questions Answered](#business-questions-answered)
5. [Key Metrics](#key-metrics)
6. [Key Insights](#key-insights)
7. [Visualizations](#visualizations)
8. [Conclusion](#conclusion)
9. [Recommendations](#recommendations)
   


## Project Overview
This project analyzes financial e-commerce transactions to detect fraud patterns, assess risk exposure, and provide actionable insights.  
The dataset contains **6,055 cleaned transactions**, and although the overall fraud rate is low, analyzing these rare events is crucial because even a few fraudulent transactions can have a significant financial impact.  The analysis explores trends across customers, merchants, transaction amounts, balances, categories, and geographies, helping businesses proactively reduce fraud.  

---
**Objectives:**
-	Measure overall fraud exposure and understand differences from normal transactions
-	Identify high-risk merchants, categories, and regions
-	Detect account and transaction patterns that indicate fraud
-	Provide actionable insights to reduce financial loss and strengthen detection systems
---

## Dataset Overview
| Column | Description |
|--------|-------------|
| TransactionID | Unique identifier for each transaction |
| Date | Transaction date |
| AccountID | Customer account identifier |
| AccountName | Customer name |
| TransactionType | Type of transaction (Purchase, Refund, Transfer, etc.) |
| Amount | Transaction amount |
| Currency | Transaction currency |
| ExchangeRate | Conversion rate applied (if any) |
| Balance | Account balance after transaction |
| Merchant | Merchant involved |
| MerchantPhone | Merchant phone |
| MerchantEmail | Merchant email |
| Category | Transaction category |
| Subcategory | Subcategory for the transaction |
| Country | Country where transaction occurred |
| City | City of transaction |
| PostalCode | Postal code of transaction |
| CardNumber | Masked card number used |
| Email | Customer email |
| Phone | Customer phone |
| IsFraud | Binary fraud indicator (0 = Non-Fraud, 1 = Fraud) |
| Notes | Additional notes about transaction |

---

## Technologies Used
- Python
- Pandas
- NumPy
- Seaborn / Matplotlib
- Jupyter Notebook

---

## Business Questions Answered
This analysis addresses the following questions:
1. What is the fraud rate in the dataset?
2. How do fraud amounts compare with non-fraud?
3. Which merchants show the highest fraud activity?
4. Which categories show more fraud patterns?
5. Are some countries more prone to fraud?
6. Do unusual balance behavior patterns indicate fraud?
7. What actionable insights can reduce fraud on the platform?
8. On which days of the week do fraud cases occur most frequently?

---

## Key Metrics
- **Fraud rate:** 0.297 (≈30% of transactions flagged as fraudulent)  
- **Top fraudulent merchants:** Amazon, ShopEasy, Zomato  
- **High-risk categories:** Entertainment, Education, Health  

---

## Key Insights
- **Fraud Rate = 29.73%** — The platform is experiencing high fraud exposure.  
- Fraudsters use low-value transactions to avoid detection.  
- Fraud is concentrated among popular, high-traffic merchants, especially digital-first platforms with fast payment flows.  
- Fraudsters target digital subscription and fast-checkout categories, which require minimal authentication.  
- Fraud is region-dependent; geographic risk scoring is necessary.  
- Balance behavior does not predict fraud — detection must rely on categorical and behavioral signals.  
- Fraud mitigation should prioritize behavioral monitoring over transaction value thresholds.  
- Fraud spikes mostly on **Sundays**.

---
##  Visualizations

### Fraud by Merchant

![Fraud by Merchant]
*Shows the top merchants where fraud occurs most frequently.*

### Fraud by Category
![Fraud by Category](images/fraud_by_category.png)  
*Highlights categories with highest fraud rates.*

### Fraud by Country
![Fraud by Country](images/fraud_by_country.png)  
*Displays geographic fraud patterns.*

### Fraud by Day of Week
![Fraud by Day](images/fraud_by_day.png)  
*Shows which days have the most fraudulent transactions.*

### Fraud by Category
![Fraud by Category](images/fraud_by_category.png)  
*Highlights categories with highest fraud rates.*

### Fraud by Country
![Fraud by Country](images/fraud_by_country.png)  
*Displays geographic fraud patterns.*

### Fraud by Day of Week
![Fraud by Day](images/fraud_by_day.png)  
*Shows which days have the most fraudulent transactions.*


---

## Conclusion
Fraud within the platform is high (29.73%), with strong patterns across merchants, categories, and regions. Numerical variables like transaction amount, balance, and exchange rate show no meaningful correlation with fraud.  

Fraud is heavily influenced by **merchant behavior, transaction category, and geographic location**, often occurring through **small-amount transactions** in fast and digital-driven categories such as Entertainment, Education, and Health.  

High-volume merchants like Amazon, ShopEasy, and Zomato are more targeted.  

**Implication:** Fraud prevention should focus on behavioral patterns, merchant-level, category-level, and regional risk analysis rather than monetary thresholds.

---


## Recommendations
1. Implement merchant-level fraud monitoring  
2. Strengthen fraud prevention in high-risk categories  
3. Apply geographic risk scoring  
4. Prioritize small-amount fraud detection  
5. Incorporate categorical features into fraud detection models  
6. Introduce anomaly detection for account behavior  
7. Educate customers and merchants  
8. Increase monitoring during high-risk periods

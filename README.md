# 🛡️ E-Commerce Fraud Detection — VPN Transactions Analysis
![Uploading image.png…]()


> Exploratory analysis of an e-commerce transaction dataset to identify fraud patterns linked to VPN usage.

---

## 📋 Overview

This project analyzes **10,000 e-commerce transactions** to understand the behavior of transactions detected with an active VPN, often associated with location spoofing or suspicious activity.

The main goal is to uncover actionable patterns to improve fraud detection strategies.

---

## 🎯 Objectives

- Identify the **product categories** most affected by VPN transactions
- Determine the **browsers** most commonly used during these transactions
- Analyze **card types** (Visa, Mastercard, etc.) associated with VPN transactions
- Compare fraud rates between VPN and non-VPN transactions
- Provide **concrete recommendations** for fraud prevention

---

## 📂 Project Structure

```
├── ecommerce_fraud_dataset.csv   # Main dataset (10,000 transactions)
├── notebook_fraude.ipynb         # Main analysis notebook
└── README.md
```

---

## 📊 Dataset

| Attribute | Detail |
|---|---|
| **File** | `ecommerce_fraud_dataset.csv` |
| **Rows** | 10,000 transactions |
| **Columns** | 18 features |
| **Period** | 2023 |

### Features

| Column | Type | Description |
|---|---|---|
| `transaction_id` | string | Unique transaction identifier |
| `transaction_date` | datetime | Date and time of the transaction |
| `hour` | int | Hour of the transaction |
| `amount_usd` | float | Transaction amount in USD |
| `category` | string | Product category |
| `country` | string | Country of origin |
| `payment_method` | string | Payment method used |
| `card_type` | string | Card type (Visa, Mastercard…) |
| `device_type` | string | Device type used |
| `browser` | string | Browser used |
| `account_age_days` | int | Account age in days |
| `tx_last_24h` | int | Number of transactions in the past 24 hours |
| `n_items` | int | Number of items purchased |
| `addr_mismatch` | int (0/1) | Shipping address mismatch flag |
| `form_fill_time_sec` | int | Form fill time in seconds |
| `email_domain` | string | Email address domain |
| `vpn_detected` | int (0/1) | VPN detected during transaction |
| `is_fraud` | int (0/1) | Label: fraudulent transaction |

---

## 🔍 Key Findings

- **6.19%** of transactions (619 out of 10,000) were made with an active VPN
- VPN transactions show a **higher fraud rate** compared to standard transactions
- Certain categories, browsers, and card types are **over-represented** in VPN transactions

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas 
```

### Run the Notebook

```bash
jupyter notebook notebook_fraude.ipynb
```

---

## 💡 Recommendations

1. **Enhanced Monitoring** — Apply stricter checks on VPN transactions, especially in high-risk categories
2. **Browser-Based Rules** — Incorporate browser type as a signal in detection models
3. **Geolocation Verification** — Develop identity verification methods beyond IP-based location detection
4. **Predictive Modeling** — Train a machine learning model on these patterns for automated detection


## 📄 License

This project is intended for educational and analytical purposes.

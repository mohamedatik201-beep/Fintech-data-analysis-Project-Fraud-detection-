# 🛡️ E-Commerce Fraud Detection — VPN Transaction Analysis in UK

Exploratory analysis of **10,000 e-commerce transactions** to identify fraud patterns linked to VPN usage, suspicious browsing behavior, and payment anomalies.

---

## 📌 Context

This project investigates how VPN usage correlates with fraudulent e-commerce activity. The goal is to surface actionable patterns that can feed into a fraud prevention strategy or a future ML classification model.

---

## 📂 Repository Structure

```
Fintech-data-analysis-Project-Fraud-detection/
├── ecommerce_fraud_dataset.csv   # Main dataset (10,000 transactions)
├── notebook_fraude.ipynb         # Full EDA notebook
└── README.md
```

---

## 📊 Dataset Overview

| Attribute | Detail |
|---|---|
| Rows | 10,000 transactions |
| Columns | 18 features |
| Period | 2023 |
| Target | `is_fraud` (0 / 1) |

### Key Features

| Column | Description |
|---|---|
| `transaction_id` | Unique transaction identifier |
| `transaction_date` | Date and time |
| `amount_usd` | Transaction amount (USD) |
| `category` | Product category |
| `country` | Country of origin |
| `card_type` | Visa, Mastercard… |
| `device_type` | Device used |
| `browser` | Browser used |
| `account_age_days` | Account age in days |
| `tx_last_24h` | Transactions in the past 24h |
| `addr_mismatch` | Shipping address mismatch (0/1) |
| `vpn_detected` | VPN active during transaction (0/1) |
| `is_fraud` | Fraud label (0/1) |

---

## 🔍 Key Findings

- **6.19%** of transactions (619 / 10,000) were made with an active VPN
- VPN transactions show a significantly **higher fraud rate** than standard ones
- Specific **product categories**, **browsers**, and **card types** are over-represented among VPN transactions
- **Address mismatch** and **short form fill time** are strong co-indicators of fraud

---

## 💡 Recommendations

| Priority | Action |
|---|---|
| 🔴 High | Apply stricter verification on VPN transactions in high-risk categories |
| 🟠 Medium | Incorporate browser type and device as fraud signals |
| 🟡 Planned | Build an ML classifier (Random Forest / XGBoost) on these patterns |

---

## 🚀 Getting Started

```bash
git clone https://github.com/mohamedatik201-beep/Fintech-data-analysis-Project-Fraud-detection-.git
cd Fintech-data-analysis-Project-Fraud-detection-
pip install pandas matplotlib jupyter
jupyter notebook notebook_fraude.ipynb
```

---

## 🛠️ Tech Stack

- **Python 3.10+**
- pandas · matplotlib · jupyter

---

## 📄 License

For educational and analytical purposes.

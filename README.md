# banking-analytics-Power-Bi
Power BI banking analytics (Data Drip Hackathon) – customer health, card security, transaction intelligence
# Banking Analytics Report – Power BI (Data Drip Hackathon, August 2025)

This repository contains a comprehensive Power BI solution for banking data analysis developed for the **Data Drip Hackathon**. The report transforms raw operational data into actionable insights across three pillars:
1) **Customer Financial Health**, 2) **Card Security**, and 3) **Transaction Intelligence**.

---

## Dataset Overview

The model uses three tables (column names preserved as in source):

### `users_data`
- `id`, `current_age`, `retirement_age`, `birth_year`, `birth_month`, `gender`, `address`,  
  `latitude`, `longitude`, `per_capita_income`, `yearly_income`, `total_debt`,  
  `credit_score`, `num_credit_cards`

### `transactions_data`
- `id`, `date`, `client_id`, `card_id`, `amount`, `use_chip`, `merchant_id`,  
  `merchant_city`, `merchant_state`, `zip`, `mcc`, `errors`

### `cards_data`
- `id`, `client_id`, `card_brand`, `card_type`, `card_number`, `expires`, `cvv`,  
  `has_chip`, `num_cards_issued`, `credit_limit`, `acct_open_date`,  
  `year_pin_last_changed`, `card_on_dark_web`

> **Privacy note:** Sensitive fields (e.g., `card_number`, `cvv`) are not surfaced in visuals.  
> **Cleaning summary:** Currency → numeric, dates parsed with locale, ZIP normalized to 5 digits text,  
> scientific notation avoided for card numbers, geolocation ranges validated, error text normalized.

---

## Key Features

- **Three Interactive Pages**
  - *Customer Financial Health*: income, debt, credit score, DTI, demographic slices.
  - *Card Security & Risk*: chip usage, dark web flags, expiries, PIN change recency.
  - *Transaction Intelligence*: channel mix (online/card-present), MCC profiles, anomalies.
- **Advanced DAX Measures (15+)**
  - Debt-to-Income, Avg Credit Score, High-Risk Flags, Error Rate, Refund Rate,  
    Online Share, Chip Adoption, Expiry Risk, PIN Change Recency Buckets, etc.
- **Dynamic Filtering**
  - Slicers by date, channel, MCC, geography, customer cohort, and risk flags.
- **Clean, Bank-Oriented Theme**
  - Green–gold–gray palette, light backgrounds, consistent typography.
- **Reusable Power Query (M) Transformations**
  - Type coercion, currency cleanup, standardization, quality flags (no destructive drops).

---
## Project Structure

## Customer Financial Health
![Customer Financial Health](banking-analytics-Power-Bi/Customer%20Financial%20Health.png)

## Card Security and Usage
![Card Security and Usage](banking-analytics-Power-Bi/Card%20Security%20and%20Usage.png)

## Transaction Intelligence Dashboard
![Transaction Intelligence Dashboard](banking-analytics-Power-Bi/Transaction%20Intelligence%20Dashboard.png)






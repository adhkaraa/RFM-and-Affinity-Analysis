# Retail Transaction Analysis – RFM & Affinity Insights

This project analyzes retail transaction data using RFM (Recency, Frequency, Monetary) and product affinity analysis to better understand customer behavior, product dynamics, and sales trends.

---

## 📌 Objectives

- Segment customers based on transaction behavior (RFM Analysis)
- Understand purchasing patterns by product category (Affinity Analysis)
- Quantify the impact of non-revenue and promotional items

---

## 🧱 Workflow Overview

### 🔹 1. Load Dataset
Import raw transactional data into a structured pandas DataFrame.

### 🔹 2. Pre-processing Data
- Handle nulls, data types, and date formats
- Filter out `GIFT CARD`, `PROMOTION GOODS`, and `MERCHANDISE GOODS` with `t_net = 0`
- Create flags for member vs. non-member

### 🔹 3. Member Transactions (RFM Analysis)
Performed only on transactions with valid member IDs.

Steps:
- **Calculate Recency**: Days since last transaction
- **Calculate Frequency**: Number of transactions per member
- **Calculate Monetary Value**: Total revenue per member
- Merge these into a single RFM table
- Assign RFM scores per customer

### 🔹 4. Affinity Analysis
- Analyze product associations **by category**
- Explore product bundling or category co-purchase behavior
- Calculate the **percentage of promotional goods** across all transactions

---

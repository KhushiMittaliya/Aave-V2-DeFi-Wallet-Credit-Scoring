# Aave V2 DeFi Wallet Credit Scoring

## 🔍 Overview

This project develops a credit scoring model for DeFi wallets using 100K+ raw transaction records from the Aave V2 lending protocol. Each wallet’s behavior is analyzed based on actions like deposit, borrow, repay, and liquidation. A machine learning pipeline assigns a **credit score (0–1000)** reflecting the wallet’s reliability and risk.

## 🎯 Objective

To build a data-driven scoring system that:
- Analyzes wallet-level transactional behavior
- Clusters users with similar DeFi behaviors
- Assigns credit scores to wallets to distinguish between responsible users and risky or exploitative ones

## 🛠️ Methodology

1. **Data Preprocessing**:
   - Loaded Aave V2 transaction data from JSON
   - Cleaned, formatted, and extracted relevant columns

2. **Feature Engineering**:
   - Aggregated wallet-wise metrics (total deposits, borrows, repays, etc.)
   - Derived behavioral ratios: borrow-to-deposit, repay-to-borrow, etc.

3. **Clustering (K-Means)**:
   - Applied K-Means on normalized features
   - Used Elbow Method to determine optimal cluster count
   - Segregated wallets into behavioral groups

4. **Credit Scoring Logic**:
   - Mapped clusters to credit score ranges (0–1000)
   - Scores reflect responsible (higher score) vs. risky (lower score) DeFi behavior

5. **Visualization**:
   - Pairplot for cluster behavior analysis
   - Elbow plot for cluster validation
   - Score distribution graph for reporting

## 📊 Features Used

- `total_deposit_usd`
- `total_borrow_usd`
- `total_repay_usd`
- `borrow_deposit_ratio`
- `repay_borrow_ratio`
- `transaction_count`
- `unique_assets_used`

## 📁 Files Included

| File Name                      | Description                                         |
|-------------------------------|-----------------------------------------------------|
| Aave V2 lending platform.ipynb | Main notebook with code and analysis               |
| README.md                     | Project overview and documentation                 |
| analysis.md                   | Score distribution, cluster-wise analysis, insights|

## ✅ Key Results

- Effective clustering of wallet behavior
- Transparent credit scoring system
- Score range clearly reflects user type:
  - 800–1000: Responsible wallets
  - 400–799: Average users
  - 0–399: Risky or bot-like wallets

## 📌 Requirements

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn

# 📈 Credit Score Analysis – Aave V2 DeFi Wallet Scoring

## 🧩 Clustering Summary

After applying K-Means clustering to wallet-level behavioral features, we identified **3 major user clusters**, each representing a unique type of DeFi user based on their transaction behavior on Aave V2.

| Cluster | Characteristics                                 | Behavior Type      | Score Range |
|---------|--------------------------------------------------|---------------------|-------------|
| 0       | High deposits, high repayments, regular usage   | Responsible Users   | 800–1000    |
| 1       | Moderate usage, average ratios                  | Average Users       | 400–799     |
| 2       | Low repays, high borrows, liquidations frequent | Risky / Bot-like    | 0–399       |

Each wallet in the dataset was assigned a cluster and scored accordingly. Clusters were mapped to score ranges to simplify interpretation.

---

## 📊 Credit Score Distribution

The credit scores were segmented into 10 bins (0–100, 100–200, ..., 900–1000). The graph below shows the number of wallets in each score range:


| Score Range | Wallet Count |
| ----------- | ------------ |
| 0–100       | ████████     |
| 100–200     | ███████████  |
| 200–300     | ████████████ |
| 300–400     | █████████    |
| 400–500     | ████████     |
| 500–600     | ███████      |
| 600–700     | █████        |
| 700–800     | ████         |
| 800–900     | ██           |
| 900–1000    | █            |

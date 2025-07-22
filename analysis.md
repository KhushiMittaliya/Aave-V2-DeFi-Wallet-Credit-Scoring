# 📈 Credit Score Analysis – Aave V2 DeFi Wallet Scoring

##  Clustering Summary

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



> *(For real plots, use `sns.histplot(df['score'], bins=10)` in the notebook)*

---

##  Behavior of Wallets – Cluster-wise Insights

### Cluster 0: Responsible Users (800–1000)
- **Traits**: High deposit & repay values, healthy repay-to-borrow ratio, low liquidation count
- **Usage**: Regular, long-term users or institutions
- **Trust Level**: High – these wallets are good candidates for undercollateralized lending or premium benefits

### Cluster 1: Average Users (400–799)
- **Traits**: Moderate deposit and borrow values, fair ratios, standard activity
- **Usage**: Typical DeFi retail users or new entrants
- **Trust Level**: Medium – these users show healthy usage but not exceptional reliability

### Cluster 2: Risky Users (0–399)
- **Traits**: Low repayments, high borrow-to-deposit ratio, some liquidation history
- **Usage**: Exploitative patterns or bot-driven activity
- **Trust Level**: Low – these users may default or abuse lending mechanics

---

## Key Takeaways

- Clustering users allows platforms like Aave to **profile risk** without accessing private data.
- Behavior-based scores reflect the **real usage trends** of DeFi users.
- This model could help design **trust-based lending**, **reputation scores**, or **DeFi credit limits**.

---

##  Future Scope

- Include time-series behavior for trend analysis (e.g., how behavior changes over weeks)
- Merge on-chain data from other protocols (e.g., Compound, MakerDAO) to build holistic scores
- Integrate wallet identity tools (ENS, Lens Protocol) for better user reputation tracking

---



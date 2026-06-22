# Mobile Money Customer Segmentation & Behavior Analysis

Exploratory data science project analyzing 6.3M+ mobile money transactions using the [PaySim](https://www.kaggle.com/datasets/ealaxi/paysim1) synthetic dataset — modeled to mirror real mobile money platforms like JazzCash/Easypaisa operating in Pakistan's branchless banking sector.

## Objective

Act as a data scientist at a mobile money operator and answer three business questions:
1. **Who are our users?** — behavioral segmentation
2. **Are they sticking around?** — cohort retention analysis
3. **Does early behavior predict long-term value?** — hypothesis testing

## Key Findings

- **4 distinct customer segments** identified via K-Means clustering: Everyday Payers (34%), Cash-Out Users (35%), Cash-In Users (22%), High-Value Transfer Users (8%)
- **PaySim is a single-transaction dataset** — 99%+ of accounts transact exactly once, making traditional retention curves flat by design. Documented and explained honestly rather than misrepresented.
- **CASH_OUT-first users transact 13x more in total volume** than PAYMENT-first users (176k vs 13k mean), with statistical significance (p ≈ 0, Cohen's d = 1.28 — large effect). This justifies designing onboarding nudges toward cash-out as a first action for a real operator.

## Dataset

[PaySim on Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1) — 6.3M transactions, 743 simulated hours (≈30 days), 11 features.

Download `PS_20174392719_1491204439457_log.csv`, rename to `paysim.csv`, place in `data/`.

The `data/` folder is gitignored — never commit the raw CSV.

## Setup

```bash
git clone https://github.com/falahhilal/paysim-mobile-money-analysis.git
cd paysim-mobile-money-analysis
python -m venv venv
source venv/Scripts/activate  # Windows
pip install -r requirements.txt
jupyter notebook
```

## Skills Demonstrated

K-Means clustering · elbow & silhouette method · cohort retention analysis · Welch's t-test · Cohen's d effect size · EDA · feature engineering from raw transaction logs · Matplotlib/Seaborn visualization
# IPL 2026 Final Match Prediction — GT vs RCB

## Overview

A machine learning project that analyzes IPL 2026 league stage match data and predicts the winner of the **IPL 2026 Final between GT and RCB**, using classification models and a stat-based comparison system.

---

## Approach

- Loaded and explored `matches.csv` from the IPL 2026 Kaggle dataset — **partial season data only** (39 out of 74 league matches, 23 columns)
- Cleaned raw columns — split `best_bowling_figure` into numeric wickets and runs, dropped irrelevant fields
- Encoded categorical columns and applied StandardScaler on key numeric features
- Trained three classification models to predict match winners
- Used 5-fold cross-validation due to the small dataset size (38 usable rows)
- Since model accuracy was low due to limited data, used a simple stat-based comparison of 5 key metrics to predict the final winner

---

## Model Comparison

| Model | Cross-Val Accuracy |
|---|---|
| Logistic Regression | 0.34 |
| Random Forest | 0.28 |
| **XGBoost** | **0.34** |

> Low accuracy is expected — the dataset has only 38 matches. Cross-validation was used over a simple train-test split to get a more reliable estimate.

---

## Final Prediction

The final predictor takes **5 current season stats** for any two teams and compares them head-to-head:

| Stat | RCB | GT |
|---|---|---|
| Wins | 11 | 11 |
| Points | 18 | 18 |
| NRR | +0.783 | +0.695 |
| Total Runs | 3108 | 3212 |
| Total Wickets | 106 | 112 |

**Predicted IPL 2026 Final Winner → GT** 🏆

---

## Tools and Libraries Used

| | |
|---|---|
| Language | Python |
| Libraries | Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost |
| Platform | Jupyter Notebook |
| Dataset | [Kaggle — IPL 2026 Complete Dataset](https://www.kaggle.com/datasets/krishd123/ipl-2026-complete-dataset) (`matches.csv` only) |

---

## Installation

```bash
uv sync
```

---


## Author

**Mitra Sreekandan**  
BE CSE, SKCT (2024–2028)

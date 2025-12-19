> **Module:** 03. Finance | **Sub-area:** Cash & Runway | **Author:** TheAuronFlux

# 03.01 - Cash & Runway: The "Zero Conjecture" Rubric

## 🔑 The Key Question (KQ)
**"If I had to decide right now, do I know EXACTLY how much capital I have, WHERE every cent is located, its LIQUIDITY status, and can I PROVE it within 5 minutes?"**

> **Hard Constraint:** Proof Time (RTO) must be **≤ 5 minutes** with organized statements/screenshots.

---

## 📊 The 80/20 Metrics (Hard Data)

### Outcome Metrics
1.  **Total Cash:** Sum of liquid accounts (excluding credit).
2.  **Immediate Liquidity Index (ILI):** % of cash in **T+0** (immediate redemption).
3.  **Age of Balance (h):** Hours since the last reconciliation.
4.  **Reconciliation Error (%):** |Recorded Balance − Bank Statement Balance| / Total Cash.

### Data Quality Metrics
5.  **Account Coverage (%):** Mapped accounts ÷ Existing accounts.
6.  **Restriction Documentation:** Are withdrawal limits/locks noted? (Binary: 1/0).
7.  **RTO (Recovery Time Objective):** Time required to gather the last 30 days of proof.

---

## 📐 Scoring Algorithm (0–100)

To achieve a score of **100**, the user must satisfy the following rubric. The system applies specific penalties for failures.

| Block | Weight | Criteria for MAX Score (100) |
| :--- | :---: | :--- |
| **Coverage** | **25 pts** | 100% of existing accounts mapped with **Name, Type, and Balance**. |
| **Freshness** | **20 pts** | **Age of Balance ≤ 24h** (weighted by volume). |
| **Accuracy** | **20 pts** | **Reconciliation Error ≤ 1%** (vs. current statements). |
| **Liquidity** | **20 pts** | 100% of balances tagged with Liquidity (T+0, T+1, T+7) & Type (OpEx/Reserves/Tax). |
| **Evidence** | **15 pts** | "Monthly Proof" folder exists with statements; **RTO < 2h**. |

### ⛔ Automatic Circuit Breakers (The Logic Traps)
* **IF** Age > 48h $\rightarrow$ **0 pts** in Freshness.
* **IF** Error > 2% $\rightarrow$ **0 pts** in Accuracy.
* **IF** Proof Time > 5 min $\rightarrow$ **KQ Status = FAIL** (The entire score is invalidated).

---

## ✅ The "Green State" Thresholds
To pass the audit (Score > 80), you must meet:
* [ ] **KQ Answer:** YES (Proof $\le$ 5 min).
* [ ] **Coverage:** 100%.
* [ ] **Freshness:** $\le$ 24h.
* [ ] **Error:** $\le$ 1%.
* [ ] **ILI:** $\ge$ 60% (Recommended floor for independent operators).

---

## ⚠️ Anti-Delusion Rules (What is NOT Cash)
1.  **Credit Limits:** Credit cards, overdrafts, or loans are **NOT** cash.
2.  **Receivables:** Invoices or "Promised Payments" without bank entry are **NOT** cash.
3.  **Volatile Assets:** Crypto/Stocks only count if Liquidation is **$\le$ T+1** AND Proof of Sale is possible.

---

*Protocol 1728 - Property of TheAuronFlux*

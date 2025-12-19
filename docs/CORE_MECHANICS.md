# Core Mechanics & Axioms

> **Classification:** System Logic / Kernel Rules
> **Version:** 1.0 (Immutable Core)

## 1. The Meta-Pareto Principle (The 64/4 Filter)

The Protocol rejects the standard distribution of effort. It operates exclusively within the **Recursive Pareto Frontier**.

### 1.1 Mathematical Derivation
Traditional optimization relies on the Pareto Principle ($P^1$), where $20\%$ of inputs generate $80\%$ of outputs. Protocol 1728 applies a recursive function ($P^2$) to isolate the signal from the noise:

$$
P(P(x)) \Rightarrow 20\% \text{ of } 20\% = \mathbf{4\% \text{ of Inputs}}
$$

Consequently, the yield is compounded:
$$
80\% \text{ of } 80\% = \mathbf{64\% \text{ of Outputs}}
$$

### 1.2 The "Meta-Pareto" Threshold
In the context of Human Metrology (Protocol 1728), a variable is only considered valid if it belongs to this critical $4\%$ quantile.
* **Rule:** Any metric that contributes less than high-magnitude leverage is discarded as "Legacy Noise".
* **Application:** We do not track "good habits". We track **Meta-Pareto Variables**—the minimal effective dose that sustains the bio-psychosocial system.

---

## 2. The Key Question (KQ) Architecture

In this Protocol, a **Key Question (KQ)** is not an interrogative sentence. It is a **Deterministic Function** designed to audit a specific node of the human system.

### 2.1 Anatomy of a KQ
Every KQ must satisfy the following **CID (Consistency, Integrity, Data)** properties:

1.  **Binary or Numeric Output:** Subjective answers ("I feel good") are forbidden. The output must be a Boolean (`TRUE/FALSE`) or a Scalar Integer (`0-100`).
2.  **RTO (Recovery Time Objective):** Evidence for the answer must be retrievable in **$\le$ 5 minutes**.
3.  **Falsifiability:** The claim must be capable of being proven false by an external auditor using Hard Data.

### 2.2 The KQ Execution Function
The logic flow for any KQ follows this algorithm:

```mermaid
graph LR
    A[Input Data] --> B{Logic Gate}
    B -- Data Matches Criteria --> C[Score: 100]
    B -- Data Fails Criteria --> D[Score: Penalty]
    B -- No Evidence --> E[Score: 0 (Null)]

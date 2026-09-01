# SpendDNA: Your Wallet's Year-End Story 💳🧬
> **"Spotify Wrapped for your money"** — Decoding 6 Months of Indian UPI & Banking Transactions

**Author:** Akash Kumar Das  
**Course Project:** The Unlox Academy - Industry-Graded Minor Project  
**Dataset:** `rahul_transactions.csv` (1,328 raw records, Jan 01 – Jun 30, 2024)[cite: 2]  
**Execution Environment:** Google Colab Notebook[cite: 2]

---

## 📌 Project Overview
**SpendDNA** is a zero-dependency fintech analytics pipeline that processes messy, heterogeneous Indian bank and UPI transaction statements[cite: 2]. Using only core Python, **NumPy**, and **Pandas**, the system parses, normalizes, tags, and evaluates spending habits through pure text and custom ASCII visual dashboards—without relying on external plotting libraries or advanced helper frameworks[cite: 2].

---

## 🔥 Key Features

1. **Custom Counter & ASCII Visualization Engine**[cite: 2]
   - Built-in `CustomCounter` class operating with zero reliance on standard `collections.Counter`[cite: 2].
   - Modular ASCII bar charts and table rendering utilities for terminal and Google Colab outputs[cite: 2].

2. **Heterogeneous Transaction Parser & Data Ingestion**[cite: 2]
   - Multi-format date parser handling mixed strings (`YYYY-MM-DD`, `DD/MM/YY`, `DD-Mon-YY`, `DD Mon YYYY`)[cite: 2].
   - Regex-free currency normalization accommodating `₹`, `Rs.`, commas, and raw floats[cite: 2].
   - Achieves 100% parsing fidelity (0 unparseable dates, 0 unparseable amounts, and 18 duplicate rows pruned)[cite: 2].

3. **Merchant Normalization & Categorization Tagger**[cite: 2]
   - Maps raw bank narrations (`BUNDL`, `KIRANAKART`, `AVENUE SUPERMARTS`) to 41 unique canonical vendors and 12 core spending categories[cite: 2].
   - Categorizes special non-consumption ledger items including P2P transfers, cash withdrawals, rent, and salary[cite: 2].

4. **Financial KPI Executive Summary**[cite: 2]
   - Calculates Total Inward Credits, Outward Debits, Net Cash Flow (Burn Rate), and Personal Savings Rate[cite: 2].

5. **Monthly Trend & Category Trajectory Analysis**[cite: 2]
   - 6-Month Category Matrix generated via `pivot_table` with pure NumPy month-over-month growth rate computations[cite: 2].

6. **Temporal & Behavioral Insights**[cite: 2]
   - Uncovers lifestyle habits such as late-night food delivery orders (9 PM – 2 AM) and morning coffee runs (8 AM – 11 AM)[cite: 2].
   - Evaluates weekday vs. weekend spending burn rates[cite: 2].

7. **Category-Specific Anomaly Detection Engine**[cite: 2]
   - Detects statistical anomalies ($Z > 2.0$ and $Z > 3.0$) computed *within individual spending categories* to prevent global threshold bias[cite: 2].

8. **Quantitative Spending Archetype Evaluation**[cite: 2]
   - Evaluates transactions against 10 behavioral archetypes (e.g., *The Foodie*, *The Quick Commerce Junkie*, *The Shopaholic*, *The Late-Night Snacker*, *The YOLO Spender*, and *The Pavement Coffee Connoisseur*)[cite: 2].

9. **Spend Forecasting via Rolling NumPy Average**[cite: 2]
   - Projects next-month (July 2024) expected category outlays using a rolling 3-month NumPy mean arithmetic model[cite: 2].

---

## 🛠 Tech Stack & Dependencies

- **Language:** Python 3.x
- **Data Manipulation:** `pandas==2.2.3`, `numpy==2.1.3`
- **Visuals & Tables:** Pure Text & Custom ASCII Engine (Zero external plotting dependencies)

---

## 🚀 Quick Start & Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/SpendDNA.git](https://github.com/your-username/SpendDNA.git)
   cd SpendDNA

# Trader Behavior Insights Based on Market Sentiment

## Overview
This repository contains an analysis of the relationship between trader performance and Bitcoin market sentiment.  
Using Hyperliquid trade data and the Bitcoin Fear & Greed Index, the goal is to uncover patterns and insights that can help design smarter trading strategies.

**Internship Objective:**  
> Explore the relationship between trader performance and market sentiment, uncover hidden patterns, and deliver insights that can drive smarter trading strategies.

---

## Repository Structure

📦 trader-sentiment-analysis/
│

├── README.md 

├── Trader_Sentiment_Analysis.ipynb 

├── Trader_Sentiment_Report.pdf 

│

├── 📂 data/

│ ├── historical_data.csv ← Hyperliquid trade dataset (see download link below)

│ ├── fear_greed_index.csv ← Bitcoin Fear & Greed Index dataset (see download link below)

│

├── 📂 outputs/

│ ├── processed_trades.csv ← Cleaned/merged trade data

│ ├── sentiment_merged.csv ← Trades merged with sentiment

│
└── 📂 figures/

├── figure1_daily_pnl.png ← Daily total PnL by sentiment

├── figure2_winrate_by_sentiment.png ← Win rate by sentiment


---

## Data Access

**Note:** The CSV files are large (>25 MB) and cannot be uploaded directly to GitHub. Download them using the links below:

- **Historical Trades CSV:** [Download Link] (https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view)
- **Fear & Greed Index CSV:** [Download Lin]  (https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view)


---

## Methodology

1. **Data Cleaning:** Standardized column names, converted timestamps to datetime, and filtered valid accounts.  
2. **Feature Engineering:** Created `is_win`, `trade_return`, `side_encoded`, and `notional`.  
3. **Data Merging:** Joined trading data with sentiment by date.  
4. **Exploratory Analysis:**  
   - Win rate by sentiment  
   - Daily total closed PnL by sentiment  
   - Statistical tests (T-test, Mann–Whitney U, Cohen’s d)  
5. **Insights Generation:** Identified performance patterns and statistical significance.

---

## Key Findings

- Win rate is higher during Greed periods than Fear (0.446 vs 0.415).  
- Statistical significance:  
  - T-test p-value = 9.42 × 10⁻⁷  
  - Mann–Whitney p-value = 3.53 × 10⁻³⁴  
- Effect size (Cohen’s d) = 0.029 → small but meaningful.  
- Visualizations:  
  - **Figure 1:** Daily total PnL by sentiment  
  - **Figure 2:** Win rate by sentiment  

---

## How to Run

1. Open `Trader_Sentiment_Analysis.ipynb` in Google Colab.  
2. Upload the downloaded CSVs into the `data/` folder in Colab.  
3. Run all cells sequentially.  
4. Outputs and charts will be saved in `outputs/` and `figures/` folders.

---

## Deliverables for Internship Submission

- **Colab Notebook** – complete, runnable, and reproducible.  
- **PDF Report** – polished insights report with figures and interpretations.  
- **Outputs Folder** – contains cleaned/merged CSV files.  
- **Figures Folder** – contains plots included in the report.

---

## Notes

- Analysis focuses on descriptive statistics and patterns rather than predictive modeling.  
- Charts and aggregates are generated with Python (pandas, matplotlib, seaborn).  
- Sentiment is analyzed on a daily basis, not intraday.

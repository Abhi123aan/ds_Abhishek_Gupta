# Trader Behavior Analysis Using Crypto Fear & Greed Index

This project analyzes the relationship between Bitcoin market sentiment (measured by the [Crypto Fear & Greed Index](https://alternative.me/crypto/fear-and-greed-index/)) and intraday trader performance on the **Hyperliquid** platform. The study validates whether psychological market regimes influence profitability, risk management, and trading efficiency.

##  Project Overview
The objective is to explore how market sentiment affects trader behavior. Key questions addressed include:

* **Profitability:** How does average PnL (Profit and Loss) vary across sentiment regimes?
* **Win Rate:** Are traders more likely to close profitable trades during "Fear" or "Greed"?
* **Risk Behavior:** How does trade size change relative to a trader's historical average during different moods?
* **Efficiency:** How effectively is capital converted into profit per dollar traded?

##  Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / Google Colab

##  Dataset Description
The analysis merges two primary data sources:
1.  **Fear & Greed Index:** Daily market sentiment classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
2.  **Historical Trader Data:** Intraday trade-level logs from Hyperliquid, including `Closed PnL`, `Size USD`, `Side`, and `Account` IDs.

##  Key Features Engineered
* **Win Indicator:** A binary feature identifying profitable vs. non-profitable trades.
* **Profit Efficiency:** Realized profit normalized by trade size (`PnL / Size USD`).
* **Relative Risk:** The ratio of a specific trade size to that trader’s historical average size.

##  Summary of Findings
* **Sentiment Impact:** Statistical testing confirms that sentiment has a measurable impact on trading outcomes.
* **Profitability Trends:** Average PnL is highest during **Extreme Greed** ($67.89) and lowest during **Extreme Fear** ($34.54).
* **Win Rates:** Traders experience higher win rates during **Extreme Greed** (~46.5%) compared to **Extreme Fear** (~37.1%).
* **Efficiency:** Profit efficiency tends to improve during **Fear-driven** markets, suggesting more cautious or selective entry points.
* **Risk Behavior:** Risk-taking (trade size) increases significantly during **Greed** and **Extreme Greed** regimes.

##  Strategic Implications
* **Risk Control:** Risk management should be tightened during "Greed" phases to protect against sudden reversals.
* **Position Sizing:** Sentiment data can be incorporated into dynamic position sizing models.
* **Contrarian Opportunities:** Fear-driven markets may offer better risk-adjusted opportunities for disciplined traders.

##  How to Run
1.  Clone the repository.
2.  Ensure CSV data files are placed in the `/content/csv_files/` directory(please ensure the path, this path is for my machine so please make change accoring to that).
3.  Install dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
4.  Run the notebook `Data_Abhishek.ipynb` to view the full analysis.

---
*Created by Abhishek*

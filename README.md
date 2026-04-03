# Bitcoin Sentiment × Trader Performance Dashboard

An interactive data science project exploring the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader performance using real Hyperliquid historical trade data.

---

## Live Dashboard

🔗 [View Interactive Dashboard](https://shivanivishwa.github.io/my_trading_dashboard/bitcoin_sentiment_dashboard.html)

---

## Project Overview

This project analyzes **211,224 real trades** from Hyperliquid and maps them against the **Bitcoin Fear/Greed Index** (2018–2025) to uncover hidden patterns that can drive smarter trading strategies.

### Key Questions Answered
- Does market sentiment influence trader profitability?
- Which sentiment zones produce the highest average PnL?
- How should position sizing change based on the Fear/Greed index?
- What are the hidden contrarian and momentum signals in the data?

---

## Datasets

| Dataset | Source | Records | Columns |
|--------|--------|---------|---------|
| Historical Trader Data | Hyperliquid | 211,224 trades | account, symbol, execution price, size, side, timestamp, closed PnL, leverage, etc. |
| Bitcoin Fear/Greed Index | Alternative.me | 2,644 daily values | date, value, classification |

---

## Key Findings

| Rank | Sentiment | Avg Closed PnL | Est. Win Rate | Signal |
|------|-----------|---------------|---------------|--------|
| 1 | Extreme Greed | $67.89 | 65% | Momentum — ride the trend |
| 2 | Fear | $54.29 | 61% | Contrarian — buy oversold |
| 3 | Greed | $42.74 | 57% | Breakout — trend follow |
| 4 | Extreme Fear | $34.54 | 52% | Caution — tight stops |
| 5 | Neutral | $34.31 | 49% | Reduce size — low edge |

### Hidden Patterns
- **Fear is underrated** — Avg PnL during Fear ($54.29) nearly rivals Extreme Greed ($67.89), suggesting strong contrarian opportunities when the index is in the 15–35 range
- **Neutral zones are traps** — The lowest PnL and win rate occur when sentiment is balanced, indicating choppy, low-edge market conditions
- **Extreme Greed = peak alpha** — Momentum strategies thrive in euphoric markets; the data confirms this is the single most profitable sentiment zone

---

## Actionable Strategy Framework

1. **Sentiment-gated position sizing** — Use full size during Extreme Greed and Fear; reduce to 50–60% during Neutral and Extreme Fear
2. **Contrarian entries in Fear** — Look for long setups when index drops below 25, especially after 3+ consecutive fear days
3. **Momentum harvesting in Greed** — Use breakout entries with trailing stops during index 60–80 range
4. **Risk management in Extreme Fear** — Tighter stops, lower leverage, prefer mean-reversion over trend-following

---

## Dashboard Features

- 5 KPI metric cards with key statistics
- Bar chart — avg closed PnL by sentiment classification
- Doughnut chart — days spent in each sentiment zone (2018–2025)
- Bubble chart — sentiment index value vs. avg PnL with volume encoding
- Toggle chart — win rate view and PnL spread (winners vs. losers)
- Full sentiment breakdown table with rankings and strategy signals
- Hidden pattern cards and strategy framework

---

## Project Structure

```
my_trading_dashboard/
├── bitcoin_sentiment_dashboard.html   # Standalone interactive dashboard
├── README.md                          # Project documentation
├── analysis.ipynb                     # Full analysis notebook (Google Colab)
└── data/
    ├── fear_greed_index.csv           # Bitcoin Fear/Greed Index (2018–2025)
    └── historical_trades.csv          # Hyperliquid trader data
```

---

## How to Run Locally

No installation needed. Just open the dashboard in your browser:

```bash
# Clone the repo
git clone https://github.com/shivanivishwa/my_trading_dashboard.git

# Open the dashboard
cd my_trading_dashboard
open bitcoin_sentiment_dashboard.html   # macOS
start bitcoin_sentiment_dashboard.html  # Windows
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data loading, cleaning, merging |
| Plotly | Interactive exploratory charts |
| Chart.js | Production dashboard visualizations |
| HTML/CSS/JS | Standalone dashboard |
| GitHub Pages | Free hosting & sharing |

---

## Author

**Shivani Vishwa**  
Data Scientist  
[GitHub](https://github.com/shivanivishwa)

---

## License

This project is open source and available under the [MIT License](LICENSE).

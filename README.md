# Crypto_Sentiment_Trader_Analysis

Analyzing the relationship between Bitcoin Fear & Greed sentiment and trader performance on Hyperliquid — uncovering patterns across 211K trades, 32 traders, and 2 years of market data.

---

## Dataset
| | |
|---|---|
| **Trades** | 211,224 |
| **Traders** | 32 unique wallets |
| **Coins** | 246 |
| **Period** | May 2023 — May 2025 |
| **Sources** | Hyperliquid historical data + Bitcoin Fear/Greed Index |

---

## Key Findings

### 📊 Overall Performance
- **Total Realized PnL:** $10,296,958
- **Overall Win Rate:** 41.1%
- The low win rate vs high total PnL reveals an **asymmetric strategy** — traders win rarely but win big

---

### 😱 Sentiment vs Performance

![Trade Count and Avg PnL by Sentiment](Assets/g2.png)

| Sentiment | Trades | Avg PnL | Win Rate |
|---|---|---|---|
| Extreme Fear | 21,400 | $34.54 | 37.1% |
| Fear | 61,837 | $54.29 | 42.1% |
| Neutral | 37,686 | $34.31 | 39.7% |
| Greed | 50,303 | $42.74 | 38.5% |
| **Extreme Greed** | 39,992 | **$67.89** | **46.5%** |

> **Extreme Greed** produces the highest avg PnL and win rate — market euphoria is the most profitable environment.

---

### 📈 BUY vs SELL by Sentiment

![BUY vs SELL by Sentiment](Assets/g6.png)

- SELL trades during Extreme Greed average **$114.58 PnL** — the strongest signal in the entire dataset
- BUY during Extreme Greed averages only **$10.50** — chasing euphoria is the worst entry
- Traders instinctively close longs and short into rallies

---

### 🏆 Trader Leaderboard

![Top 15 Traders Heatmap](Assets/g3.png)

| Rank | Address | Total PnL | Win Rate | Style |
|---|---|---|---|---|
| 1 | 0xb123...ed23 | $2,143,382 | 34% | Momentum |
| 2 | 0x0833...9012 | $1,600,229 | 36% | Contrarian |
| 3 | 0xbaaa...7864 | $940,163 | 47% | Mixed |
| ✦ | 0x75f7...70d4 | $379,095 | **81%** | Smart Money |
| ✦ | 0x2c22...11dd | $168,658 | 52% | Smart Money |

> ✦ Smart Money = win rate ≥ 50% with 50+ trades. Only **3 out of 32 traders** qualify.

---

### ⏳ Sentiment Streak Effect

![Avg PnL by Streak Length](Assets/g4.png)

- After **7 consecutive days** of the same sentiment, avg PnL spikes to **$155.76**
- Market conviction builds over a week — day 7 of a streak is a reliable entry signal
- Day 5 streaks go negative — a dip before the breakout

---

### 🪙 Coin Performance by Sentiment

![Coin Sentiment Heatmap](Assets/g1.png)

| Coin | Best Sentiment | Avg PnL | Worst Sentiment |
|---|---|---|---|
| ETH | Fear | $236.9 | Extreme Greed (-$20.8) |
| SOL | Greed | $284.8 | Extreme Fear (+$56) |
| MELANIA | Extreme Fear | $218.3 | Extreme Greed (-$70.4) |
| BTC | Fear | $48.9 | Stable across all |
| FARTCOIN | — | — | Extreme Fear (-$244.3) ⚠️ |

---

## Strategy Signals

| Signal | Avg PnL | Win Rate | Verdict |
|---|---|---|---|
| Buy on Extreme Fear | $34.11 | 20.2% | High risk contrarian play |
| Buy on Extreme Greed | $10.50 | 31.1% | ❌ Worst setup |
| **Sell on Extreme Greed** | **$114.58** | — | ✅ Strongest edge |
| **7-Day Streak Entry** | **$155.76** | — | ✅ Strong timing signal |

---

## Tools Used
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

---

*Submitted as part of PrimeTrade.ai Data Science hiring assignment — April 2026*

# 📈 AI Stock Predictor

An AI-powered stock market simulator built with Streamlit, Yahoo Finance, and Claude (Anthropic). Browse every stock in the **Dow Jones 30**, **S&P 500**, or **NASDAQ-100**, analyze technicals and fundamentals in real time, run a Monte Carlo price forecast, and ask an AI assistant natural-language questions to discover stocks that match your investment criteria.

---

## Features

### 📊 Stock Detail
- **Candlestick price chart** with Bollinger Bands, SMA 20, SMA 50, RSI, and Volume subplots
- **Monte Carlo 30-day forecast overlay** — 500 simulation paths shown as probability bands (10–90% and 25–75%) in purple
- **6 live metrics** — RSI, P/E, Forward P/E, Annualized Volatility, 52-Week High/Low
- **Technicals tab** — MACD chart, Bollinger Band position, SMA crossover signals, Beta
- **Fundamentals tab** — Valuation, growth, profitability, balance sheet, and Wall Street consensus
- **News tab** — Latest headlines with clickable source links
- **Full AI Analysis** — Claude streams a detailed research report covering technicals, fundamentals, news impact, bull/bear case, price target, and top risks

### 🌐 Index Overview
- Batch price snapshot for all stocks in the selected index
- **Market cap heatmap** (treemap) — sized by market cap, colored by daily % change
- Full sortable data table with Day % and 5-Day % change
- Top 3 gainers and losers for the day

### 🤖 AI Assistant
- Ask natural language questions like:
  - *"Show me technology stocks expected to grow more than 200% in the next year"*
  - *"Which stocks are the most undervalued right now?"*
  - *"Find defensive dividend stocks with low volatility"*
- Claude scans the active index and streams a detailed response identifying matching stocks
- **One-click load** — recommended stocks load directly into the simulator

---

## Tech Stack

| Layer | Tools |
|---|---|
| UI | [Streamlit](https://streamlit.io) |
| Market Data | [yfinance](https://github.com/ranaroussi/yfinance) (Yahoo Finance) |
| AI / Analysis | [Anthropic Claude](https://anthropic.com) (`claude-opus-4-7`, adaptive thinking, streaming) |
| Charts | [Plotly](https://plotly.com/python/) |
| Data | [pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/) |
| S&P 500 Components | Wikipedia (cached 24h) |

---

## Setup

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/stock-predictor.git
cd stock-predictor
```

### 2. Install dependencies
```bash
pip install streamlit yfinance anthropic pandas numpy plotly requests
```

> **Note:** Requires Python 3.10+. If you're using Anaconda, prefix commands with `/opt/anaconda3/bin/`.

### 3. Add your Anthropic API key

Get a free API key at [console.anthropic.com](https://console.anthropic.com).

```bash
echo "sk-ant-your-key-here" > .api_key
```

Or set it as an environment variable:
```bash
export ANTHROPIC_API_KEY=sk-ant-your-key-here
```

> The AI analysis and assistant features require an API key. The charts and data work without one.

### 4. Run the app
```bash
streamlit run app.py
```

---

## Usage

1. **Select an index** from the sidebar — Dow Jones 30, S&P 500, or NASDAQ-100
2. **Search or browse** stocks using the search bar and dropdown
3. **Explore the charts** — toggle the 30-day Monte Carlo forecast with the checkbox above the chart
4. **Run a full AI analysis** — click *⚡ Generate Full Analysis* for a streaming research report
5. **Use the AI Assistant** — describe what you're looking for and Claude will find matching stocks and load them into the simulator

---

## Screenshots

> *Add screenshots here*

---

## Disclaimer

This tool is for **educational and informational purposes only**. Nothing in this application constitutes financial advice. Always do your own research before making investment decisions.

---

## License

MIT

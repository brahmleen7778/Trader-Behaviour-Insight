# Trader Behavior Insights: Market Sentiment vs Trading Performance

## Project Overview

This project analyzes how **market sentiment (Fear vs Greed)** influences **trader behavior and performance** using historical trading data from Hyperliquid and Bitcoin market sentiment data.

The goal is to understand whether trader profitability, activity, and risk-taking patterns change under different sentiment conditions and to generate actionable strategy insights.

---

## Datasets Used

### 1. Bitcoin Market Sentiment Dataset

Contains daily sentiment classification:

* Date
* Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

### 2. Historical Trader Data (Hyperliquid)

Contains trading activity data such as:

* Account
* Execution Price
* Size (USD)
* Side (Buy/Sell)
* Closed PnL
* Timestamp
* Start Position
* Fees

---

## Methodology

### Data Preparation

* Loaded both datasets using pandas
* Checked for missing values and duplicates
* Standardized column names
* Converted timestamps to datetime
* Created a daily **date** column
* Merged trader data with sentiment data on date
* Removed rows without matching sentiment

---

### Key Metrics Created

* Daily PnL per trader
* Win rate
* Average trade size
* Trades per day
* Position size proxy (start position)

---

## Analysis Performed

### Performance vs Sentiment

Compared:

* Average PnL
* Total PnL
* Win rate

across sentiment categories.

---

### Trader Behavior Analysis

Examined:

* Trade frequency by sentiment
* Average trade size by sentiment
* Average position size
* Win rate differences

---

### Trader Segmentation

Traders were segmented into:

**Activity Segment**

* Frequent traders
* Occasional traders

**Profitability Segment**

* Profitable traders
* Losing traders

**Trade Size Segment**

* Large position traders
* Small position traders

---

## Key Insights

1. Trader profitability is highest during **Extreme Greed** sentiment periods.
2. Trading activity increases during **Fear** market conditions.
3. Larger trade sizes are associated with significantly higher average PnL.
4. Win rates tend to decline during **Extreme Fear** periods.

---

## Strategy Recommendations

**Strategy 1**
Reduce position sizes during Extreme Fear sentiment periods to manage risk.

**Strategy 2**
Increase participation during Extreme Greed periods where profitability and win rates are higher.

---

## Tools Used

* Python
* Pandas
* Matplotlib
* Jupyter Notebook

---

## How to Run

1. Clone the repository
2. Install dependencies:

```
pip install pandas matplotlib
```

3. Open the notebook:

```
jupyter notebook Trader_Behavior_Insights.ipynb
```

---

## Project Structure

```
Trader-Behavior-Insights/
│
├── Trader_Behavior_Insights.ipynb
├── README.md
└── charts/
```


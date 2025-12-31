# Data Science Project: Trading Behavior vs Market Sentiment Analysis

##  Project Overview
This project analyzes the relationship between cryptocurrency trader behavior and Bitcoin market sentiment (Fear & Greed Index) to identify patterns, divergences, and strategic trading opportunities.

### **Key Question:**
> "How does trading behavior (profitability, risk, volume, leverage) align or diverge from market sentiment (fear vs greed), and what hidden signals can inform smarter trading strategies?"

##  Datasets Used

### 1. **Hyperliquid Historical Trader Data**
 **Source:** Provided trading dataset
 **Key Columns:**
  - `account`, `symbol`, `execution price`, `size`
  - `side` (buy/sell), `time`, `start position`
  - `closedPnL` (profit/loss), `leverage`, `event`
**Purpose:** Analyze actual trading behavior patterns

### 2. **Bitcoin Fear & Greed Index**
 **Source:** Alternative.me Fear & Greed Index
 **Key Columns:**
   `Date`, `Classification` (Fear/Greed)
 **Purpose:** Measure market sentiment extremes

##  Analysis Performed

### **Core Analysis Areas:**
1. **Profitability vs Sentiment** - Do traders make more money during fear or greed?
2. **Risk (Leverage) Analysis** - How does risk-taking change with sentiment?
3. **Trading Volume Patterns** - Does activity align with sentiment?
4. **Hidden Signals** - Identifying contrarian opportunities

### **Key Techniques:**
- Time series merging & alignment
- Statistical correlation analysis
- Comparative visualization (fear vs greed periods)
- Pattern recognition in trading behavior
- Strategic recommendation development

##  How to Run This Project

###  Google Colab (**
1. **Upload data to Google Drive** in folder `csv_files/`
2. **Open** `notebook_1.ipynb` in Google Colab
3. **Mount Google Drive:**
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
4. **Update file paths:**
   ```python
   trader_data = pd.read_csv('/content/drive/MyDrive/csv_files/historical_trader_data.csv')
   ```
5. **Run all cells sequentially**

## 📈 Key Findings Summary

### **Major Insights:**
1. **Contrarian Profitability:** Traders tend to be more profitable during **Fear** periods
2. **Risk Mismatch:** Highest leverage used during **Greed** periods (overconfidence)
3. **Volume-Sentiment Alignment:** Trading activity spikes with greed sentiment
4. **Quality-Quantity Tradeoff:** More trades ≠ better results during greed

### **Statistical Highlights:**
- **Correlation (Sentiment vs Profit):** 
1. Sentiment & Profit Correlation: -0.117
   → Negative correlation
2. Sentiment & Volume Correlation: -0.130
   → Weak relationship
- **Volume Multiplier (Fear→Greed):** 0.4x times higher
- **Win Rate Difference:** 18.6% higher during fear periods

##  Trading Strategy Recommendations

### **Strategy 1: Fear-Exploitation**
- **When:** Fear Index > Threshold
- **Action:** Increase position size
- **Risk:** Moderate leverage (X.XX max)
- **Exit:** Shift to greed sentiment

### **Strategy 2: Greed-Defensive**
- **When:** Greed Index > Threshold
- **Action:** Reduce position sizes
- **Risk:** Lower leverage, take profits
- **Focus:** Capital preservation

### **Strategy 3: Sentiment-Aware Risk Management**
- Dynamic leverage caps based on sentiment
- Position sizing adjusted for sentiment phase
- Profit-taking schedules tied to sentiment shifts

##  Output Files Generated

 `profit_vs_sentiment.png` , 4-panel chart showing profit, volume, and trade patterns , Visual comparison of key metrics 
 `leverage_vs_sentiment.png` , Leverage statistics and distribution , Risk analysis visualization 
 `trading_patterns_time_series.png` ,Time series of sentiment, profit, volume , Pattern recognition over time 
 `ds_report.pdf` , Comprehensive analysis report , Final insights and recommendations 




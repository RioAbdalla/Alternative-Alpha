# Unveiling Alpha in DeFi Markets

## 📌 Project Overview
This project develops a **modular, agent-based framework** for predicting DeFi token performance using **alternative data** and **machine learning**.  

The framework integrates **data acquisition, feature engineering, factor validation, predictive modeling, and portfolio backtesting** into a scalable architecture. It systematically evaluates whale activity, exchange flows, social sentiment, and ownership concentration as predictive signals for token-level returns.  

Our approach consistently outperforms benchmarks such as the **DeFi Pulse Index (DPI)**, highlighting the potential of interpretable ML models in decentralized finance.

---

## 📊 Methodology
1. **Data Acquisition Agent**  
   - Sources token-level alternative data from Santiment (36 tokens, 2023–2025).  
   - Features include whale transactions, exchange inflows/outflows, sentiment, social volume, and development activity.  

2. **Feature Engineering & Validation**  
   - Applied z-score, log+z-score, and rank transforms for comparability.  
   - Validated predictive signals using Information Coefficient (IC), quantile return spreads, and regression analysis.  

3. **Predictive Modeling**  
   - Cross-sectional **XGBoost classifier** trained on rolling 60-day windows.  
   - Tokens ranked daily by predicted probability of positive returns.  
   - Long-short portfolios constructed across multiple quantile cutoffs and holding periods.  

4. **Portfolio Backtesting**  
   - Rolling out-of-sample evaluation with 7–30 day horizons.  
   - Benchmarked against equal-weight portfolios, logistic regression models, and the DeFi Pulse Index.  
   - Evaluated with Sharpe ratio, drawdown, and cumulative return metrics.  

---

## 📈 Key Results
- **Alpha Generation**: ML-driven portfolios achieved higher Sharpe ratios (up to 1.15) than benchmarks.  
- **Dominant Signals**: Whale activity and exchange flows are the strongest predictors; sentiment adds timing power.  
- **Robustness**: Results consistent across multiple portfolio configurations (Top-N/Bottom-N, holding periods).  
- **Outperformance**: ML portfolios exceeded both passive equal-weight and DPI benchmarks.  

---

## 🛠️ Tech Stack
- **Python** (Jupyter Notebooks)  
- Libraries: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `matplotlib`, `seaborn`  
- **Data Source**: Santiment API (DeFi tokens, 2023–2025)  

---

## 📂 Repository Structure
```
├── Data_Fetching_Agent_and_Others_Application_2_0.ipynb   # Data acquisition and preprocessing agent
├── notebooks/                                            # Feature engineering, modeling, and backtesting
├── FIN580_Final_Project_Paper.pdf                        # Full academic paper
└── README.md                                             # Project documentation
```

---

## 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/defi-alpha-prediction.git
   cd defi-alpha-prediction
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn xgboost matplotlib seaborn
   ```
3. Run the notebook(s) for factor analysis and backtesting:
   ```bash
   jupyter notebook Data_Fetching_Agent_and_Others_Application_2_0.ipynb
   ```

---

## 🤝 Contributors
- Qingwen He  
- Damario Abdalla  
- Jingwen Hu  
- Paul Shi  

---

## 📜 License
Add your chosen license here (MIT recommended if open-source).  

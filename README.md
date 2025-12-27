# NBA Player Performance Backtesting Framework

### Project Overview
A predictive modeling engine designed to backtest various player projection strategies. The framework simulates historical game logs and betting lines to identify the most reliable statistical indicators (e.g., 5-game vs. 15-game rolling averages) for predicting future player output.

### 🔧 Key Technical Competencies
* **Parameter Optimization (Grid Search):** Automated testing of multiple rolling windows (5, 10, 15 games) and adjustment variables to maximize predictive accuracy.
* **Synthetic Data Generation:** Developed a robust simulation module to generate realistic player game logs and odds data for framework stress-testing (overcoming web scraping API limitations).
* **Contextual Filtering:** Implemented logic to filter performance projections based on "Game Script" environments (e.g., High Total / Close Spread games).

### 📊 Methodology & Results
* **Objective:** To determine the optimal "Lookback Window" for projecting player 3-point efficiency (FG3M).
* **Data Architecture:** Refactored project to decouple configuration data from logic. Player attributes and odds configurations are loaded dynamically from external JSON files (`players.json` and `team_odds_config.json`), demonstrating modular software design.
* **Result:** Identified that a **15-game rolling average** (with a -3.0 volatility adjustment) provided the highest stability in High-Total game environments (>93% hypothetical accuracy).

### 🛠 Tools Used
* **Languages:** Python (Pandas, NumPy)
* **Development:** Google Colab, AI-Assisted Prototyping (LLM) for rapid syntax generation and logic validation.

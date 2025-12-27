# NBA Parlay Strategy Engine

### Project Overview
A quantitative research framework designed to identify and validate "Parlay Edges" in NBA player prop markets. Unlike traditional models that focus on single-bet Expected Value (EV), this engine simulates player variance to find highly correlated, low-volatility statistical trends and mathematically proves how combining them maximizes ROI against standard bookmaker odds.

### 🔧 Key Technical Competencies
* **Simulation & Synthetic Data:** Built a robust data generator to create "Dummy Game Logs" and odds, allowing for high-volume backtesting of strategies without relying on fragile external APIs.
* **Grid Search Optimization:** Implemented a forecasting engine that tests thousands of parameter combinations (Rolling Window, Adjustment Factor, Spread Threshold) to find the most predictive trend lines.
* **Parlay Math Validation:** Custom logic that calculates the "True Probability" of a multi-leg parlay vs. "Implied Market Probability" to quantify the exact mathematical edge.

### 📊 Methodology & Results

#### 1. Simulation Engine (Current Codebase)
* **Objective:** To stress-test the mathematical framework using high-volume synthetic data.
* **Findings:** Validated that "safe" adjusted lines (e.g., 15-game average minus 3.0) can maintain hit rates above 95% in controlled variance environments.
* **The Parlay Edge:** Validated that combining 3 high-confidence legs creates a composite wager that drastically outperforms the 50% implied probability of standard market odds.

#### 2. Real-World Validation (Historical Execution)
* **Process:** Prior to automating this engine, I executed this strategy using manually aggregated data from actual NBA seasons, processing hundreds of game logs via CSV.
* **The "Winning Formula":** I successfully identified and executed a 4-Leg Correlation Strategy that consistently outperformed the house edge:
    * **Leg 1 (FG3M):** 94% Historical Hit Rate
    * **Leg 2 (FG3M):** 94% Historical Hit Rate
    * **Leg 3 (Rebounds):** 80% Historical Hit Rate
    * **Leg 4 (Assists):** 76% Historical Hit Rate
* **The Correlation Edge:** While independent probability suggests a ~53.7% win rate, the strong correlation between these stats pushed the **Real-World Win Rate to ~65%**.
* **The ROI:** By betting these correlated parlays at **+100 (Even Money)** odds—which imply only a 50% win probability—I secured a **15% Edge** over the sportsbook.

### 🛠 Tools Used
* **Languages:** Python (Pandas, NumPy)
* **Techniques:** Monte Carlo-style Simulation, Feature Engineering, Rolling Window Statistics
* **Architecture:** Self-Contained Notebook (No external dependencies required)

### 🚀 How to Run This Project
1. Open the notebook in Google Colab (click the badge above).
2. Run **Cell 1** to initialize the Simulation Environment (generates synthetic player data).
3. Run **Cell 2** to execute the Forecasting Grid Search.
4. Run **Cell 3** to aggregate results and identify high-confidence trend lines.
5. Run **Cell 4** to view the **Parlay Edge Calculator** results.

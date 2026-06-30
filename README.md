# NBA_Outcome_Prediction

**Author:** Raul Diaz  
**Project Status:** Active / Portfolio Piece

## 🏀 Project Overview
This project is an end-to-end data science pipeline designed to forecast NBA postseason accolades and simulate game matchups using machine learning. By transforming raw player-level performance statistics into probabilistic outcomes, the system identifies structural advantages and market inefficiencies.

### 🛠 Technical Stack
*   **Language:** Python 3.11
*   **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
*   **Environment:** Jupyter Notebook
*   **Algorithms:** Random Forest Classification, Sigmoid-based Probabilistic Mapping

---

## 🚀 Key Features

### 1. Award Prediction Model
Using a **Random Forest Classifier**, the model analyzes season-long statistical aggregates to predict the probability of a player receiving postseason honors (All-Star, All-NBA, etc.). 
*   **Precision-Focused:** Optimized for high-precision (0.75) to ensure that when the AI flags a "future award winner," the prediction is highly reliable.
*   **Feature Importance:** Automatically isolates which metrics (e.g., PTS, Star Power, AST) carry the most weight in the model's decision-making process.

### 2. Algorithmic Matchup Simulator
The engine aggregates atomic player metrics into a composite **Team-Strength Matrix**. It simulates matchups between two teams by calculating:
*   **Performance Differentials:** Scoring power, defensive disruption, and turnover efficiency.
*   **Star Power Concentration:** Uses the ML-derived award probabilities to weigh the impact of elite talent on the floor.
*   **Fair Market Odds:** Converts win probabilities into implied moneyline odds (e.g., -180, +220) to identify +EV (positive expected value) opportunities.

---

## 📊 Backtesting & Analysis
The simulation engine has been backtested against postseason data:
*   **Success:** Correctly predicted the **OKC vs. IND** Finals outcome, isolating OKC’s talent concentration as a 68% favorite.
*   **Refinement:** Post-mortem analysis of the **IND vs. NYK** series highlighted the need for a "weighted active-roster availability index" to account for real-time injuries.

---

## 📂 Installation & Usage

1. **Clone the repository:**
```bash
   git clone https://github.com/diaraul/nba-predictive-analytics.git
```
2. **Install Dependencies**
```bash
 pip install -r requirements.txt
```
3. Run the Analysis:
```
Open NBA_data.ipynb in Jupyter Notebook and execute the cells to generate fresh predictions and run the matchup simulator.

# 📊 Financial Forecasting Using Ensemble Methods: A Comparative Study  

**Author:** ERTUGRUL TUNC  
**Degree:** MSc in Data Analytics (2025)  

---

## 📖 Overview  
This repository contains the code, results, and thesis materials for my MSc research:  
**“Financial Forecasting Using Ensemble Methods: A Comparative Study.”**  

The study evaluates the effectiveness of **bagging (Random Forest), boosting (Gradient Boosting, XGBoost), and stacking ensembles** in forecasting financial time series, specifically the **S&P 500 index (2010–2024)**.  

---

## 🎯 Research Objectives  
- Compare **bagging, boosting, and stacking** with traditional forecasting methods.  
- Assess their ability to predict **stock market indices and macroeconomic trends**.  
- Identify strengths, limitations, and real-world applications of ensemble models.  

---

## 🛠️ Methodology  
- **Dataset:** S&P 500 index (2010–2024) from Yahoo Finance via `yfinance`.  
- **Features:** `Open`, `High`, `Low`, `Volume` → target: `Close`.  
- **Preprocessing:** handling missing values (forward fill), scaling, feature selection.  
- **Models:**  
  - Random Forest (Bagging)  
  - Gradient Boosting Regressor  
  - XGBoost Regressor  
  - Stacking Ensemble (Random Forest + Gradient Boosting → Ridge Regression meta-learner)  
- **Evaluation metrics:** RMSE, MAE, R².  
- **Validation:** Train-test split (80/20) + 5-fold cross-validation.  

---

## 📊 Key Findings  
- **Random Forest & Gradient Boosting** → best balance of accuracy and interpretability.  
- **XGBoost** → fastest to train and accurate on test data, but prone to **overfitting**.  
- **Stacking** → underperformed due to insufficient diversity of base learners.  
- **Feature Importance** → `High` and `Low` prices were the most predictive variables; `Volume` had minimal impact.  

---

## 🚀 How to Run  
```bash
# Clone repository
git clone https://github.com/username/thesis-repo.git
cd thesis-repo

# Install dependencies
pip install -r requirements.txt

# Run experiments
jupyter notebook "CODE.ipynb"
```

---

## 📂 Repository Structure  
```
├── README.md            # Project overview
├── thesis           # Full MSc thesis (optional upload)
├── CODE.ipynb           # Main Jupyter Notebook with experiments

## 📈 Example Results  
- Random Forest & Gradient Boosting: **R² ~ 0.55**, RMSE ~ 440.  
- XGBoost: strong test accuracy, but **negative R² in CV** (overfit).  
- Stacking: **poor performance** (negative R²).  

📌 Figures (add these in `/results/` and embed here):  
- S&P 500 Close Price vs Predictions  
- Confusion/error plots  
- Feature Importance  

---

## 🙌 Acknowledgements  
Supervised by **Dr. Maqsood Hussain Shah**.  
Thanks to the Data Analytics faculty and open-source contributors for tools such as **scikit-learn**, **xgboost**, and **yfinance**.  

---

## 🔖 License  
This repository is licensed under the **MIT License** – free to use and adapt with attribution.  

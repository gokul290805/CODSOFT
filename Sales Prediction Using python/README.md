# Sales Prediction using Machine Learning
### CodSoft Data Science Internship — Task 4

Predicts the amount of product sales based on advertising budgets across TV, Radio, and Newspaper platforms using various machine learning models.

---

## Problem Statement
Businesses need to forecast sales based on advertising expenditure to optimize their marketing strategies. This project builds and compares multiple ML models to predict sales from advertising spend data.

---

## Dataset
- **Name:** Advertising.csv
- **Source:** [Selva86 Datasets](https://raw.githubusercontent.com/selva86/datasets/master/Advertising.csv)
- **Rows:** 200
- **Columns:** TV, Radio, Newspaper, Sales

| Column | Description |
|--------|-------------|
| TV | Ad spend on TV (in $000s) |
| Radio | Ad spend on Radio (in $000s) |
| Newspaper | Ad spend on Newspaper (in $000s) |
| Sales | Units sold (in $000s) — Target Variable |

---

## Project Structure
```
sales-prediction-ml/
├── Screenshots                           # Results and Visualizations
├── Sales_Prediciton_Using_Python.ipynb   # Main notebook
├── advertising.csv                        # Dataset
├── requirements.txt                       # Dependencies
└── README.md                             # Project documentation
```

---

## Workflow

```
Load Data → EDA → Feature Engineering → Train-Test Split → Train Models → Compare → Predict
```

### Feature Engineering
| Feature | How it was created |
|---|---|
| `Total_Ad_Spend` | TV + Radio + Newspaper |
| `Sales_Category` | pd.qcut into Low / Medium / High |
| `Sales_Category_Encoded` | Low=0, Medium=1, High=2 |
| `Efficiency` | Sales / Total_Ad_Spend |

---

## Models Trained

| Model | MAE | RMSE | R² |
|-------|-----|------|----|
| Linear Regression | ~0.85 | ~1.10 | ~0.97 |
| Ridge Regression | ~0.85 | ~1.10 | ~0.97 |
| Lasso Regression | ~0.85 | ~1.10 | ~0.97 |
| Random Forest | ~0.45 | ~0.60 | ~0.99 |
| **Gradient Boosting** | **~0.40** | **~0.55** | **~0.99** |

**Best Model: Gradient Boosting** with R² ≈ 0.99

---

## Key Findings
- **TV** has the strongest impact on sales among all advertising channels
- **Newspaper** advertising has the least predictive value
- Tree-based models (Random Forest, Gradient Boosting) significantly outperform linear models
- The engineered `Efficiency` feature helped capture ROI per advertising dollar

---

## Sample Predictions (Gradient Boosting)

```python
predict_sales(tv=200, radio=40, newspaper=30)  # → ~20.8k units
predict_sales(tv=50,  radio=10, newspaper=5)   # → ~9.5k units
predict_sales(tv=300, radio=50, newspaper=60)  # → ~26.9k units
```

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/gokul290805/sales-prediction-ml.git
cd sales-prediction-ml

# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook Sales_Prediciton_Using_Python.ipynb
```

---

## Libraries Used
- pandas, numpy — Data handling
- matplotlib, seaborn — Visualizations
- scikit-learn — ML models and evaluation

---

*Developed as part of the CodSoft Data Science Virtual Internship*

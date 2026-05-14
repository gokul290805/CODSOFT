# 🚢 Titanic Survival Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

A Machine Learning project that predicts whether a passenger survived the Titanic disaster based on features like age, gender, ticket class, and fare.

---

## 📌 Project Overview

The sinking of the Titanic in 1912 is one of the most infamous shipwrecks in history. This project uses passenger data to build a classification model that predicts survival outcomes.

- **Dataset:** 891 passengers, 12 features
- **Problem Type:** Binary Classification (Survived: 0 or 1)
- **Best Accuracy Achieved:** ~82%

---

## 📂 Project Structure

```
titanic-survival-prediction/
│
├── 📓 Titanic_Survival_Prediction.ipynb
├── 📊 Titanic-Dataset.csv
├── 📸 screenshots
├── 📄 README.md
└── 📄 requirements.txt     
```

---

## 📊 Dataset Description

| Column | Description |
|--------|-------------|
| PassengerId | Unique ID for each passenger |
| Survived | 0 = Did not survive, 1 = Survived |
| Pclass | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| Name | Passenger name |
| Sex | Gender |
| Age | Age in years |
| SibSp | No. of siblings/spouses aboard |
| Parch | No. of parents/children aboard |
| Ticket | Ticket number |
| Fare | Passenger fare |
| Cabin | Cabin number |
| Embarked | Port of embarkation (C, Q, S) |

---

## 🔄 Project Workflow

```
1. Import Libraries
        ↓
2. Load Dataset
        ↓
3. Exploratory Data Analysis (EDA)
        ↓
4. Data Cleaning
        ↓
5. Feature Engineering
        ↓
6. Visualizations
        ↓
7. Train-Test Split
        ↓
8. Feature Scaling
        ↓
9. Model Training & Comparison
        ↓
10. Confusion Matrix & Evaluation
        ↓
11. Conclusion
```

---

## 🧹 Data Cleaning Steps

- Dropped irrelevant columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Imputed missing `Age` values with **median age**
- Imputed missing `Embarked` values with **mode**
- Encoded `Sex` using **LabelEncoder** (female=0, male=1)
- Encoded `Embarked` using **get_dummies** to avoid false ordering

---

## ⚙️ Feature Engineering

| New Feature | How It Was Created | Why |
|-------------|-------------------|-----|
| FamilySize | SibSp + Parch + 1 | Captures total family aboard |
| IsAlone | 1 if FamilySize == 1 | Solo travellers had lower survival |
| Fare (log) | log1p(Fare) | Reduces skewness in fare values |

---

## 📈 Visualizations Included

- ✅ Survival by gender
- ✅ Survival by passenger class
- ✅ Age distribution
- ✅ Confusion matrix heatmap

---

## 🤖 Models Used

| Model | Accuracy | CV Score |
|-------|----------|----------|
| Logistic Regression | 81.0% | 80.0% |
| Decision Tree | 79.0% | 78.0% |
| Random Forest | 82.0% | 81.0% |

> ✅ **Random Forest** performed best with ~82% accuracy

---

## 📉 Evaluation Metrics

### Best Model — Random Forest

```
                  Precision   Recall   F1-Score
Did not survive     0.85       0.88      0.86
Survived            0.79       0.74      0.76

Accuracy                                 0.82
```

### What These Mean
- **Precision** → Of all predicted survivors, how many actually survived
- **Recall** → Of all actual survivors, how many did the model correctly identify
- **F1-Score** → Balance between precision and recall

---

## 🔍 Key Findings

- 👩 **Gender** was the strongest predictor — women had ~74% survival rate vs men at ~19%
- 🎫 **Passenger class** mattered — 1st class had ~63% survival vs 3rd class at ~24%
- 👶 **Children** had higher survival rates than adults
- 👨‍👩‍👧 **Family size** of 2–4 had better survival than solo travellers

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python 3.8+ | Core programming language |
| Pandas | Data manipulation |
| NumPy | Numerical computations |
| Scikit-learn | Machine learning models |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualizations |

---


---

## 📦 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

---

## 👤 Author

**Your Name**
- GitHub: [@gokul290805](https://github.com/gokul290805)
- LinkedIn: [Gokul Krishnan](https://www.linkedin.com/in/gokul-krishnan-615226260/)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- Dataset sourced from [Kaggle — Titanic Dataset](https://www.kaggle.com/c/titanic)
- Project completed as part of a Virtual Internship Program at CodSoft

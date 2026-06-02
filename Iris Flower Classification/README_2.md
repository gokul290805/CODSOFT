#  Iris Flower Classification

A machine learning project that predicts the species of an Iris flower based on its sepal and petal measurements using a **Random Forest Classifier**.

---

##  Project Structure

```
iris-flower-classification/
├── iris_classifier.py   # Main script
├── IRIS.csv             # Dataset
├── requirements.txt     # Dependencies
└── README.md            # Project documentation
```

---

##  Dataset

- **Source**: UCI Machine Learning Repository — Iris Dataset
- **Samples**: 150
- **Features**: 4 (Sepal Length, Sepal Width, Petal Length, Petal Width)
- **Target Classes**: Iris-setosa, Iris-versicolor, Iris-virginica

---

##  Model Details

| Parameter         | Value              |
|-------------------|--------------------|
| Algorithm         | Random Forest      |
| Number of Trees   | 100                |
| Train/Test Split  | 80% / 20%          |
| Random State      | 42                 |
| Label Encoding    | LabelEncoder       |

---

## ▶ How to Run

**1. Clone the repository**
```bash
git clone https://github.com/gokul290805/iris-flower-classification.git
cd iris-flower-classification
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the script**
```bash
python iris_classifier.py
```

**4. Enter measurements when prompted**
```
Enter Iris Flower Measurements
Sepal Length (cm): 5.1
Sepal Width (cm): 3.5
Petal Length (cm): 1.4
Petal Width (cm): 0.2

----- Prediction Result -----
Predicted Species: Iris-setosa
```

---

##  Technologies Used

- Python 3.x
- Pandas
- Scikit-learn

---

##  Author

**Gokul**
B.Tech CSE — GITAM University, Hyderabad
[GitHub](https://github.com/gokul290805)

---

> 📌 *This project was developed as part of the CodSoft Data Science Internship.*

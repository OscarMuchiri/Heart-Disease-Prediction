# Heart Disease Prediction

A supervised machine-learning project that compares multiple classification algorithms for predicting the **binary presence of heart disease** from clinical attributes.

![Python](https://img.shields.io/badge/Python-Machine%20Learning-3776AB?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Classification-F7931E?logo=scikitlearn&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

> **Educational use only:** this repository demonstrates a machine-learning workflow. It is **not** a diagnostic system and should not be used to make medical decisions.

## Project Objective

The project explores whether common clinical attributes can be used to classify whether heart disease is present.

The original target column, `num`, is converted to:

- `0` — no heart disease
- `1` — heart disease present (`num > 0`)

Three baseline classifiers are compared:

- Logistic Regression
- K-Nearest Neighbors
- Random Forest

---

## Recorded Results

The original notebook run used an 80/20 train–test split.

| Model | Test Accuracy |
|---|---:|
| Logistic Regression | 80.43% |
| K-Nearest Neighbors | 69.57% |
| Random Forest | **82.07%** |

Random Forest produced the strongest recorded performance.

For the positive class (heart disease present), Random Forest achieved:

| Metric | Value |
|---|---:|
| Precision | 0.87 |
| Recall | 0.83 |
| F1-score | 0.85 |

Its recorded confusion matrix was:

```text
[[61, 14],
 [19, 90]]
```

These figures reflect the original coursework run and should be interpreted as baseline experimental results rather than clinical performance claims.

---

## Workflow

The notebook follows this sequence:

1. Load the heart-disease dataset
2. Convert the target to a binary classification problem
3. Remove selected high-missingness fields used in the original workflow
4. Median-impute missing numeric values
5. Encode categorical variables
6. Remove identifier/source fields
7. Split the dataset into training and test sets
8. Train three classification models
9. Compare accuracy, classification reports, and confusion matrices

---

## Repository Structure

```text
Heart-Disease-Prediction/
├── data/
│   └── README.md
├── notebooks/
│   └── heart_disease_prediction.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## Dataset

The notebook expects:

```text
data/heart_disease_uci.csv
```

The dataset used in the coursework combines heart-disease records associated with the Cleveland, Hungary, Switzerland, and VA Long Beach collections.

The underlying **UCI Heart Disease** dataset is available from the UCI Machine Learning Repository:

https://archive.ics.uci.edu/dataset/45/heart+disease

UCI lists the dataset under the **CC BY 4.0** license. See [data/README.md](data/README.md) for setup and attribution notes.

---

## Running the Notebook

Install the required Python packages:

```bash
python -m pip install -r requirements.txt
```

Place the source CSV at:

```text
data/heart_disease_uci.csv
```

Then open:

```text
notebooks/heart_disease_prediction.ipynb
```

and run the cells in order.

---

## Skills Demonstrated

- supervised machine learning
- binary classification
- data cleaning
- missing-value treatment
- categorical encoding
- train–test evaluation
- Logistic Regression
- K-Nearest Neighbors
- Random Forest
- confusion-matrix interpretation
- precision, recall, F1-score, and accuracy
- Python, pandas, and scikit-learn

---

## Limitations and Next Improvements

This is a baseline educational project. A stronger production-oriented experiment would include:

- preprocessing pipelines fitted only on training data
- stratified cross-validation
- feature scaling where appropriate
- hyperparameter tuning
- ROC-AUC and probability calibration
- external validation
- subgroup and fairness analysis
- explainability analysis
- clinical review before any healthcare use

---

## Portfolio Role

This is a **supporting machine-learning project** that demonstrates classical classification and model comparison. It complements the portfolio's larger forecasting and computer-vision projects without replacing them as flagship work.

---

## Author

**Oscar Muchiri**

Computer Scientist | Machine Learning • Software Engineering • Geospatial Systems

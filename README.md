# 🌸 CodeAlpha_IrisClassification

**Iris Flower Classification** — CodeAlpha Data Science Internship, Task 1

Machine learning models that predict the species of an iris flower (**Setosa**, **Versicolor** or **Virginica**) from its four physical measurements.

## 📌 Project Overview

The goal of this task is to train a classification model that identifies iris species from flower measurements and to evaluate its accuracy and performance on test data. Four models are trained and compared, and the best one is selected using cross-validation.

## 📊 Dataset

The Iris dataset is loaded directly from scikit-learn (`load_iris`), so no separate download is needed.

- **150 flowers**, 50 per species (perfectly balanced)
- **4 numeric features:** sepal length, sepal width, petal length, petal width (cm)
- **3 classes:** Setosa, Versicolor, Virginica
- No missing values (1 duplicated row, kept in the data)

## 🔄 Workflow

1. Setup and library imports
2. Load the dataset
3. Exploratory data analysis (shape, missing values, statistics, class balance)
4. Visualisations (pairplot, box plots, correlation heatmap)
5. Feature selection discussion
6. Train/test split (80% / 20%, stratified)
7. Model training and evaluation (accuracy, confusion matrix, classification report)
8. Model comparison with 5-fold stratified cross-validation
9. Feature importance and a prediction for a new flower
10. Conclusion

## 🤖 Models

| Model | Test accuracy | CV mean accuracy (5-fold) |
|---|---|---|
| k-Nearest Neighbours (k=5) | 93.33% | **97.33%** |
| Random Forest | 90.00% | 96.00% |
| Decision Tree (max_depth=3) | 96.67% | 96.00% |
| Logistic Regression | 93.33% | 95.33% |

**Best model:** k-Nearest Neighbours, with 97.33% cross-validated accuracy.

## 🔍 Key Findings

- **Petal length** and **petal width** are the most informative features (about 87% of the Random Forest feature importance).
- **Setosa** is perfectly separated from the other two species. All mistakes are between **Versicolor** and **Virginica**.
- The test set has only 30 flowers, so one wrong prediction changes accuracy by about 3.3 points. Cross-validation gives a more reliable comparison.
- The models perform very closely, and the differences are smaller than the cross-validation standard deviation, so the ranking is a preference rather than a proven winner.

## 🛠️ Tech Stack

Python · pandas · NumPy · scikit-learn · matplotlib · seaborn · Jupyter Notebook

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/riniramadhannaim99/CodeAlpha_IrisClassification.git
cd CodeAlpha_IrisClassification

# 2. Install the requirements
pip install numpy pandas matplotlib seaborn scikit-learn jupyter

# 3. Open the notebook
jupyter notebook IrisClassification.ipynb
```

## 📁 Repository Structure

```
CodeAlpha_IrisClassification/
├── IrisClassification.ipynb   # full analysis and models
└── README.md
```

## 👤 Author

**Rini Ramadhan Naim**
[LinkedIn](https://www.linkedin.com/in/rini-ramadhan-naim-1b0286429)

Completed as part of the **CodeAlpha Data Science Internship** · #CodeAlpha

# Employee Turnover Prediction (Logistic Regression + Regularization)

This project predicts whether an employee will leave the organization (**Employee Turnover**) using employee and workplace-related features.
Three Logistic Regression models are trained and compared:

* Baseline Logistic Regression
* L1 Regularization (Lasso)
* L2 Regularization (Ridge)

---

## Dataset Information

* File: `data/employee_turnover.csv`
* Target column: `Employee_Turnover`

  * `0` = Employee stayed
  * `1` = Employee left

---

## Project Workflow

1. Load and explore dataset
2. Preprocess features (scaling + encoding)
3. Train baseline Logistic Regression
4. Improve model using:

   * L1 Regularization (Lasso)
   * L2 Regularization (Ridge)
5. Hyperparameter tuning using **GridSearchCV**
6. Evaluate models using:

   * Accuracy
   * ROC-AUC
   * Confusion Matrix
   * ROC Curve
   * Classification Report (Precision, Recall, F1-score)

---

## Tech Stack

* Python
* NumPy, Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## Repo Structure

```
employee-turnover-prediction/
│── notebooks/
│   └── employee_turnover_project_FINAL.ipynb
│── data/
│   └── employee_turnover.csv
│── assets/
│   ├── confusion_matrix_baseline.png
│   ├── confusion_matrix_l1.png
│   ├── confusion_matrix_l2.png
│   ├── roc_curve_baseline.png
│   ├── roc_curve_l1.png
│   └── roc_curve_l2.png
│── requirements.txt
│── .gitignore
└── README.md
```

---

## How to Run the Project

### 1) Clone the repository

```bash
git clone https://github.com/Nandd11/Employee-turnover-prediction.git
cd Employee-turnover-prediction
```

### 2) Install dependencies

```bash
pip install -r requirements.txt
```

### 3) Run the notebook

```bash
jupyter notebook
```

Open:

```
notebooks/employee_turnover_project_FINAL.ipynb
```

---

## Model Evaluation & Results

### Metrics Used

* Accuracy
* ROC-AUC Score
* Confusion Matrix
* ROC Curve
* Classification Report

### Results Comparison Table

| Model                              | Accuracy | ROC-AUC |
| ---------------------------------- | -------- | ------- |
| Baseline Logistic Regression       | 0.8815   | 0.9583  |
| L1 Regularized Logistic Regression | 0.8815   | 0.9605  |
| L2 Regularized Logistic Regression | 0.8852   | 0.9585  |

✅ **Best Accuracy:** L2 Regularization (0.8852)
✅ **Best ROC-AUC:** L1 Regularization (0.9605)

---

## Plots

### L2 Regularized Logistic Regression

#### Confusion Matrix (L2)

![Confusion Matrix - L2](assets/confusion_matrix_l2.png)

#### ROC Curve (L2)

![ROC Curve - L2](assets/roc_curve_l2.png)

---

### Additional Plots (Baseline & L1)

#### Confusion Matrix (Baseline)

![Confusion Matrix - Baseline](assets/confusion_matrix_baseline.png)

#### Confusion Matrix (L1)

![Confusion Matrix - L1](assets/confusion_matrix_l1.png)

#### ROC Curve (Baseline)

![ROC Curve - Baseline](assets/roc_curve_baseline.png)

#### ROC Curve (L1)

![ROC Curve - L1](assets/roc_curve_l1.png)

---

## Final Conclusion

* The model performance was compared using Accuracy and ROC-AUC.
* **L2 Regularization** achieved the highest **Accuracy**, so it is best for overall correct predictions.
* **L1 Regularization** achieved the highest **ROC-AUC**, meaning it is better at distinguishing between employees who leave vs stay.
* Overall, both regularized models perform better and more stable than the baseline model.

✅ **Final Recommendation:**

* Use **L2 Regularization** if your priority is Accuracy (best overall prediction).
* Use **L1 Regularization** if your priority is ROC-AUC (best classification separation).

---

## Author

**Nand**

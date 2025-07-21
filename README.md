# ML-random-forest-algorithm-
# Student Adaptability Level Prediction (Online Education)

This project focuses on predicting the **adaptability level** of students in an online education environment using machine learning techniques. The objective is to classify students into one of three adaptability levels — **Low**, **Moderate**, or **High** — based on demographic, environmental, and technological factors.

---

## Dataset

- **File:** `students_adaptability_level_online_education.csv`
- **Records:** 1205 rows
- **Features:** 14 columns

### Input Features:
- Gender
- Age
- Education Level
- Institution Type
- IT Student
- Location
- Load-shedding
- Financial Condition
- Internet Type
- Network Type
- Class Duration
- Self LMS
- Device

### Target Variable:
- `Adaptivity Level`: Low, Moderate, High

---

## Technologies Used

- Python
- pandas, numpy, matplotlib, seaborn (Data analysis & visualization)
- scikit-learn (Machine learning & preprocessing)
- joblib (Model serialization)

---

## Preprocessing Steps

1. **Encoding**:
   - Ordinal Encoding: `Age`, `Education Level`, `Class Duration`
   - One-Hot Encoding: All other categorical features
2. **Scaling**:
   - StandardScaler applied to numerical data
3. **Data Split**:
   - 80% Training, 20% Testing

---

## Machine Learning Models

Several classification algorithms were tested:

| Model                  | Accuracy |
|------------------------|----------|
| Logistic Regression    | 72.61%   |
| K-Nearest Neighbors    | 76.76%   |
| Support Vector Machine | 82.16%   |
| Decision Tree          | 86.72%   |
| Random Forest          | 89.21%   |
| Gradient Boosting      | 83.40%   |

---

## Hyperparameter Tuning

A `GridSearchCV` was performed on the **Random Forest** model to find the best hyperparameters.

**Best Parameters:**
```python
{
  'bootstrap': False,
  'max_depth': None,
  'min_samples_leaf': 1,
  'min_samples_split': 2,
  'n_estimators': 300
}

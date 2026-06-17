# 🎓 Student Performance & Dropout Prediction


![Python](https://img.shields.io/badge/Python-3.x-blue) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
A university wants to identify at-risk students early. This project builds multi-class classifiers to predict student performance level (High/Medium/Low) from LMS engagement data, and extracts interpretable rules for an early-warning system.

## Dataset
- Students Academic Performance Dataset (xAPI) — [Kaggle](https://www.kaggle.com/datasets/aljarah/xAPI-Edu-Data)

## Tech Stack
Python · Pandas · NumPy · Seaborn · Scikit-learn (Logistic Regression, Decision Tree) · SciPy (Inferential Statistics)

## Approach
1. Explored performance by gender, topic, resource visits and discussion participation
2. Ran t-tests comparing Low vs High performers on key engagement metrics
3. Label-encoded all categorical columns including the target performance class
4. Trained a multi-class Logistic Regression for probability-based predictions
5. Trained a depth-limited Decision Tree (max_depth=4) and extracted its rules as a usable early-warning policy
6. Evaluated with weighted F1 score and translated findings into intervention recommendations

## Key Results & Insights
- Resource visits and discussion participation are the strongest predictors of performance level (both p < 0.001)
- Students in the Low performance group visit course resources 60–70% less often than High performers
- The Decision Tree achieves a weighted F1 of ~0.70–0.75 — solid for a 3-class problem
- Raised-hands count is surprisingly predictive — active participation correlates with performance
- Top decision rule: students with resource visits ≤ 40 AND discussion posts ≤ 5 are almost always Low performers — a directly actionable early-warning signal

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook student_performance_prediction.ipynb
```

## Project Structure
```
student-performance-dropout-prediction/
├── notebooks/student_performance_prediction.ipynb
├── images/  (eda.png, feature_importance.png)
├── requirements.txt
└── README.md
```

## Author
Akshat Kesharwani — [LinkedIn](https://linkedin.com/in/akshat-kesharwani-b0452b346) · [Portfolio](https://akshatkesharwani-info.github.io)

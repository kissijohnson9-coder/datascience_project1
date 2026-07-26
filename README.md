# Titanic Data Science Project

Exploratory data analysis, statistical analysis and a machine learning model built on the
Titanic dataset, for the BCS 404 project at Accra Technical University.

**Name:** Kissi Kwame Johnson
**ID:** 01250608B
**Course:** BCS 404 - Introduction to Data Science with Python
**Lecturer:** Dr. Joseph Dadzie
**Academic Year:** 2025/2026, Second Semester

## Overview

This project works through the full data science pipeline in Python: acquiring the Titanic
dataset, cleaning it, visualising it, running statistical analysis, and building a Logistic
Regression model to predict passenger survival.

## Repository Structure

```
├── dataset/
│   └── titanic.csv              # Titanic dataset (891 passengers), from Kaggle
├── notebooks/
│   └── main_analysis.ipynb      # Full analysis notebook, run top to bottom
├── report/
│   ├── analysis_report.docx     # Written report (cover page, methodology, results, references)
│   └── analysis_report.pdf      # PDF version of the report
└── README.md
```

## Dataset

Titanic dataset from Kaggle: https://www.kaggle.com/competitions/titanic/data

## Requirements

- Python 3
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Install with:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Run

1. Clone this repository.
2. Install the requirements listed above.
3. Open `notebooks/main_analysis.ipynb` in Jupyter Notebook or Jupyter Lab.
4. Run all cells from top to bottom (Cell > Run All).

## Summary of Findings

- Missing values handled: `Age` filled with the mean, `Embarked` filled with the mode, `Cabin`
  converted into a `HasCabin` flag rather than dropped outright.
- Engineered features: `FamilySize` and `IsAlone`, derived from `SibSp` and `Parch`.
- Six visualisations produced: age histogram with density curve, passenger class bar chart,
  age-by-class boxplot, age vs fare scatter plot (coloured by survival), correlation heatmap, and
  a pairplot coloured by survival outcome.
- Strongest correlations: Fare and HasCabin showed the strongest positive correlation among all
  numeric variables; Pclass and HasCabin showed the strongest negative correlation.
- A Logistic Regression model was trained to predict survival using the engineered features,
  achieving roughly 76% accuracy on the test set.

Full methodology, results and discussion are available in `report/analysis_report.docx` (or the
PDF version).

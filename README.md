# Titanic Survival Analysis

This project analyzes the Titanic passenger dataset to understand the factors associated with passenger survival. It includes data cleaning, exploratory data analysis, correlation analysis, and a simple machine learning model using logistic regression.

## Project Objective

The main objective is to answer two questions:

1. Which passenger characteristics were most strongly associated with survival?
2. Can a classification model predict whether a passenger survived using basic passenger information?

## Dataset

The project uses the Titanic dataset, which contains passenger records with features such as:

- Passenger class
- Sex
- Age
- Number of siblings or spouses aboard
- Number of parents or children aboard
- Fare
- Port of embarkation
- Survival status

The main dataset file is `train.csv`.

## Project Files

- `main.ipynb`: Jupyter Notebook containing the full data analysis and machine learning workflow.
- `train.csv`: Titanic training dataset used for analysis.
- `gender_submission.csv`: Sample submission file from the Titanic dataset package.
- `Titanic_Survival_Analysis_Report.docx`: Final written report generated from the analysis.
- `build_titanic_report.py`: Python script used to generate the Word report.
- `CPS_Data_Science Project.pdf`: Project instruction/reference document.
- `README.md`: Project overview and usage instructions.

## Methodology

The analysis follows these main steps:

1. Load the Titanic dataset using pandas.
2. Inspect dataset dimensions, column names, and data types.
3. Detect and handle missing values.
4. Remove the `Cabin` column because it contains many missing values.
5. Fill missing `Age` values using the median age.
6. Fill missing `Embarked` values using the most common embarkation port.
7. Explore passenger distributions using visualizations.
8. Analyze correlations among numerical variables.
9. Compare survival rates by passenger class and sex.
10. Train and evaluate a logistic regression classification model.

## Key Findings

- Only about 38.4% of passengers in the dataset survived.
- Female passengers had a much higher survival rate than male passengers.
- First-class passengers had a higher survival rate than second- and third-class passengers.
- Passenger class and fare were meaningfully related to survival.
- The logistic regression model achieved about 81% accuracy on the test set.

## Machine Learning Model

The project uses logistic regression to predict survival. The selected model features are:

- `Pclass`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Fare`

The target variable is `Survived`.

## How to Run the Notebook

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Then open and run:

```bash
jupyter notebook main.ipynb
```

## How to Generate the Report

The Word report can be regenerated with:

```bash
python3 build_titanic_report.py
```

This creates:

```text
Titanic_Survival_Analysis_Report.docx
```

## Conclusion

This project demonstrates a complete introductory data science workflow: data acquisition, cleaning, visualization, statistical interpretation, and machine learning classification. The results show that sex, passenger class, and fare were important indicators of survival in the Titanic dataset.

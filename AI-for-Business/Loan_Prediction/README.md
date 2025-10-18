# Loan-default

# Loan Default Prediction Project

## Overview

This project aims to develop a predictive model to determine the likelihood of loan default among applicants. By analyzing various features related to the applicants' financial situations and demographics, the model helps in making informed lending decisions.

## Table of Contents

- [Project Description](#project-description)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
- [Modeling](#modeling)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Project Description

The Loan Default Prediction project leverages machine learning algorithms to predict whether a loan applicant will default on their loan. The project involves:

- Data analysis and visualization
- Data cleaning and preprocessing
- Feature selection and engineering
- Model training and evaluation

## Dataset

The dataset used in this project is sourced from [insert source, e.g., Kaggle, UCI Machine Learning Repository]. It contains the following key features:

- `TARGET`: Target variable indicating whether the loan defaulted (1) or not (0)
- `NAME_CONTRACT_TYPE`: Type of loan (Cash or Revolving)
- `CODE_GENDER`: Gender of the applicant
- `FLAG_OWN_CAR`: Indicates if the applicant owns a car (Y/N)
- `FLAG_OWN_REALTY`: Indicates if the applicant owns real estate (Y/N)
- `CNT_CHILDREN`: Number of children
- `AMT_INCOME_TOTAL`: Total annual income
- `AMT_CREDIT`: Amount of credit requested
- `AMT_ANNUITY`: Amount of annuity
- `DAYS_BIRTH`: Applicant's age in days (negative values)
- `YEARS_EMPLOYED`: Years of employment

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Data Cleaning and Preprocessing

1. **Outlier Handling**: Outliers in the `CNT_CHILDREN` column were removed based on the 99th percentile.
2. **Null Values**: Missing values were addressed by:
   - Imputing `FLAG_OWN_CAR` with proportions of 'Y' and 'N'.
   - Filling missing values in `AMT_INCOME_TOTAL` with the mean.
   - Removing rows with missing target values.
3. **Inconsistencies**: Fixed inconsistencies in the `FLAG_OWN_REALTY` column.
4. **Feature Engineering**: Converted `DAYS_BIRTH` to years and replaced negative values with positive equivalents.

## Modeling

The project employs  Logistic Regression to predict loan defaults. Each model's performance is evaluated using metrics like accuracy, precision, recall, and F1 score.

## Results

The model achieved an accuracy of 0.98.

## License
This project is licensed under the Apache License.

# Clean and Transform Diabetes Data

A focused data preprocessing project that takes a raw diabetes dataset with 
missing values and transforms it into a clean, analysis-ready file. The project 
applies targeted imputation strategies and engineers two new features to enrich 
the dataset for downstream machine learning or analysis tasks.

## Overview

Raw medical datasets rarely arrive clean. This project demonstrates proper data 
wrangling practices on a real-world diabetes dataset — handling missing values 
with statistically appropriate strategies, stripping hidden characters from column 
names, and creating meaningful derived features that add analytical value without 
introducing bias.

## What This Project Does

- Loads a diabetes dataset with missing values across multiple clinical columns
- Detects and removes hidden characters and whitespace from column names
- Fills missing Glucose and BMI values using column means
- Fills missing Blood Pressure, Skin Thickness, and Insulin values using medians
- Engineers a BMI Category feature with four classifications:
  Underweight, Normal, Overweight, and Obese
- Engineers an Age Group feature segmenting patients into Young, 
  Middle-aged, and Senior categories
- Exports the fully cleaned and enriched dataset as a new CSV file

## Why Mean vs Median

Mean imputation was used for normally distributed columns like Glucose and BMI, 
while median imputation was applied to skewed columns like Insulin and Skin 
Thickness — a deliberate choice to avoid pulling imputed values toward outliers.

## Output

| File | Description |
|------|-------------|
| Cleaned_Diabetes_Data.csv | Fully cleaned dataset with engineered features |

## Tech Stack

- Python (Pandas, NumPy)
- Google Colab

## Dataset

The project uses the Pima Indians Diabetes dataset containing clinical measurements 
such as glucose level, blood pressure, BMI, insulin, and age for 768 female patients.

## Author

M. Talal Bin Waheed

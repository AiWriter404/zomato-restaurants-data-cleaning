# Zomato Restaurants — Data Cleaning Project

## 📌 Overview
This project focuses on cleaning and preprocessing the **Zomato Bangalore Restaurants** dataset from Kaggle. The raw dataset contains missing values, duplicate entries, inconsistent text formatting, and mixed data types — making it a great real-world case study for data cleaning practice.

The goal is to transform the messy raw dataset into a clean, analysis-ready dataset using Python and Pandas.

## 📊 Dataset
- **Source:** [Zomato Bangalore Restaurants — Kaggle](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants)
- **Rows:** ~51,000
- **Columns:** Restaurant name, location, cuisines, cost, ratings, votes, online order availability, table booking, and more

## 🎯 Objectives
- Handle missing values appropriately
- Remove duplicate records
- Fix inconsistent data types (e.g., cost stored as text)
- Standardize categorical/text columns (cuisines, restaurant types, locations)
- Detect and handle outliers
- Produce a clean, well-documented final dataset

## 🛠️ Tools & Technologies
- Python
- Pandas
- NumPy
- Jupyter / Kaggle Notebook
- Matplotlib / Seaborn (for outlier & missing value visualization)

## 🧹 Data Cleaning Steps
1. Load data and explore structure (`.info()`, `.describe()`, `.isnull().sum()`)
2. Handle missing values (drop / impute)
3. Remove duplicate rows
4. Fix data types (e.g., convert cost column to numeric)
5. Clean and standardize text/categorical columns
6. Detect and treat outliers
7. Save the final cleaned dataset
8. Document before/after comparison

## 📁 Project Structure
```
zomato-restaurants-data-cleaning/
│
├── data/
│   ├── raw/                # original dataset (not uploaded if large)
│   └── cleaned/            # cleaned dataset output
│
├── notebook/
│   └── zomato_data_cleaning.ipynb
│
├── README.md
└── requirements.txt
```

## 🚀 How to Run
1. Clone this repository
2. Download the dataset from the Kaggle link above and place it in `data/raw/`
3. Open the notebook in Jupyter or Kaggle
4. Run all cells step by step

## 📈 Results
*(To be updated after project completion — summary of cleaning steps performed and final dataset shape)*

## 👤 Author
*(Add your name / GitHub profile / LinkedIn here)*

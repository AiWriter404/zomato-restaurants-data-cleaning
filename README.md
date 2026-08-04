# Zomato Restaurants — Data Cleaning Project

🔗 **GitHub Repository:** [zomato-restaurants-data-cleaning](https://github.com/AiWriter404/zomato-restaurants-data-cleaning/tree/main)
🔗 **Kaggle Notebook:** [zomato-restaurants-data-cleaning](https://www.kaggle.com/code/muhammadumer7804/zomato-restaurants-data-cleaning)

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

**Original dataset:** 51,717 rows × 17 columns
**Cleaned dataset:** 51,466 rows × 16 columns

### Cleaning summary:
- Dropped the `dish_liked` column (~54% missing values)
- Handled missing values in `location`, `rest_type`, `cuisines`, `rate`, `phone`, and `approx_cost`
- Checked for duplicate rows (none found)
- Converted `rate` column from text (e.g. `"4.1/5"`) to numeric float
- Converted `approx_cost` column from text with commas (e.g. `"1,200"`) to numeric integer
- Cleaned extra whitespace in text columns (`name`, `location`, `rest_type`, `cuisines`)
- Standardized `phone` column formatting (removed line breaks)
- Renamed unclear column names (`approx_cost(for two people)` → `approx_cost`, etc.)
- Reviewed outliers in `votes`, `approx_cost`, and `rate` — kept as they represent genuine variation (popular vs less popular restaurants, budget vs fine dining) rather than data errors

### Final dataset stats:
| Column | Min | Max | Mean |
|---|---|---|---|
| rate | 1.8 | 4.9 | 3.70 |
| votes | 0 | 16,832 | 284.76 |
| approx_cost | 40 | 6,000 | 554.46 |

The cleaned dataset (`zomato_cleaned.csv`) is ready for further analysis and visualization.

## 📊 Exploratory Data Analysis (EDA)

After cleaning, an in-depth EDA was performed to uncover patterns in restaurant ratings, pricing, cuisines, and location trends.

### Key Insights

**Ratings & Cost Distribution**
- Most restaurants are rated between 3.5–4.0, showing overall above-average quality
- Majority of restaurants fall in the ₹300–600 price range for two people, indicating a budget-friendly market

**Online Order & Table Booking**
- ~59% of restaurants offer online ordering; online order availability has little effect on rating
- Only ~12% of restaurants offer table booking, but these restaurants have a noticeably higher median rating (~4.1 vs ~3.7) and nearly 3x higher average cost (₹1,271 vs ₹451) — table booking is a strong indicator of a premium dining experience

**Restaurant Types & Cuisines**
- "Quick Bites" and "Casual Dining" are the most common restaurant types, reflecting a fast/casual food culture
- North Indian and Chinese are the most widely offered cuisines, followed by South Indian and Biryani as strong standalone categories

**Location Trends**
- BTM has the highest number of restaurants but the lowest average cost, making it a high-density, budget-friendly food hub
- Koramangala 5th Block and Indiranagar have fewer restaurants but the highest average cost, representing premium dining areas

**Correlation Analysis**
- Rate, votes, and cost show only moderate positive correlations (0.37–0.43) — no single factor strongly predicts another
- Restaurants with higher vote counts consistently converge toward higher ratings (4.0–4.9), while low-vote restaurants show much more scattered/volatile ratings

## 👤 Author
GitHub: @AiWriter404
Kaggle: @muhammadumer7804

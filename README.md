# FIFA 21 Player Dataset Cleaning Project

## Overview
This project focuses on cleaning the **FIFA 15–21 Complete Player Dataset** from Kaggle.  
The dataset contains detailed player attributes such as personal information, ratings, and financial data across multiple FIFA game editions.

The primary goal is **data cleaning** — ensuring consistency, detecting missing values, removing duplicates, and preparing a clean dataset for future analysis.  
One highlight of this project is **repeating the same cleaning process across multiple sheets (years) with the same structure**, which makes the cleaning process efficient and scalable.

---

## Dataset
- **Source:** FIFA 21 Complete Player Dataset (Kaggle)
- **Format:** Excel file with multiple sheets (one for each FIFA edition, 2015–2021)
- **Columns:** 106 (player stats, financials, club details, etc.)

---

## Data Cleaning Steps
The notebook `FIFA_clean_lite.ipynb` performs the following:
- Load raw data from Excel
- Remove whitespace from text columns
- Convert date columns (`dob`, `joined`, `contract_valid_until`)
- Convert monetary columns (`value_eur`, `wage_eur`, `release_clause_eur`) to numeric
- Split `work_rate` into `attack_work_rate` and `defense_work_rate`
- Convert player traits into list format
- Remove duplicate players based on `sofifa_id`
- Perform anomaly checks (age, height, weight, ratings, stats, money)
- Save cleaned data into:
  - A multi-sheet cleaned Excel file
  - A merged dataset (2015–2021) for easy analysis

---

## Project Structure
FIFA21-Cleaning-Project
- notebooks/ FIFA_clean_lite.ipynb # Jupyter notebook with cleaning code
- README.md # Project documentation
- requirements.txt # Python dependencies

*(Note: The data file  be included due to size constraints.)*

---

## Installation
Clone this repository and install the required packages:
```
git clone https://github.com/Chuqin5114/FIFA21-Cleaning-Project.git
cd FIFA21-Cleaning-Project
pip install -r requirements.txt
  ```

## Usage
Open the notebook: FIFA_clean_lite.ipynb

Run all cells to:
1. Download the dataset (via kagglehub).
2. Clean and merge data.
3. Save final cleaned Excel files.

## Requirements
See `requirements.txt.`

(Currently includes: `pandas`, `openpyxl`, `kagglehub`).

## Future Work
- Exploratory Data Analysis (EDA).
- More detailed player statistics analysis.
- Visualisation Dashboard.




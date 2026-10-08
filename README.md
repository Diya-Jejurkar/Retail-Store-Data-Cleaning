# Retail Store Data Cleaning

## Project Overview

This project focuses on cleaning a retail store sales dataset. The dataset contains information about transactions, customers, products, prices, quantities, payment methods, locations, dates, and discounts.

The main objective is to identify and clean missing values, duplicate records, incorrect data types, and inconsistent values.

## Dataset

Dataset: Retail Store Sales: Dirty for Data Cleaning

Source: Kaggle

## Dataset Information

* Number of records: 12,575
* Number of columns: 11
* Duplicate records found: 0

## Data Quality Issues Found

The dataset contained missing values in:

* Item
* Price Per Unit
* Quantity
* Total Spent
* Discount Applied

Some columns also required data type conversion.

## Data Cleaning Performed

The following cleaning operations were performed using Python and Pandas:

1. Missing Item values were replaced with `Unknown`.
2. Missing Price Per Unit values were replaced using the median price.
3. Missing Quantity values were replaced using the median quantity.
4. Missing Total Spent values were calculated using Price Per Unit × Quantity.
5. Missing Discount Applied values were replaced with `False`.
6. Duplicate records were removed.
7. Transaction Date was converted to datetime format.
8. Quantity was converted to integer format.
9. Discount Applied was converted to Boolean format.
10. The cleaned dataset was saved as a new CSV file.

## Tools Used

* Python
* Pandas
* NumPy
* Jupyter Notebook
* VS Code

## Project Files

```text
Retail-Store-Data-Cleaning/
│
├── data/
│   ├── retail_store_sales.csv
│   └── retail_store_sales_cleaned.csv
│
├── Retail_Store_Data_Cleaning.ipynb
├── data_cleaning.py
├── README.md
└── requirements.txt
```

## Result

After cleaning, the dataset was checked again for missing values, duplicate records, and data types. The cleaned dataset was exported as:

`retail_store_sales_cleaned.csv`

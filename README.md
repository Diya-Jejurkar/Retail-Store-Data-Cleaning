# Retail Store Data Cleaning and Exploratory Data Analysis

## Project Overview

This project focuses on cleaning and analyzing a retail store sales dataset.

The project is divided into two main tasks:

- **Task 1:** Data Cleaning
- **Task 2:** Exploratory Data Analysis (EDA)

Python and Pandas were used for data cleaning and analysis, while Matplotlib was used to create visualizations.

---

## Dataset

The dataset used in this project is **Retail Store Sales: Dirty for Data Cleaning**, a public dataset available on Kaggle.

The dataset contains retail transaction information such as:

- Transaction ID
- Customer ID
- Category
- Item
- Price Per Unit
- Quantity
- Total Spent
- Payment Method
- Location
- Transaction Date
- Discount Applied

The original dataset contains **12,575 records and 11 columns**.

---

# Task 1: Data Cleaning

The raw dataset was examined to identify common data quality problems.

### Data Quality Checks

The following checks were performed:

- Missing values
- Duplicate records
- Incorrect data types
- Unique values and possible inconsistencies

### Cleaning Performed

#### 1. Missing Item Values

Missing values in the `Item` column were replaced with:

```text
Unknown
```

#### 2. Missing Price Per Unit

Missing values were replaced using the **median price** of the column.

#### 3. Missing Quantity

Missing quantity values were replaced using the **median quantity**.

#### 4. Missing Total Spent

Missing `Total Spent` values were calculated using:

```text
Price Per Unit × Quantity
```

#### 5. Missing Discount Applied

Missing values in `Discount Applied` were replaced with:

```text
False
```

#### 6. Duplicate Records

Duplicate records were checked and removed.

#### 7. Data Type Correction

The following data types were corrected:

- `Transaction Date` → DateTime
- `Quantity` → Integer
- `Discount Applied` → Boolean

### Cleaned Dataset

The cleaned dataset was saved as:

```text
data/retail_store_sales_cleaned.csv
```

---

# Task 2: Exploratory Data Analysis

After cleaning the dataset, exploratory data analysis was performed to understand sales patterns, trends, and relationships.

The following analyses were performed:

- Statistical summary
- Sales by category
- Payment method analysis
- Sales by location
- Monthly sales trend
- Quantity analysis
- Quantity vs Total Spent correlation

## Key Statistics

The dataset was analyzed using descriptive statistics to understand numerical columns such as:

- Price Per Unit
- Quantity
- Total Spent

---

# Key Insights

### 1. Sales by Category

The **Butchers** category generated the highest total sales.

- Butchers: **218,153**
- Milk Products: **189,892**

This shows that Butchers was the strongest-performing category in terms of total sales.

### 2. Payment Method

**Cash** was the most commonly used payment method.

- Cash: **4,310 transactions**
- Digital Wallet: **4,144 transactions**
- Credit Card: **4,121 transactions**

### 3. Sales by Location

Online sales were slightly higher than In-store sales.

- Online: **831,922**
- In-store: **805,445**

This indicates that the Online channel generated more total sales in the analyzed dataset.

### 4. Monthly Sales Trend

The highest monthly sales were recorded in **January 2022**.

- January 2022: **56,271.5**

This was the highest total monthly sales value identified during the analysis.

### 5. Quantity and Total Spent

The correlation between `Quantity` and `Total Spent` was:

```text
0.7039376244694937
```

This indicates a **positive relationship** between quantity purchased and total spending. In general, transactions with higher quantities tend to have higher total spending.

---

# Visualizations

The EDA notebook includes visualizations for:

- Total Sales by Category
- Transactions by Payment Method
- Total Sales by Location
- Monthly Sales Trend
- Quantity vs Total Spent

These charts help understand the sales distribution, customer payment preferences, location performance, and relationships between variables.

---

# Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

---

# Project Structure

```text
Retail-Store-Data-Cleaning/
│
├── data/
│   ├── retail_store_sales.csv
│   └── retail_store_sales_cleaned.csv
│
├── data_cleaning.ipynb
├── eda_analysis.ipynb
├── README.md
└── requirements.txt
```

---

# How to Run the Project

### Step 1: Clone the repository

```bash
git clone https://github.com/Diya-Jejurkar/Retail-Store-Data-Cleaning.git
```

### Step 2: Open the project folder

```bash
cd Retail-Store-Data-Cleaning
```

### Step 3: Install the required libraries

```bash
pip install -r requirements.txt
```

### Step 4: Open Jupyter Notebook

```bash
jupyter notebook
```

### Step 5: Run the notebooks

Run the notebooks in the following order:

1. `data_cleaning.ipynb`
2. `eda_analysis.ipynb`

---

# Conclusion

This project demonstrates the complete workflow of working with a real-world retail dataset, starting from raw data cleaning and continuing through exploratory data analysis.

The analysis helped identify important sales patterns, including the best-performing category, most-used payment method, stronger sales channel, highest-sales month, and the relationship between quantity and total spending.

The project provides practical experience in **data cleaning, exploratory data analysis, statistical analysis, data visualization, and Python-based data analysis**.
# Walmart Data Analysis: End-to-End SQL + Python Project

## 🚀 Project Overview

This project is an end-to-end data analysis workflow using Walmart sales data. It includes data acquisition, cleaning, transformation, and advanced SQL analysis using **PostgreSQL** and **Python**. This project is ideal for data analysts aiming to enhance their skills in PostgreSQL querying, data manipulation with Python, and analytical problem-solving.

---

## 🧱 Project Workflow

### 1. Environment Setup

* **Tools**: Visual Studio Code, Python, PostgreSQL
* **Task**: Create a clean and structured workspace with organized folders for scripts, notebooks, and data files.

### 2. Kaggle API Integration

* **Steps**:

  * Download your API token from [Kaggle](https://www.kaggle.com/account).
  * Save `kaggle.json` in your system’s `.kaggle` folder.
  * Use the command:

    kaggle datasets download -d <dataset-path>


### 3. Download Walmart Sales Data

* **Source**: [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
* **Storage**: Save the dataset inside the `data/` folder.

### 4. Install Required Libraries & Load Data

Install Python libraries:

pip install pandas numpy sqlalchemy psycopg2

Load the dataset into a Pandas DataFrame for further processing.

### 5. Exploratory Data Analysis (EDA)

Use `.info()`, `.describe()`, and `.head()` to understand the structure, data types, and potential issues in the dataset.

### 6. Data Cleaning

* **Remove Duplicates**: Eliminate duplicate entries.
* **Handle Missing Values**: Fill or drop based on context.
* **Fix Data Types**: Convert to appropriate formats (`datetime`, `float`, etc.).
* **Format Currency**: Clean up currency fields using `.replace()` and other string operations.

### 7. Feature Engineering

* Add a new column:

  python code -
  df["total_amount"] = df["unit_price"] * df["quantity"]
  
* This makes revenue analysis and SQL aggregations easier.

### 8. Load Data into PostgreSQL

* Use `SQLAlchemy` and `psycopg2` to connect to PostgreSQL.
* Create a new table and insert the cleaned data.
* Run verification queries to confirm data integrity.

### 9. SQL Analysis

Use PostgreSQL to write and execute SQL queries that answer business questions such as:

* Revenue trends by branch and product category.
* Top-performing cities and payment methods.
* Customer behavior patterns and peak shopping times.
* Profit margins by location and category.

### 10. Documentation & Publishing

* Document the process using Markdown and/or Jupyter Notebooks.
* Publish to GitHub with the following:

  * `README.md`
  * SQL query scripts
  * Notebooks and/or `.py` scripts
  * Instructions to obtain and set up the data

---

## ✅ Requirements

* **Python**: 3.8+
* **Database**: PostgreSQL
* **Libraries**:

  * `pandas`, `numpy`, `sqlalchemy`, `psycopg2`
* **Kaggle API key** (for data download)

---

## 📁 Project Structure

```plaintext
|-- data/                     # Raw and cleaned data files
|-- sql_queries/              # PostgreSQL scripts
|-- notebooks/                # Jupyter/Python analysis notebooks
|-- main.py                   # Script for loading and processing data
|-- requirements.txt          # Python dependencies
|-- README.md                 # Project documentation
```

---

## 📊 Key Insights

* **Top Branches**: Identify branches with highest revenue and best-selling categories.
* **Customer Preferences**: Most used payment methods and peak buying times.
* **Profitability**: Evaluate which categories and cities are most profitable.

---

## 🔮 Future Enhancements

* Add interactive dashboards using Power BI or Tableau.
* Automate the pipeline for live data ingestion.
* Integrate external data sources (e.g., customer feedback or inventory data).



## 🙏 Acknowledgments

* **Dataset**: Walmart Sales Dataset from Kaggle
* **Inspired by**: Real-world business analytics use cases in retail

---

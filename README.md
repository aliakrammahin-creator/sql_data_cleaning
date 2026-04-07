# 📊 Layoffs Data Cleaning Project (MySQL)

## 📌 Overview
In this project, I worked on cleaning a real-world layoffs dataset using MySQL.  
The goal was to take messy, unstructured data and turn it into something clean and ready for analysis.

While working on this, I got hands-on experience with common data cleaning problems like duplicates, missing values, and inconsistent formatting.

---

## 🎯 What I Did
- Removed duplicate records  
- Cleaned and standardized messy text data  
- Converted date formats into proper SQL date type  
- Handled null and blank values  
- Removed unnecessary or incomplete rows  

---

## 🛠️ Tools Used
- MySQL  
- SQL (Window Functions, Joins, Data Cleaning techniques)

---

## ⚙️ Cleaning Process

### 🔹 Removing Duplicates
I created staging tables to avoid modifying the original dataset.  
Then I used `ROW_NUMBER()` with `PARTITION BY` to identify duplicate rows and removed them.

---

### 🔹 Standardizing Data
- Trimmed extra spaces in company names  
- Fixed inconsistent values like:
  - “Crypto%” → “Crypto”  
  - “United States%” → “United States”  
- Converted the `date` column from text format into a proper `DATE` type  

---

### 🔹 Handling Missing Values
- Replaced blank values with `NULL`  
- Used a self join to fill missing `industry` values based on other rows from the same company  

---

### 🔹 Removing Unnecessary Data
- Deleted rows where both `total_laid_off` and `percentage_laid_off` were NULL  
- Dropped the helper column (`row_num`) after cleaning  

---

## 📊 Final Result
At the end of this process, the dataset became much cleaner and more consistent, making it ready for:
- Data analysis  
- Visualization (Power BI / Tableau)  
- Further SQL exploration  

---

## 📚 What I Learned
- How to remove duplicates using window functions  
- Handling missing data using self joins  
- The importance of data standardization before analysis  
- Writing cleaner and more structured SQL queries  
- Real-world data is almost always messy  

---

## 🚀 How to Use
1. Import the raw layoffs dataset into MySQL  
2. Run the SQL script:  
   data_cleaning_layoffs_mysql.sql  
3. Use the cleaned table (layoff_staging2) for analysis  

---

## 💡 Future Plans
- Perform exploratory data analysis (EDA) on this dataset  
- Build a dashboard using Power BI or Tableau  
- Work on more real-world datasets  

---

## 👤 About Me
I’m currently learning and building projects to become a Data Analyst.  
This project is part of my journey to improve my SQL and data cleaning skills.

# Employee Data Cleaning & Quality Analysis

## 📌 Project Overview

This project focuses on cleaning and preprocessing a messy company employee dataset using **Python and Pandas**.

Real-world datasets often contain missing values, duplicate records, inconsistent categorical entries, incorrect data types, invalid numerical values, and formatting issues. This project identifies these problems, applies appropriate data-cleaning techniques, and produces a reliable, structured, and analysis-ready employee dataset.

The project also compares the condition of the dataset **before and after cleaning** and exports the final cleaned dataset as a CSV file.

---

## 🎯 Objectives

The main objectives of this project are:

* Load and inspect a messy employee dataset.
* Understand the structure and characteristics of the dataset.
* Identify and quantify missing values.
* Detect duplicate employee records.
* Identify inconsistent categorical values.
* Detect incorrect data types.
* Identify invalid numerical values.
* Apply appropriate data-cleaning techniques.
* Validate the dataset after cleaning.
* Compare the dataset before and after cleaning.
* Export the cleaned dataset for further analysis.

---

## 📊 Dataset Features

The dataset contains the following employee-related attributes:

| Column              | Description                                                       |
| ------------------- | ----------------------------------------------------------------- |
| `Employee_ID`       | Unique identifier assigned to each employee                       |
| `Employee_Name`     | Name of the employee                                              |
| `Department`        | Department in which the employee works                            |
| `Job_Title`         | Employee's job position                                           |
| `Age`               | Age of the employee                                               |
| `Gender`            | Gender of the employee                                            |
| `Annual_Salary`     | Annual salary of the employee                                     |
| `Experience_Years`  | Total years of professional experience                            |
| `Joining_Date`      | Date the employee joined the company                              |
| `City`              | Employee's city                                                   |
| `Performance_Score` | Employee performance rating                                       |
| `Work_Mode`         | Employee's working arrangement such as Remote, Hybrid, or On-site |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Jupyter Notebook / Google Colab**

---

## 🧹 Data Cleaning Techniques

The project uses several Pandas data-cleaning techniques.

### Missing Values

Missing values are identified using:

```python
df.isnull().sum()
```

Different strategies are applied depending on the type of data.

* Numerical columns → median imputation
* Categorical columns → mode imputation
* Employee names → `"Unknown"`
* Joining dates → retained as missing rather than inventing dates

### Duplicate Records

Duplicate rows are identified and removed using:

```python
df.duplicated()
df.drop_duplicates()
```

Duplicate `Employee_ID` records are also checked separately.

### Data Type Correction

Numerical columns such as:

* Age
* Annual Salary
* Experience Years
* Performance Score

are converted to appropriate numeric data types.

The `Joining_Date` column is converted to the datetime format.

### Inconsistent Values

Categorical values are standardized.

For example:

```text
m
M
male
Male
```

are standardized to:

```text
Male
```

Similarly, variations in department and work-mode values are standardized.

### Invalid Values

The dataset is checked for invalid values such as:

* Age below 18 or above 100
* Negative experience
* Zero or negative salary
* Performance scores outside the expected range

Invalid values are converted to missing values and handled using suitable imputation methods.

---

## 🔄 Data Cleaning Workflow

```text
Raw Employee Dataset
        │
        ▼
Load Dataset with Pandas
        │
        ▼
Initial Dataset Inspection
        │
        ├── Missing Values
        ├── Duplicate Records
        ├── Data Types
        ├── Inconsistent Values
        └── Invalid Values
        │
        ▼
Data Cleaning
        │
        ├── Remove Duplicates
        ├── Handle Missing Values
        ├── Standardize Categories
        ├── Correct Data Types
        └── Handle Invalid Values
        │
        ▼
Final Validation
        │
        ▼
Before vs After Comparison
        │
        ▼
Cleaned Employee Dataset
        │
        ▼
CSV Export
```

---

## 📁 Project Structure

```text
Employee-Data-Cleaning/
│
├── messy_company_employee_dataset.csv
├── cleaned_company_employee_dataset.csv
├── Employee_Data_Cleaning.ipynb
├── cleaning_summary.txt
├── README.md
└── .gitignore
```

> The raw and cleaned datasets may be excluded from GitHub if they contain sensitive or confidential employee information.

---

## 📈 Before vs After Validation

The project evaluates the dataset before and after cleaning using metrics such as:

* Number of rows
* Number of columns
* Total missing values
* Number of duplicate records
* Data types
* Dataset structure

Example:

| Metric         | Before Cleaning | After Cleaning |
| -------------- | --------------: | -------------: |
| Rows           |        Original |        Cleaned |
| Columns        |        Original |        Cleaned |
| Missing Values |          Higher |        Reduced |
| Duplicate Rows |         Present |        Removed |
| Data Types     |    Inconsistent |      Corrected |

The actual values are generated automatically when the notebook is executed.

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Employee-Data-Cleaning.git
```

### 2. Navigate to the Project

```bash
cd Employee-Data-Cleaning
```

### 3. Install Dependencies

```bash
pip install pandas numpy jupyter
```

### 4. Open the Notebook

```bash
jupyter notebook
```

Open:

```text
Employee_Data_Cleaning.ipynb
```

### 5. Run the Notebook

Execute the cells sequentially.

The notebook will:

1. Load the dataset.
2. Inspect the data.
3. Detect data-quality issues.
4. Clean the dataset.
5. Validate the cleaned data.
6. Generate a before-and-after comparison.
7. Export the cleaned dataset.

---

## 📤 Output Files

After execution, the project generates:

### Cleaned Dataset

```text
cleaned_company_employee_dataset.csv
```

This file contains the cleaned and standardized employee records.

### Cleaning Summary

```text
cleaning_summary.txt
```

This file contains a brief summary of the cleaning operations and before/after statistics.

---

## 💡 Key Learning Outcomes

Through this project, the following concepts are demonstrated:

* Pandas DataFrame operations
* Data inspection
* Data quality analysis
* Missing-value handling
* Mean/median/mode imputation
* Forward filling
* Duplicate detection
* Duplicate removal
* Categorical data standardization
* Data type conversion
* Date handling
* Outlier and invalid-value detection
* Dataset validation
* CSV data export

---

## 🚀 Future Improvements

The project can be extended by adding:

* Automated data-quality reports
* Outlier detection using IQR and Z-score methods
* Data visualization using Matplotlib and Seaborn
* Interactive dashboards
* Automated validation rules
* Data-quality scoring
* Logging of every cleaning operation
* A reusable data-cleaning pipeline
* Machine-learning-based anomaly detection

---

## 📄 License

This project is intended for educational and learning purposes.

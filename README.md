# Financial Loan Portfolio Analysis

## Project Overview

This project provides a comprehensive analysis of financial loan data. The primary objective is to perform an exploratory data analysis (EDA) to understand the key characteristics of the loan portfolio, identify trends in loan applications, and evaluate key performance indicators (KPIs) related to loan funding and repayment. The insights derived from this analysis can be used to inform risk assessment, guide marketing efforts, and improve overall portfolio management.

## Dataset

The analysis is based on the `financial_loan.csv` dataset, which contains 38,576 records of individual loan applications.

**Key columns in the dataset include:**

* `id`, `member_id`

* `loan_amount`, `term`, `int_rate`, `installment`

* `grade`, `sub_grade`, `purpose`

* `emp_length`, `home_ownership`, `annual_income`, `dti`

* `issue_date`, `loan_status`

* `total_payment`, `total_acc`

## Analysis Steps

The project was carried out in a Jupyter Notebook (`Financial_Loan_Analysis_Notebook.ipynb`) and involved the following steps:

### 1. Data Cleaning and Preparation

* **Import Libraries:** Loaded necessary Python libraries including Pandas, NumPy, Matplotlib, Seaborn, and Plotly.

* **Load Data:** The `financial_loan.csv` dataset was loaded into a Pandas DataFrame.

* **Handle Missing Values:** Missing values in categorical columns were filled with the mode, and numerical columns were filled with the median.

* **Data Type Conversion:** Date-related columns were converted to a datetime format for time-series analysis.

* **Feature Engineering:** New columns were created to enhance the analysis:

  * `ISSUE_MONTH` and `ISSUE_YEAR` were extracted from the `issue_date`.

  * `LOAN_CONDITION` was created to classify loans as 'Good Loan' (Fully Paid, Current) or 'Bad Loan'.

### 2. Key Performance Indicator (KPI) Analysis

Several key metrics were calculated to summarize the portfolio's performance:

* **Total Loan Applications:** 38,576

* **Total Funded Amount:** $435.76M

* **Total Amount Received:** $473.07M

* **Average Interest Rate:** 12.05%

* **Average Debt-to-Income (DTI) Ratio:** 13.33%

* **Good vs. Bad Loan Breakdown:**

  * **Good Loans:** 86.18% of applications.

  * **Bad Loans:** 13.82% of applications.

### 3. Exploratory Data Analysis (EDA) & Visualization

The data was visualized to identify trends and patterns across different dimensions:

* **Monthly Trends:** A line chart shows the total number of loan applications by month, revealing seasonal patterns.

* **State-Level Analysis:** A bar chart highlights the top 20 states with the highest number of loan applications, with California, New York, and Florida leading.

* **Loan Term Distribution:** A donut chart illustrates that 36-month loans are significantly more common than 60-month loans.

* **Employment Length:** A bar chart shows that borrowers with 10+ years of employment are the largest group of applicants.

* **Loan Purpose:** Debt consolidation is the most frequent reason for obtaining a loan, followed by credit card refinancing.

* **Home Ownership:** A treemap visualizes the distribution of loans by home ownership status, with most borrowers either renting or having a mortgage.

## Conclusion

The analysis provides a detailed snapshot of the loan portfolio. Key takeaways include the high prevalence of **36-month loans** for the purpose of **debt consolidation**. The typical borrower is likely to have **10+ years of work experience** and either **rents or has a mortgage**. Geographically, loan applications are concentrated in states like **California, New York, and Florida**. While the majority of the portfolio (86.18%) consists of 'Good Loans', the 13.82% identified as 'Bad Loans' warrants further investigation to refine risk models.

These findings can be used to optimize lending criteria, develop targeted marketing campaigns for key demographics, and improve risk management strategies.

## Tools and Libraries Used

* **Python 3**

* **Pandas & NumPy:** For data cleaning and manipulation.

* **Matplotlib & Seaborn:** For static data visualizations.

* **Plotly Express:** For interactive visualizations.

* **Jupyter Notebook:** As the analytical environment.

## How to Run This Project

1. **Prerequisites:**

   * Python 3 installed.

   * Jupyter Notebook or a compatible environment (like Google Colab) installed.

2. **Installation:**
   Install the necessary Python libraries:

pip install pandas numpy matplotlib seaborn plotly jupyter
3. **Execution:**

* Ensure `Financial_Loan_Analysis_Notebook.ipynb` and `financial_loan.csv` are in the same directory.

* Launch Jupyter Notebook:

  ```
  jupyter notebook
  
  ```

* Open the notebook and run the cells sequentially to view the analysis and visualizations.

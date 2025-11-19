#  Credit Risk Analysis — Case Study (EDA Project)

This project focuses on analyzing a loan dataset to understand customer behaviour, income levels, loan intentions, default patterns, and risk indicators.  
The objective is to apply Exploratory Data Analysis (EDA) techniques and provide actionable insights for financial decision-making.

---

## 1. Introduction

Credit risk analysis enables financial institutions to assess the likelihood of a customer defaulting on a loan.  
Through this case study, we explore:

- Customer demographics  
- Income and employment patterns  
- Loan behaviour  
- Default tendencies  
- Key relationships between variables  


##  2. Dataset Description

| Column | Meaning |
|--------|---------|
| **person_age** | Customer age |
| **person_income** | Annual income |
| **person_home_ownership** | RENT / OWN / MORTGAGE |
| **person_emp_length** | Employment length (years) |
| **loan_intent** | Purpose of loan (e.g., Personal, Medical, Education) |
| **loan_grade** | Loan grade (A = best, G = worst) |
| **loan_amnt** | Loan amount |
| **loan_int_rate** | Interest rate (%) |
| **loan_status** | 1 = Default, 0 = No default |
| **loan_percent_income** | Loan as % of income |
| **cb_person_default_on_file** | Past default (Y/N) |
| **cb_person_cred_hist_length** | Credit history length (years) |


# 3. EDA Framework

A systematic approach to explore and understand the dataset.

##  3.1 Data Loading
- Load the dataset  
- Display sample rows  
- Check data types  


##  3.2 Data Cleaning
- Handle missing values  
- Remove duplicates  
- Treat outliers  
- Convert incorrect data types  

#  4. Exploratory Data Analysis (EDA)


#  4.1 Univariate Analysis  
Analysis of **one variable at a time**.


## **A. Discrete Data** (Categorical or Numerical-Discrete)

### ✔ Statistical (Non-Visual)  
**Purpose: Summarize frequency and category behaviour**

- `count`  
- `nunique`  
- `unique`  
- `value_counts`

###  Visual  
**Purpose: View distribution and detect unusual patterns**

- Bar Plot  
- Count Plot  


## **B. Continuous Numerical Data** (Real numbers)

###  Statistical (Non-Visual)  
**Purpose: Understand central tendency + spread**

- `min`, `max`  
- `sum`  
- `mean`, `median`  
- `var`, `std`  
- `range`  
- `IQR`  

### Visual  
**Purpose: Study distribution + identify outliers**

- Histogram  
- KDE Plot  
- Box Plot  


# 4.2 Bivariate Analysis  
Analysis of **two variables together** to understand relationships.


## **A. Continuous Numerical vs Continuous Numerical**

###  Statistical  
- Pearson Correlation Coefficient  

**Purpose:** Detect linear or non-linear relationships.

###  Visual  
- Scatter Plot  

---

## **B. Continuous Numerical vs Discrete Data**

###  Statistical  
**Purpose:** Compare behaviour across groups  
- Group Mean  
- Group Median  
- Group Std  

###  Visual  
- Box Plot  
- Histogram  

---

## **C. Discrete vs Discrete Data**

###  Statistical  
- Cross-tabulation (Frequency Tables)  

**Purpose:** Check dependency between categorical groups.

###  Visual  
- Stacked Bar Plot  
- Unstacked Bar Plot  



# 5. Final Summary

This case study demonstrates how to:

- Clean and preprocess financial datasets  
- Perform detailed univariate and bivariate analysis  
- Interpret relationships between key variables  
- Translate data patterns into meaningful business insights  

This project serves as a practical EDA example for learners, analysts, and anyone exploring credit-risk datasets.

---


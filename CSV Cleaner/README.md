Credit Customer Data Cleaning & Preprocessing

This project provides a step-by-step workflow for cleaning and preparing credit customer data in Python using pandas. The objective is to transform a raw credit scoring dataset into a refined, analysis-ready form, suitable for statistical analysis or machine learning applications.

📂 Dataset Description
The input dataset (credit_customers.csv) consists of credit and demographic information for 1,000 customers with the following variables:

Credit_amount: Credit requested/approved (numeric)

Age: Customer’s age (numeric)

Housing: Housing type (categorical: e.g., 'own', 'for free')

Existing_credits: Number of existing credits at this bank (numeric)

Job: Job type/status (categorical)

Own_telephone: Telephone possession (categorical)

Foreign_worker: Whether the customer is a foreign worker (categorical)

Class: Creditworthiness class (target; originally 'good'/'bad', converted to 1/0)

Original columns included many more features and categorical fields (such as 'checking_status', 'credit_history', etc.) that are dropped in this cleaning pipeline for analysis relevance.

✨ Cleaning & Preprocessing Steps
The data pipeline proceeds as follows:

Import and Initial Inspection

Load data with pandas.

Examine data structure, column names, types, and missing values.

Drop Irrelevant Columns

Retain only analytic and target features (as above).

Remove all others, including 'savings_status' and intermediary attributes.

Rename Columns for Consistency

Title-case all columns for clarity and a uniform look (e.g., 'credit_amount' → 'Credit_amount').

Remove Duplicate Rows

Check for duplicate records and drop them to preserve unique entries and integrity.

Handle Missing Values

Identify and remove any rows with null (NaN) values.

Encode Target Variable

Convert 'Class' from strings ('good'/'bad') to binary (1 for 'good', 0 for 'bad').

Data Type Corrections

Ensure 'Existing_credits' is stored as integer.

Export Cleaned Data

Save the cleaned DataFrame as cleaned_credit_customers.csv.

📝 Usage
Prerequisites
Python 3.12+

Running the Code
Place credit_customers.csv in your working directory.
Execute the Jupyter notebook, or the equivalent Python script using any Python environment.
On successful completion, a cleaned version, cleaned_credit_customers.csv, will be generated.

🧹 Key Outcomes
All duplicate and missing rows are removed for maximum reliability.
Target column ('Class') converted from categorical to binary integer.
User-friendly, analysis-ready columns and consistent data types.
The resulting table is now ideal for predictive modeling, statistics, or business analytics.
🧑💻 Author & Credits
Data cleaning performed by: [Sabin Shah]

Contact: [sabinshah619@gmail.com]
Dataset Source: [Kaggle]
Notebook environment: Jupyter, pandas v2.2.3

📎 License
You are welcome to use, adapt, and distribute this code for any application. Attribution is appreciated!

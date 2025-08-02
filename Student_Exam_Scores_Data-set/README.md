Student Performance Data Cleaning & Preprocessing
This project demonstrates a comprehensive workflow for cleaning and preprocessing student performance data using Python and pandas. The goal is to prepare high-quality, analysis-ready data from a raw dataset containing demographic information and exam scores. The cleaned data can be subsequently used for data analysis or as input for machine learning models.
📂 Dataset Description
The raw dataset (Expanded_data_with_more_features.csv) contains information about 30,641 students and the following columns:

Gender: Student gender

EthnicGroup: Student’s ethnic group

ParentEduc: Parental education level

LunchType: Type of lunch received

TestPrep: Test preparation course status

ParentMaritalStatus: Parent's marital status

PracticeSport: Whether the student practices sports

IsFirstChild: Whether the student is the first child

NrSiblings: Number of siblings

TransportMeans: Primary means of transport

WklyStudyHours: Weekly study hours

MathScore, ReadingScore, WritingScore: Scores in respective subjects

✨ Cleaning & Preprocessing Steps
The pipeline follows these key steps:

Import and Inspect Data

Load data using pandas.

Check structure, missing values, and data types.

Drop Irrelevant or Redundant Columns

Remove unnecessary columns (Unnamed: 0, TestPrep, ParentMaritalStatus, PracticeSport, IsFirstChild).

Rename Columns for Clarity

Rename ambiguous columns for better readability (e.g. NrSiblings → No: of Siblings).

Remove Duplicate Rows

Identify and drop any exact row duplicates for data integrity.

Handle Missing Values

Drop any row containing NaN values in crucial columns to ensure analysis will not be biased or error-prone.

Convert Data Types / Encoding

Convert categorical variables to numerical values where appropriate (e.g. Gender: female → 1, male → 0).

Ensure column data types match analytic needs (e.g. convert sibling count to integer).

Reset Index

Reset the DataFrame index for consistency and easier referencing after row drops.

Export Cleaned Data

Save the preprocessed data in both .csv and .xlsx formats for further use.

📝 Usage
Prerequisites
Python 3.12+
pandas

Running the Code
Place the raw CSV file in your working directory.

Run the Jupyter notebook or execute the Python code in your environment.

On completion, two cleaned files are generated:

Cleaned_csv_data.csv
Cleaned_excel_data.xlsx

🧹 Key Outcomes
Reduced data from 30,641 to 22,343 rows of complete and reliable records.

All categorical values and data types made analysis- and machine learning-ready.

Consistent and clear feature naming.

No duplicate or missing values remain in the cleaned file.

🧑 Author & Credits
Data cleaning performed by: [Sabin Shah]

Contact: [sabinshah619@gmail.com]

Dataset Source: [Kaggle]

Notebook environment: Jupyter, pandas v2.2.3

📎 License
You are free to use, modify, and share this code for educational, research, or commercial purposes. Attribution appreciated!


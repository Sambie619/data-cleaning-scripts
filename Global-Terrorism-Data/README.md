Global Terrorism Data Cleaning & Preprocessing
📊 Project Overview
The Global Terrorism Database (GTD) contains detailed information on terrorist events from 1970 to 2020, including location, tactics, targets, casualties, responsible parties, and more (over 200,000 rows and 100+ columns). However, the raw data is messy, full of missing values, inconsistent categories, mixed data types, and structural quirks—making direct analysis difficult and unreliable.
This project delivers:
Consistent, cleaned, and well-documented data for analysis or machine learning
Systematic handling of missing values, inconsistent values, and noisy categories
Transformation of columns into easily understandable, standardized formats

📋 Features
Data Inspection: Overview and audits of the raw GTD data structure.
Column Selection: Prunes unused columns, retaining only those critical for research and modeling.
Missing Value Imputation: Sensible fillers for categorical/text and numerical columns, e.g., "Unknown" or zero.
Duplication Removal: Safely eliminates duplicated entries.
Data Consistency: Standardizes cases, removes leading/trailing whitespace, and unifies naming across all categorical columns.
Date Fixes: Handles missing/invalid months and days, creates a single datetime column for ease of time-series work.
Type Conversions: Ensures numerical columns (killed, wounded) are integers.
Error Correction: Harmonizes key fields like group names, countries, attack types, and target types.
Structural Validation: Validates final index, column order, datatypes, and completeness.
Outlier Handling: Visualizes and reviews outliers in casualties, provides guidance on interpretation.

🚦 How To Use
Requirements
Python 3
pandas, numpy, seaborn, matplotlib
Data Flow
Place the original GTD Excel (globalterrorismdb_0522dist.xlsx) in the working directory.
Run the notebook or scripts. All major cleaning stages are annotated and reproducible.
Outputs
Cleaned_GTD.csv and Cleaned_GTD1.xlsx
Analysis-ready, indexed, and standardized datasets.

🧹 Cleaning Steps Explained
Stage	                       Description
Data Audit	                 Inspect format, columns, types, missingness, uniqueness, value counts
Initial Column Selection	   Retain key columns for date, region, type, perpetrator, casualties, geo, etc.
Missing Data Imputation	     Fill NAs: categorical texts with 'Unknown', numerics with 0
Standarize Categories	       Strip spaces, lower/title-case, fix typos and variants
Deduplication	               Remove duplicate incident entries
Date Handling	               Impute missing month/day, create single datetime column
Outlier Identification	     Visualize & review (do not remove rare real atrocities)
Final Validations	           All-null check, type conversion, index reset

🧩 Key Columns in the Cleaned Dataset
Year / Month / Day / Date: Full event date (datetime)

Country / Region: Cleansed and title-cased

Attack_type / Weapon_type / Target_type: Standardized event characteristics

Killed / Wounded: Always integer, zero for unknown/none

Group_name: Responsible group (always title-cased; ‘Unknown’ where not claimed)

Is_claimed: 1=Claimed, 0=Not, ‘Unknown’ for unclear

Is_suicide: 1=Suicide attack, 0=Not

Summary / Motive: Text with missing handled

Latitude / Longitude: Geocoded, complete for all rows

🔍 Usage Suggestions
Ready for statistical analysis, dashboards, geospatial mapping, and ML modeling.
All fields are explained and harmonized—no more mysterious codes or missing rows.
For the rare remaining ambiguities, clear placeholder values and documentation are included.

🚀 Extend and Contribute
Pull requests are welcome! If you build new ML modeling, exploratory analyses, or visualizations from this cleaned dataset, please contribute back or open issues for improvements.

📂 Files Included
DataCleaning4.ipynb: Full project notebook/code (cleaning pipeline)
Cleaned_GTD.csv / Cleaned_GTD1.xlsx: Output datasets
Cleaned_GTD1.xlsx/cleaned excel workbook
README.md: This documentation

🙏 Acknowledgments
Original Data Source: National Consortium for the Study of Terrorism and Responses to Terrorism (START), University of Maryland.

🧑💻 Author & Credits
Data cleaning performed by: [Sabin Shah]
Contact: [sabinshah619@gmail.com]
Notebook Environment: Jupyter, pandas v2.2.3

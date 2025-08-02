Fashion Dataset Data Cleaning & Preprocessing
This project presents a thorough cleaning and preprocessing pipeline for a large fashion product dataset using Python and pandas. The focus is on producing a reliable, analysis-ready file from a raw e-commerce fashion catalog, ideal for exploratory analysis, BI, or machine learning.

📂 Dataset Description
The raw data file (FashionDataset.csv) contains over 30,000 rows of women's fashion products with these fields:

BrandName: Brand selling the item

Details: Full product description (style/material/fit)

Sizes: Available size options (may include error codes or NA)

MRP: Maximum Retail Price (with “Rs\n” prefix in original)

SellPrice: Current listed price

Discount: Percentage or phrase (“50% off”, “No Discount”)

Category: Product category, e.g. 'Westernwear-Women'

✨ Cleaning & Preprocessing Steps
The workflow applies these main steps:

Import and Exploration

Load with pandas, inspect columns, sizing, data types, and first/last rows.

Drop Redundant Columns

Remove irrelevant index columns (e.g., Unnamed: 0).

Rename Mislabelled Columns

Fix typos for clarity (Deatils → Details).

Remove Duplicates

Identify and drop exact duplicate rows to ensure uniqueness.

Data Reset

Reset DataFrame index post-cleaning.

Handle Missing Values

Drop any rows with NaNs in required fields.

String Normalization

Capitalize brand names and details for uniformity.

Standardize how missing entries are represented:

Replace "Nan" in Sizes with "NA Values", then filter out "NA Values" rows (true missing size info).

Set "Nan" in Discount to "No Discount" in discount column.

Final Integrity Correction

Final reset of DataFrame index for consecutiveness.

Ensure columns are cleanly separated and well-named.

Export Cleaned Data

Save the processed file to both cleaned_csv.csv and cleaned_excel.xlsx formats.

After cleaning: The dataset is reduced to 22,687 valid, unique items with reliably structured information.

📝 Usage
Prerequisites
Python 3.12+
pandas

Running the code
Place FashionDataset.csv in your working directory.

Run the Jupyter notebook or Python script.

After successful execution, you’ll get two files:
cleaned_csv.csv
cleaned_excel.xlsx

🧹 Key Outcomes
Reduced entries from over 30,000 to 22,687 valid items.

All textual fields are cleaned and standardized (capitalization for consistency).

Downgraded “Nan”/“NA Values” cleaned/removed.

Only items with valid size information retained.

No duplicate or missing rows.

Dataset is ready for analytics, BI tools, or ML pipelines.

🧑💻 Author & Credits
Data cleaning performed by: [Sabin Shah]

Contact: [sabinshah619@gmail.com]

Dataset Source: [Kaggle]

Notebook Environment: Jupyter, pandas v2.2.3

📎 License
You are free to use, share, or modify this code for any educational or commercial application. Attribution is appreciated!

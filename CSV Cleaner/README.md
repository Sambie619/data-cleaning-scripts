->This notebook CSV Cleaner demonstrates some of the basic data cleaning techniques.
->A csv file [text](credit_customers.csv) consisting of 21 columns and 1000 rows  is loaded using pandas
->Columns of less significance like 'checking_status', 'duration', 'credit_history', 'purpose','employment','installment_commitment', 'personal_status', 'other_parties', 
'residence_since', 'property_magnitude','other_payment_plans', 'num_dependents' are droped so as to focus on columns of business importance
->Then for capitalizing the exisitng column names ,used .capitalize()
->Checked for duplicated rows using duplicated() and droped using drop_duplicates()
->Checked for NULL columns using isna()and droped using dropna()
->Changes object values of class column like ['good', 'bad'] to 1 & 0 respectively using: data["Class"]=data["Class"].apply(lambda x:1 if x=="good" else 0)
->The values of the column Existing_credits seemed messy to me like it was of float data type so changes it to int data type using: data["Existing_credits"]=data["Existing_credits"].astype(int)
->Final cleaned data set is exported to a csv file [text](cleaned_credit_customers.csv)


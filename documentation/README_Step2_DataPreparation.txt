Customer Churn Diagnostic
Step 2: Data Understanding & Preparation

Objective:
	To import, inspect, clean, and structure the raw customer churn dataset so it becomes ready for exploratory analysis. This step ensures data accuracy, consistency, and analytical usability while maintaining full transparency of cleaning decisions.

Data Source:
	Dataset: Telco Customer Churn - downloaded from Kaggle
		Saved as: data_raw/customer_churn_raw.csv
	Although designed for the telecom churn, the structure aligns well with CloudWorks' SaaS model for this project's narrative. 

Steps: 
	1. Import & Structure
		Loaded the raw CSV into Excel (file: churn_working.xlsx, sheet: churn_raw_import sheet).
		Verified row count (7,043 records).
		Identified key columns for analysis (customer attributes, services, billing, churn flag).
	2. Data Dictionary Creation
		Created sheet dictionary defining: Column names, Descriptions, Data types (categorical, numeric, string)
	3. Initial Data Quality Review
		Checked for missing values, blanks, spacing, inconsistent labels.
		Observed:
			TotalCharges contained blanks for customers with tenure = 0.
			Potentially inconsistent formatting present in categorical fields (Yes/yes, No/no).
	4. Cleaning Actions
		4A. Missing Value Treatment
			TotalCharges blanks replaced with 0 since tenure = 0 means no billing yet.
			Documented this assumption in the cleaning plan (sheet: clean_plan).
		4B. Standardisation of Categorical Fields
			Applied Find + Replace (no helper columns) to ensure: "yes" was replaced with "Yes" and "no" was replaced with "No".
			Remove double spaces if present (e.g., "No internet service")
			Fields standardized include:Partner, Dependents, PhoneService, MultipleLines, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, PaperlessBilling, Churn.
		4C. Derived Fields Created
			Added two new columns:
				tenure_group (customer lifecycle buckets)
					=IF(A2="", "",
					  IF(F2<6, "New (0–6 months)",
					  IF(F2<12, "Early (6–12 months)",
					  IF(F2<24, "Established (1–2 years)",
					  IF(F2<48, "Mature (2–4 years)",
					  "Long-term (4+ years)"))))
					)
				total_revenue (lifetime revenue)
					=IF(A2="", "", MonthlyCharges * tenure)
	5. Save Clean Version
		Saved cleaned dataset as:
			analysis/churn_working/churn_clean.xlsx
			data_clean/churn_clean.csv
			data_clean/churn_clean.xlsx

Key Findings: 
	The dataset contains ~26.5% churn (Churn = Yes) and ~73.4% retention (Churn = No), consistent with typical SaaS churn ranges.
	All tenure = 0 customers were correctly marked as Churn = No, confirming dataset logic.
	TotalCharges missing values were structurally valid and fixed.
	No duplicate CustomerIDs detected.
	Categorical inconsistencies verified for clean analysis.

Outputs Created: 
	documentation/data_dictionary_customer_churn.xlsx
	analysis/churn_working.xlsx	
		sheets: churn_clean, churn_raw_import, clean_plan
	data_clean/churn_clean.csv
	data_clean/churn_clean.xlsx

Next Step: 
	Exploratory Analysis & Diagnostics 

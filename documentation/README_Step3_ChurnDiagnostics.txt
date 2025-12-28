Customer Churn Diagnostic
Step 3: Churn Diagnostics & Root Cause Analysis

Objective:
	Diagnose why customers churn by combining quantitative churn patterns with qualitative behavioural signals.

Data Source: 
	Cleaned customer churn dataset (churn_clean.xlsx) derived from public Telco churn data, interpreted as a SaaS context.

Steps:
	1. Segment-level churn analysis using pivot tables as follows:
		Churn Distribution by Contract Type (%): Percentage of customers churned (yes/no) for each type of contract (month-to-month, one year, two year).
		Churn Distribution by Tenure Group (%): Percentage of customers churned (yes/no) for each type of tenure group (early, established, long-term, mature, new).
		Churn Distribution by Tech Support (%): Percentage of customers churned (yes/no) based on the subscribed tech support. 
	2. Identification of high-risk customer profiles.
	3. Qualitative signal synthesis aligned with quantitative evidence
		5 qualitative signals (Q1-Q5) created with corresponding group (pricing & contract, product usage, service & support, payment & billing, onboarding & experience) and code 
	4. Integration of findings into diagnostic insights
		Insight IDs (I1-I4) created basis the qualitative signals and interpreted each of them

Key Findings:
	Month-to-month contracts exhibit the highest churn
	New customers (0–6 months) are most vulnerable
	Lack of technical support increases churn risk
	Higher monthly charges correlate with churn

Outputs:
	analysis/churn_clean.xlsx
		Sheet: pivots_churn_analysis
			Pivot tables: churn by contract, tenure group, tech support
		Sheet: qualitative_signals
			Qualitative signals table (Q1–Q5)
		Sheet: summary_churn_metrics
			Diagnostic insight summary (I1–I4)
			
Next Step:
	Translate diagnostics into actionable retention strategies and business recommendations.
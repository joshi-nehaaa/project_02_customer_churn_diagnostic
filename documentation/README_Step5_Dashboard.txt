Customer Churn Diagnostic
Step 5: Dashboard & Visual Summary

Objective: 
	To create a concise, decision-ready dashboard that visually summarises customer churn patterns, high-risk segments, and key business metrics, enabling stakeholders to quickly understand churn drivers and prioritise retention actions.

Data Source:
	Cleaned customer churn dataset (churn_clean.xlsx) derived from public Telco churn data, interpreted as a SaaS context.
	Data prepared and validated in Step 2 and analysed in Steps 3–4

Steps: 
	KPI Definition
		Defined core churn KPIs: Total Customers, Churn Rate, Retention Rate, Churned Customers, and High-Risk Customer Segment.
		KPIs were first structured in Excel (sheet: dashboard_kpis) to validate values and layout.
	Dashboard Design in Power BI
		Imported cleaned churn dataset into Power BI.
		Created KPI cards for high-level metrics similar to the one created in Excel (dashboard_kpis)
		Built visualisations to show:
			Churn by Contract Type
			Churn by Tenure Group
			Churn by Tech Support subscription
		Added interactive slicers for Contract, Tenure Group, and Tech Support.
	Visual Consistency & Storytelling
		Applied a consistent colour palette aligned with the Excel dashboard.
		Used percentage-based and count-based charts appropriately depending on analytical intent.
		Added clear titles, subtitles, and legends to guide interpretation.
	Export & Documentation
		Exported the final dashboard as a static PDF for portfolio and stakeholder review.
		Saved Power BI file for reproducibility and future enhancement.

Key Findings: 
	Customers on month-to-month contracts exhibit the highest churn risk.
	Early-tenure customers (0–6 months) represent the most vulnerable segment.
	Lack of technical support is associated with higher churn.
	A small number of high-risk segments contribute disproportionately to overall churn.

Outputs: 
	analysis/churn_clean.xlsx
		Sheet: dashboard_kpis
	Interactive Power BI dashboard file
		analysis/churn_dashboard.pbix
	Static executive dashboard for portfolio use
		outputs/churn_dashboard.pdf
		outputs/churn_dashboard.png

Next Step:
	Portfolio Packaging on GitHub and Notion

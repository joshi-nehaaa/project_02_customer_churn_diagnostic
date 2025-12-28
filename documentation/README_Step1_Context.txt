Customer Churn Diagnostic
Step 1A: Business Scenario Definition

Company Type
	CloudWorks is a fictitious, mid-sized UK-based SaaS company offering a subscription-based B2B project management and productivity platform.

Business Context
	The company serves small and medium-sized businesses through monthly and annual subscription plans.
	Over the past year, CloudWorks has observed an increase in customer churn, particularly within the first 12 months of subscription, raising concerns about onboarding effectiveness and early product adoption.

Business Impact
	Customer churn directly impacts recurring revenue and customer lifetime value, while increasing dependency on sales and marketing to replace lost customers.
	Reducing churn is therefore more cost-effective than acquiring new customers and has become a strategic priority for the business 

Business Questions
	Which customer segments are most at risk of churn?
	What behavioral, usage, or service-related factors are associated with churn?
	What data-driven interventions can be designed to improve customer retention?

Step 1B: Stakeholders & Decisions

Key Stakeholders
	Cusomter Success (CS): Responsible for onboarding, renewals, reducing early-stage churn.
	Product Management: Uses churn insights to prioritise feature improvements and fix usability gaps. 
	Analytics / Operations Team: Monitors churn KPIs, builds dashboards, tracks retention performance
	Management: Needs high-level view of churn risk, revenue impact, and intervention priorities. 

Decisions This Analysis Informs
	Which customer segments should be prioritised for retention efforts?
	When to trigger proactive interventions (eg: onboarding support, check-ins)?
	Whether churn is driven more by product usage, service experience or pricing structure?
	How to allocate CS resources to maximise retention impact? 

Success Criteria
	Clear identification of high-risk churn segments. 
	Actionable insights that can be translated into retention strategies. 
	Metrics suitable for ongoing tracking via dashboards. 

Step 1C: Churn Definition

What Churn Means for CloudWorks	
	Churn is defined as a customer actively cancelling their subscription. 
	A customer is considered churned if any one of the following is true: 
		Their subscription status changed to "Cancelled" 
		The churn flag equals 1 in the dataset
	The analysis focuses on early churn, that is, occurring within the first 12 months of the subscription. 
	Churn is treated as a binary outcome: 
		1 = Churned
		0 = Retained

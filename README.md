📘 Customer Churn Analysis – Project Report
📌 Objective
The goal of this project is to understand the factors influencing customer churn in a telecom company. By identifying patterns and correlations in customer behavior and service usage, the business can take proactive steps to reduce churn and improve customer retention.
🧹 Data Cleaning & Preparation
✅ Steps Performed:
1.	Handled Missing Values:
o	TotalCharges had blanks → replaced with 0, then converted to float.
o	Verified no other columns had significant nulls.
2.	Data Type Conversion:
o	SeniorCitizen converted from 0/1 to Yes/No for clarity.
o	Ensured correct types for numerical features (MonthlyCharges, TotalCharges, tenure).
3.	Duplicates:
o	Checked for duplicated rows and customer IDs.
o	Result: ✅ No duplicates found.
4.	Data Transformation:
o	Categorical values standardized for visualization.







📊 Exploratory Data Analysis (EDA)
1. Overall Churn Rate
•	Churned Customers: 1,869 out of 7,043 → 26.5%
•	Non-Churned: 5,174 → 73.5%
🔍 Insight: The dataset is imbalanced, with significantly more non-churners.
________________________________________
2. Demographic Insights
Feature	Churn Rate (Yes)	Notable Patterns
Gender	Female: 26.5%, Male: 26.1%	Gender has no significant effect on churn.
Senior Citizen	Yes: 41.7%, No: 24.1%	Seniors churn ~1.7x more than non-seniors.
Partner	No: 32.1%, Yes: 20.4%	No partner → Higher churn.
Dependents	No: 31.0%, Yes: 15.7%	Customers without dependents are 2x more likely to churn.
________________________________________
3. Service Subscription Behavior
Service Feature	Churn Rate (Yes)	Observations
Phone Service	No: 7.1%, Yes: 27.2%	No phone = low churn, but small sample size.
Internet Service	DSL: 19.0%, Fiber optic: 42.4%, No internet: 7.5%	Fiber optic users churn the most.
Online Security	No: 36.9%, Yes: 15.2%	Strong correlation with churn.
Tech Support	No: 37.3%, Yes: 14.0%	Customers with tech support churn much less.
Streaming Services	No clear effect. Both TV & Movies churn rates ~27%.	Entertainment features don’t influence churn much.
________________________________________
4. Contract & Billing Insights
Feature	Churn Rate (Yes)	Observations
Contract Type	Month-to-month: 43.9%, One year: 11.0%, Two year: 2.8%	Major driver! Long-term contracts = high retention.
Paperless Billing	Yes: 33.7%, No: 16.1%	Paperless billing customers churn 2x more.
Payment Method	Electronic check: 45.2%, Other methods: ~15-22%	Highest churn from electronic check users.
________________________________________
5. Tenure & Charges
Metric	Churn Tendency
Tenure	Lower tenure → higher churn. Most churners are <10 months.
Monthly Charges	Churn increases with higher charges.
Total Charges	Churners have significantly lower total charges, indicating shorter retention.
________________________________________





📌 Executive Summary
This churn analysis reveals contract type, senior status, and support services as the most influential churn drivers. Customers on month-to-month plans, those without technical support, and senior citizens exhibit significantly higher churn rates.
Moreover, billing type and payment method strongly influence retention. Customers using electronic checks and paperless billing churn at much higher rates.
🔑 Key Risk Segments:
•	Month-to-month subscribers without online support or bundled services.
•	Senior citizens without dependents or partners.
•	Customers paying via electronic checks.

📌 Recommendations
1.	🎯 Targeted Retention Campaigns:
o	Focus on month-to-month and new users (<6 months tenure).
o	Offer incentives for long-term contract upgrades.
2.	🛡️ Promote Security & Tech Support Services:
o	Bundle with plans to improve perceived value and stickiness.
3.	🏦 Improve Payment Flexibility:
o	Discourage use of electronic checks; promote auto-pay methods.
4.	📬 Paperless Billing Evaluation:
o	Examine UX and comms for digital billing – possibly a friction point.


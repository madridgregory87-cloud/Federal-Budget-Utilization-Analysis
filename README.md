# Federal-Budget-Utilization-Analysis
An analysis of FY2023 Q4 federal agency spending and resource utilization, identifying multi-sector budget gaps and proposing audit frameworks to maximize fund efficiency.
Data Analytics Case Study: FY2023 Federal Budget Utilization Analysis
Author: Madrid J. Gregory
Tools Used: Microsoft Excel, Tableau
________________________________________
1. ASK Phase (The Business Task)
•	Core Goal: To analyze the spending efficiency and resource allocation of federal entities at the close of Fiscal Year 2023 (Q4).
•	Objective: Identify specific spending gaps across agencies—focusing on utilization anomalies—and propose data-driven solutions to optimize fund distribution before the critical September 30th fiscal deadline.
•	Key Stakeholder Question: Which sectors are failing to fully utilize their authorized budget authority, what are the primary operational bottlenecks causing these lags, and how can we ensure a target utilization rate of 100%?
________________________________________
2. PREPARE Phase (Data Sourcing & Integrity)
•	Data Source: Sourced the public "US Federal Agencies Budget and Spending Data" via Kaggle.
•	Data Size & Structure: The dataset consists of 108 records tracking active federal agencies for Fiscal Year 2023, Quarter 4.
•	Key Variables: agency_name, outlay_amount (actual spending), obligated_amount (committed funds), and budget_authority_amount (total authorized budget).
•	Data Integrity: The data features zero duplicate rows or missing critical financial records, maintaining a high level of credibility and verification for audit purposes.
________________________________________
3. PROCESS Phase (Data Cleaning & Formatting)
Because the dataset represented trillions of dollars in total government funding, Excel automatically compressed the grand total summaries into complex scientific notation formats (e.g., 1.36153E+13 for total budget authority and microscopic decimals like 8.41622e-07 for individual agency percentage shares).
To ensure the data was readable, accurate, and optimized for visualization, the following cleaning and data enrichment steps were performed in Microsoft Excel:
1.	Metric Engineering (Utilization Rate): Created a custom calculated column to isolate agency spending efficiency by dividing the actual spending by the authorized budget:
Excel Formula:
= [outlay_amount] / [budget_authority_amount]
2.	Error & Exception Handling: Anticipated logical system breaks. For inactive accounts or agencies with a budget_authority_amount of $0, standard division would throw a #DIV/0! error. These anomalies were cleaned and standardized to a clean numeric value of 0.0 (0%), preventing broken data fields upon export.
3.	Data Type Validation: Verified all core financial columns were explicitly cast as currency/numeric data types with standard decimal precision to avoid aggregation errors in the visualization phase.
4.	Sorting & Prioritization: Sorted the final worksheet by the newly engineered Utilization Rate in descending order. This immediately pushed critical spending anomalies to the top and severe utilization lags (0%) to the bottom, optimizing the file structure for visual analysis.
________________________________________
4. ANALYZE Phase (Data Insights)
By analyzing the calculated utilization metrics, deep operational insights and significant regional spending variances were discovered:
•	Spending Overages: Highly active sectors like the Federal Communications Commission ($127.7%) and the Department of Education ($104.9%) exceeded their baseline budget authorities, requiring resource shifts. (Not utilized as “important” in this dataset due to focus being on District Courts only, but is worth mentioning for comparative purposes)
•	Significant Spending Gaps: Across multiple sectors, including specific District Courts, utilization rates plummeted to ranges between 32% and 65%.
•	Root Cause Analysis: Applying domain logic to the numbers reveals that these severe end-of-year funding surpluses are likely driven by hiring lags/vacancies and deferred operational projects that failed to execute before the close of Q4.
________________________________________
5. SHARE Phase (Data Visualization)
To translate these tabular rows into a narrative stakeholders could act on, the cleaned dataset was imported into Tableau to build an interactive executive dashboard.
•	Dashboard Focus: The visualizations distinctly highlight the stark contrast between optimized agencies and those suffering from critical spending bottlenecks.
•	Project Link (Linkedin): https://www.linkedin.com/in/madrid-gregory-8b8800358/overlay/1775149900226/single-media-viewer/?profileId=ACoAAFkbpQwBrSi9kgo1HnUc0vdeSg6ptdIRHdU
________________________________________
6. ACT Phase (Actionable Recommendations)
To solve the spending gaps and drive the organization toward a 100% utilization rate by the September 30th end-of-fiscal-year deadline, the following three strategic actions are recommended:
1.	Establish Proactive Quarterly Audits: Move away from retroactive end-of-year reviews. Implement standardized quarterly internal budget evaluations to catch spending lags in Q1, Q2, and Q3 before they accumulate.
2.	Dynamic Fund Reallocation Framework: Create an administrative process to dynamically sweep and reallocate projected surplus funds from agencies experiencing hiring delays, redirecting those dollars to over-utilized, high-performing sectors before the fiscal clock runs out.
3.	Project Milestone Tracking: Tie budget authority to rigid operational project timelines, ensuring that if a project is deferred, the unspent funds are flagged immediately for organizational reuse rather than sitting idle.

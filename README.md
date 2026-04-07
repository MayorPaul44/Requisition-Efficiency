# **Requisition Operational Efficiency (Descriptive Data Analysis using MS Excel)**
## Project Description
This is a Descriptive Data Analysis project, using Microsoft Excel to analyze the internal requisition-to-delivery process for a large private university in West Africa. The procurement unit processes an average of 500 requests monthly across academic and administrative departments.
Using Excel connected directly to the organization’s MySQL database, I extracted raw requisition data, cleaned it with Power Query, transformed it using dynamic array functions, and built an interactive dashboard to visualize bottlenecks, cycle times, and departmental patterns.
All data has been fully anonymized to protect confidential information while preserving the analytical structure and business logic.

## Project Objective
To identify inefficiencies in the requisition approval process and provide actionable recommendations that can reduce processing time, improve compliance, and help the procurement unit manage high-volume periods more effectively.

## Questions (KPIs)
Requisition Volume: How many requisitions are submitted monthly? Which departments submit the most?
1. Cycle Time: What is the average time from submission to delivery? How does it vary by department or item category?
2. Approval Period: What is the average time for requisition to be approved by each department and for further action by the procurement unit?
3. Turnaround Time: What is the average time for requisition to be fulfilled and marked completed?
4. Fulfilment: What percentage of requisitions are fulfilled vs. pending per department?
5. Seasonal Trends: Are there peak periods (e.g., start of academic year) that overwhelm the system?

## Dataset & Interactive Dashboard
<a href="https://github.com/MayorPaul44/Requisition-Efficiency/blob/main/Proc.%20Funnel%20Analysis%20Data.xlsb">Dashboard & Dataset</a>

## Process
### Step 1: Data Extraction
1. Connected Excel to the company’s MySQL database using native database connectors.
2. Extracted raw requisition logs covering a 6-month anonymized period (the period under review).

### Step 2: Data Cleaning & Transformation (Power Query)
3. Removed duplicate entries.
4. Filtered out test, canceled, and rejected requisitions.
5. Standardized date formats and department names.
6. Handled null values in approval timestamps.

### Step 3: Anonymization
7. Removed employee names.
8. Recoded email addresses with random initials and changed domain.
9. Renamed requisition items generically (e.g., "Item 1", "Item 2", etc.)
10. Deleted all free-text comments.

### Step 4: Working Table 
11. Used Excel dynamic array function, FILTER(), to create a clean working table.
12. Added needed and useful calculated columns, which included Approval Period, Turnaround Period (Processing Time), Pending Request Period, etc.

### Step 5: Summarization (Pivot Tables)
13. Created pivot tables to aggregate by department, month, category, and approval stage.
14. Calculated approval rates, average cycle times, and volume distributions.

### Step 6: Visualization & Dashboard
15. Built a dashboard with:
Pie chart (requisition fulfilment summary)
Funnel chart (fulfilment lead days)
Column & Bar charts (requisition volumes & completion rates)
All charts linked dynamically to pivot tables.

## Dashboard Image
![Proc  Funnel Analysis](https://github.com/user-attachments/assets/1af268f4-67d0-46fb-a0e2-960d737111b5)

## Insights:
1. Volume concentration: Three non-academic departments account for nearly 70% of all requisitions.
2. Requisition volume & Cycle time: The average requisition volume per month (for the period under review) is 470, while average turnaround for period under review took 17.6 days.
3. Anomalies & Outliers: 
- January 2026 had the highest average turnaround period (24 days) despite having a relatively low requisition volume (227), which is just about half of the average monthly volume.
- Requisition volume was highest in in September (being the start of a new financial year), followed closely by October (when a new academic session kicks off).

## Conclusion
The current requisition process is functionally sound, but with further analysis (like diagnostic analysis), further insights could be uncovered (like the imminent bottlenecks indicated by the unusually high average fulfilment days in January)

## Tools & Techniques Used
1. Excel Power Query: Data extraction & cleaning
2. Excel Dynamic Arrays & Functions (FILTER, XLOOKUP, IF, TEXT, etc.): Working table creation
3. Excel Pivot Tables: Aggregation & summarization
4. Excel Charts: Visualization
5. MySQL: Source database
6. GitHub: Portfolio hosting

## Confidentiality Note:
All data in this project has been fully anonymized. No real employee names, emails, vendor details, financial figures, or internal comments appear in any file. The structure and patterns reflect real business logic, but specific values have been modified to protect confidentiality.


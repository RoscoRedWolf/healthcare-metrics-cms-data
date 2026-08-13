📊 CMS Healthcare Quality Measures - Executive Summary Dashboard
📌 Project Overview
This project processes and visualizes federal healthcare quality data from the Centers for Medicare & Medicaid Services (CMS) (specifically the Medicaid & CHIP Child and Adult Core Sets).

The goal was to transform raw, multi-state clinical quality metrics into an interactive, single-page Executive Summary Dashboard in Power BI. The resulting deliverable allows decision-makers to evaluate state-level performance across key healthcare domains within seconds.

🛠️ Data Cleaning & ETL Process (Power Query)
Raw public health datasets often contain structural errors, non-numeric placeholders, and duplicate entries that break aggregations in Business Intelligence tools. Using Power Query, I performed the following data transformations:

Handling Non-Numeric Values for Aggregation:

Challenge: Several numeric fields in the State Rate column contained string text, nulls, or special placeholder codes (e.g., "NR" for Not Reported, "Suppressed", or text symbols), which prevented Power BI from recognizing the column as a decimal/percentage and calculating mathematical averages.

Solution: Executed value replacement operations in Power Query to standardise missing values, stripped non-numeric strings, and cast the State Rate column to a Decimal Number type. This enabled accurate summary statistics and DAX calculations.

Deduplication & Data Hygiene:

Audited the dataset for true duplicate rows and removed redundant records to prevent inflated measure counts.

Column Cleanup & Domain Categorization:

Filtered out unnecessary administrative columns, ensuring clean, optimized data loads into the Power BI data model.

🎨 Dashboard Design & Visual Architecture
The report canvas was specifically engineered following Executive Summary design principles—focusing on clarity, scannability, and immediate visual hierarchy:

Top-Level KPI Banner:

Positioned high-impact Card visuals at the very top left (National Avg Rate, Total Measures Tracked) so stakeholders immediately grasp macro performance before diving into specific states.

Comparative Visual Analytics:

Utilized a Clustered Bar Chart to rank performance across reporting states, making outliers and high/low-performing regions immediately obvious.

Interactive Control & Context:

Integrated dedicated Slicers (Domain, Reporting Program) in the header area, allowing users to filter the entire page dynamically without cluttering the main visual layout.

Detailed Breakdown Table:

Included a clean, structured detail table alongside the primary chart, giving users granular access to underlying measure names and specific state rates when needed.

🧰 Tools & Technologies
Business Intelligence: Power BI Desktop

Data Transformation: Power Query (ETL)

Data Source: Centers for Medicare & Medicaid Services (CMS) Public Healthcare Quality Datasets

🚀 How to View
Power BI File: Clone this repository and open Healthcare_Quality_Executive_Summary.pbix directly in Power BI Desktop.

Static Snapshot: Check the ScreenShots/ directory for high-resolution images of the interactive report layout.

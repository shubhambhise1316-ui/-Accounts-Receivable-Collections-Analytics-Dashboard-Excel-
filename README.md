# -Accounts-Receivable-Collections-Analytics-Dashboard-Excel-
An end-to-end Accounts Receivable (AR) &amp; Collections Analytics Dashboard built in Microsoft Excel. 

📌 Project Overview

An end-to-end Accounts Receivable (AR) & Collections Analytics Dashboard built in Microsoft Excel. This project transforms raw, uncleaned invoice records into an executive-ready reporting system designed to monitor cash flow, identify overdue bottlenecks, evaluate regional credit risk, and track salesperson collection performance.

🎯 Business Objectives

1. Monitor Cash Flow Health: Track total invoiced revenue, collected payments, outstanding balances, and overall collection efficiency.
2. Identify Aging Bottlenecks: Categorize unpaid invoices into aging buckets (Current, 1–30 Days, 31–60 Days, 61–90 Days, 90+ Days) to prioritize collections.
3. Assess Regional & Account Risk: Pinpoint high-risk regions, customers nearing credit limits, and sales territories requiring follow-up support.
4. Analyze Monthly Trends: Compare monthly billing volume against collection percentages to detect seasonal payment delays.

🧹 Data Cleaning & Preparation

Before building the analytical model, the raw dataset (25 enterprise invoices across 7 major clients) underwent structured cleaning:
• Resolved Corrupted Entries: Identified and corrected a text anomaly ("nT") in Collected_Amount_INR for cleared invoice INV-2026-1010 (₹18,752.07), ensuring accurate collection totals.
• Standardized Text Fields: Applied TRIM() and PROPER() functions to remove trailing spaces ("Ram ", "Patil ") and unify inconsistent casing ("ISHAN", "kumar", "KIRAN") in the Sales_Person column to prevent duplicate groupings.
• Date & Aging Logic: Verified standard 30-day payment terms (Due_Date - Invoice_Date) and structured dynamic aging buckets based on overdue days.

🏗️ Workbook Architecture

The Excel workbook (Accounts_Receivable_Dashboard.xlsx) is organized into three modular sheets:
1. Data: Cleaned master invoice table with standardized fields and automated term calculations.
2. Analysis: Dynamic summary tables powered by SUMIF, COUNTIF, and INDEX/MATCH formulas breaking down performance by Region, Aging Bucket, Salesperson, Month, and Customer Credit Utilization.
3. Dashboard: Executive visual layer featuring 5 top-line KPI cards, 4 analytical charts, and interactive Slicers (Region, Aging_Bucket, Customer_Name).

💡 Key Analytical Insights

• Portfolio Snapshot: Out of ₹32,22,683.74 total invoiced, ₹17,94,672.90 has been collected (55.7% collection efficiency), leaving ₹14,46,762.91 in outstanding receivables.
• Regional Concentration: The South region holds the highest outstanding balance at ₹6,21,895.63 (43.0% of total AR), followed by North (₹3,43,953.72), West (₹2,82,693.15), and East (₹1,98,220.41).
• Primary Overdue Bottleneck: The 31–60 Days bucket accounts for the largest overdue share (₹5,38,714.52), indicating a critical window for proactive payment reminders before invoices escalate to 61–90+ days.
• Salesperson Exposure: Ishan carries the highest open receivable balance (₹3,39,973.12), followed by Ram (₹2,42,928.82), whereas Avinash, Vishali, and Yogesh maintain ₹0 outstanding balances.
• Monthly Collection Lag: August recorded the highest billing volume (₹12,27,487.60) alongside the lowest collection rate (44.2%).

🛠️ Tools & Excel Techniques Used

• Microsoft Excel (Pivot Tables, Pivot Charts, Interactive Slicers)
• Data Cleaning Functions: TRIM, PROPER, Data Validation
• Dynamic Lookup & Aggregation Formulas: SUMIF, COUNTIF, INDEX, MATCH
• Dashboard Design: KPI Cards, Combo Charts (Column + Line), Donut Charts, Conditional Formatting

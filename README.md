# CodeAlpha_FinancialHealthDashboard-Final-I understand. To make this a truly elite GitHub README, we need to move beyond descriptions and provide the Technical Blueprints. This version includes the exact DAX formulas used to solve the "flat-line" and "summarization" issues, plus a visual-by-visual breakdown of every chart you created.

# 📊 Advanced Financial Intelligence & Stability Dashboard
# A Professional Power BI Framework for SME Fiscal Analysis
# 📌 Project Overview
This project transforms static financial statements into a dynamic, three-page analytical engine. It was engineered to solve the "Data Aggregation Trap" common in Power BI—where historical trends often collapse into single data points—by implementing context-aware DAX measures and custom visual configurations.

## 🧠 The DAX Measurement Layer
To ensure the dashboard remains accurate across multiple years and companies, the following custom measures were developed. These formulas are the "brain" of the dashboard, allowing for real-time recalculations.

# 1. Performance & Efficiency Measures
Total Revenue & Net Income: Established as the primary KPIs to track top-line growth and bottom-line profit.

## Dynamic Profit Margin %: Profit Margin % = DIVIDE(SUM([Net Income]), SUM([Revenue]), 0) This formula handles zero-division errors and was formatted as a percentage to reveal shifts from 9% to 22%.

# 2. Liquidity & Stability Measures
Corrected Current Ratio: Current Ratio = DIVIDE(SUM([Total Current Assets]), SUM([Total Current Liabilities])) Used in the Gauge visual to track the health score of 2.04.

## Yearly ROE (Table-Specific): Table Yearly ROE = SELECTEDVALUE('Financial Statements'[ROE]) This measure was critical in forcing the Stability Table to show individual yearly data (e.g., 11.66%) instead of a single total.

## Debt-to-Equity Ratio: D/E Ratio = AVERAGE('Financial Statements'[Debt/Equity Ratio]) Calculates the leverage of 1.21, allowing for risk assessment against industry peers.

🎨 Visual-by-Visual Configuration
Every chart in this dashboard was meticulously tuned to provide a specific financial insight.

# Page 1: 
Revenue vs. Net Income (Line & Stacked Column):

Goal: Compare volume (Revenue) vs. Efficiency (Profit).

Key Fix: Enabled a Secondary Y-Axis for Net Income. This prevents the profit line from appearing "flat" against the $12M revenue scale.

Liquidity Gauge:

Goal: Visual health check of short-term solvency.

Config: Set to a range of 0–4.0, with the needle pointing to 2.04.

Market Cap Treemap:

Goal: Peer comparison and market positioning.

Function: Categorizes major competitors (AAPL, MSFT, GOOG) by size to provide sector context.

# Page 2: 
## Detailed Stability Table:

Goal: Provide the "raw truth" of the balance sheet.

Config: Set Year to "Don't Summarize" to expand the table into 14 rows (2009–2022).

## Shareholder Equity Trend (Area Chart):

Goal: Track the net worth growth of the business.

Key Fix: Set X-Axis to Categorical to break the "Flat Line" error and show actual yearly movement.

## Cash Flow Bridge (Stacked Bar):

Goal: Visualize the source and use of funds.

Segmentation: Breaks down cash into Operating, Investing, and Financing categories.

# 🛠️ Technical Problem-Solving 
The Flat-Line Resolution: Solved the issue where financial trends appeared as horizontal lines by reconfiguring the axis type and disabling auto-summarization in the Visualizations pane.

The "Zero-Label" Fix: Addressed the error where profit margins appeared as "0" by applying Global Percentage Formatting and adjusting decimal precision in the Measure Tools tab.

Context Filtering: Implemented slicers for Company and Year that interact across all three pages, allowing for deep-dive analysis into specific economic cycles.

# 📈 Executive Insights Summary
Efficiency: Profitability margins expanded significantly, peaking at 22%.

Solvency: A Current Ratio of 2.04 indicates high liquidity and low short-term risk.

ROI: Average ROE of 11.66% demonstrates effective management of shareholder capital.

# Financial Analysis Dashboard — Customers & Cost Centers (Excel)

## Overview

This project analyzes customer credit risk, cost estimation accuracy,
and revenue impact from returns across the company's customer segments
and cost centers from 2021–2024.

The goal is to move beyond surface-level metrics and uncover
the underlying patterns that drive — or threaten — cash flow stability,
operational efficiency, and net revenue health.

---

## Business Questions

**1. Customer Credit Risk & Outstanding Balance Concentration**:

Which customer segment holds the largest share
of outstanding balance, and does it reflect
a credit risk?

**2. Cost Estimation Accuracy & Budget Variance**:

Is the company accurately estimating its costs,
or is there a consistent gap between
Budget and Actual spending?

**3. Revenue Impact from Product Returns**:

What is the impact of returns on the company's
net revenue, and do they represent a significant
financial risk?



## 1. Customer Credit Risk & Outstanding Balance Concentration

**Business Question:**
Which customer segment holds the largest share
of outstanding balance, and does it reflect
a credit risk?

**Analysis Approach:**
- Calculate total Outstanding Balance per Segment
- Compare against Credit Limit to get utilization rate
- Identify highest concentration segment

**📊 Visualization:**

![Credit Risk by Segment](/images/Q1-outstanding%20balance.png)
![Credit Risk by Segment](/images/Q1-Credit%20Limit.png)

**📊 Key Findings:**
- Retail holds 40% of total outstanding (866M)
- SME holds 35% — Retail + SME = 75% of total debt
- Credit utilization ~40% across all segments — no segment exceeding its limit

**💡 Business Insights:**
- Retail & SME concentration is expected given customer volume
- 75% debt in lowest-creditworthy segments signals Concentration Risk
- Credit policy review recommended for Retail & SME segments

---

### 2. Cost Estimation Accuracy & Budget Variance

**Business Question:**
Is the company accurately estimating its costs,
or is there a consistent gap between
Budget and Actual spending?

**Analysis Approach:**
- Calculate Budget Variance per year (Budget - Cost)
- Track variance trend across 2021–2024
- Identify if over-budgeting is consistent pattern

**📊 Visualization:**

![Cost Amount And Budget Amount](/images/Q2-cost-budget%20amount.png)

**📊 Key Findings:**
- Cost Amount stable ~44M across all years
- Budget Amount increasing yearly (44M → 51M)
- Budget Variance growing each year — company consistently under-spending

**💡 Business Insights:**
- Consistent over-budgeting suggests poor cost estimation
- Excess reserved budget could be redirected to growth investments
- Recommend revising budgeting methodology to align with actual spending patterns

---

### 3. Revenue Impact from Product Returns

**Business Question:**
What is the impact of returns on the company's
net revenue, and do they represent a significant
financial risk?

**Analysis Approach:**
- Break down Revenue by Transaction Type (Sale / Return / Adjustment)
- Calculate return rate as % of total transactions
- Calculate Net Revenue after deducting returns

**📊 Visualization:**

![Returns Percentage](/images/Q3-Returns%20PCT.png)

**📊 Key Findings:**
- Returns represent 10% of total revenue (503M out of 5B)
- Sales represent 85% — Adjustments 5%
- Net Revenue after returns = 3,757,607,935

**💡 Business Insights:**
- 10% return rate is a red flag — industry benchmark is 5% or less
- High returns suggest product quality or customer expectation issues
- Reducing returns by 5% could recover ~250M in lost revenue

---

## Strategic Recommendations

1. **Strengthen credit controls for Retail & SME segments**
   
   With 75% of outstanding debt concentrated in the lowest-creditworthy segments,
   implement stricter credit policies, require personal guarantees,
   or reduce credit limits to mitigate concentration risk.

2. **Improve cost budgeting accuracy**
   
   The growing variance between budget and actual costs indicates
   ineffective planning. Implement zero-based budgeting or
   rolling forecasts tied to actual departmental spending patterns.

3. **Launch product quality initiative to reduce returns**
   
   A 10% return rate is unsustainable. Investigate root causes
   through customer feedback and product testing, then implement
   corrective actions to bring returns down to industry standard (≤5%).

## Technical Details

- **Database:** CSV Files (Customers, Transactions, Cost Centers)
- **Analysis Tools:** Excel, Power Query, Power Pivot
- **Data Cleaning:** [Data Cleaning Summary](/PROJECT%201/data_cleaning.md)

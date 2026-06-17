## 🧹 Data Cleaning
## Cost Centers
### Cost Amount — Negative Values
- **Issue:** 150 rows with negative values (1.25% of data)
- **Fix:** Converted to ABS() — costs can't be negative by definition
### Currency
- 80% EGP / 20% USD & EUR
- Analysis scoped to EGP transactions only
- Multi-currency conversion excluded due to
  exchange rate volatility (2021–2024)

- **Issue:** Mixed currencies (EGP/USD/EUR) + 4% null values
- **Fix:** Retained EGP transactions only — null replaced with "EGP"


## Transactions
### Revenue — Null Values
- **Issue:** 2,000 null values (0.4% of data)
- **Fix:** Removed via Power Query filter — excluded from all calculations
### Discount_Pct — Format Correction
- **Issue:** Discount stored as whole number (e.g. 20 instead of 0.20)
- **Fix:** Divided by 100 → formatted as Percentage
- **Why:** Ensures correct calculation in all discount-related formulas

### City — Inconsistent Names
- **Issue:** Same city stored in multiple formats (Cairo, CAIRO, cairo, Alex)
- **Fix:** Standardized via Replace Values in Power Query

### Date — Null Values
- **Issue:** Null values (< 1% of data)
- **Fix:** Removed via Power Query filter — too few to impact analysis

## Customers

### Account_Status — Null Values
- **Issue:** Null values (< 4% of data)
- **Fix:** Removed via Power Query filter — too few to impact analysis


 
## Change Type — Numeric Columns
- **Issue:** Columns stored as Text instead of numeric in Customers and Transactions
- **Fix:** Changed to correct data types

| Column | Type |
|--------|------|
| Unit_Price | Currency |
| Revenue | Currency |
| COGS | Currency |
| Gross_Profit | Currency |
| Tax_Amount | Currency |
| Credit_Limit | Currency |
| Outstanding_Balance | Currency |
| Annual_Revenue_EGP | Currency |
| Payment_Terms_Days | Whole Number |
| Registration_Date | Date |
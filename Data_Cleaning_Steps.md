#  Data Cleaning Steps

This document outlines the ETL process applied to the raw sales data in Excel.

## ✅ Steps Performed

1. **Removed Duplicates**
   - Checked for duplicate `Order ID` entries and removed them using Excel's "Remove Duplicates" feature.

2. **Handled Commission Formatting**
   - Converted scientific notation (e.g., `7.0000000000000007E-2`) to decimal format using Excel formulas.

3. **Added Primary Keys**
   - Verified `Order ID` as a unique identifier for each transaction.

4. **Created Calculated Columns**
   - **Commission Amount** = `Total Sales × Commission Rate`
   - **Profit Flag** = IF `Commission Rate > 0.05`, then "High Margin", else "Low Margin"
   - **Sales Category** = Based on `Total Sales` thresholds (e.g., <1000 = "Low", >3000 = "High")

5. **Standardized Date Format**
   - Ensured all dates were in `MM/DD/YYYY` format using Excel's formatting tools.

6. **Validated State and Sales Rep Entries**
   - Used Data Validation to ensure consistent spelling and prevent typos.

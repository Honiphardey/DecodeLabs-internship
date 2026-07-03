# Product Sales Data Cleaning

## Project Overview
This project documents the data cleaning process performed on a retail 
sales dataset containing 2,000 orders across multiple regions, products, 
and salespersons. The goal was to prepare the dataset for exploratory 
data analysis and visualization.

---

## Dataset Overview
| Field | Details |
|---|---|
| Source | Retail Sales Dataset |
| Total Records | 2,000 orders |
| Total Columns | 19 columns |
| Time Period | January — December |

---

## Columns in Dataset
`date`, `region`, `product`, `quantity`, `unit price`, `store location`,
`customer type`, `discount`, `salesperson`, `total price`,
`payment method`, `promotion`, `returned`, `orderID`, `customer name`,
`shipping cost`, `order date`, `delivery date`, `region manager`

---

## Cleaning Steps Performed

### 1. Data Type Formatting
- Converted `date`, `order date`, `delivery date` to proper Date format
- Converted `quantity`, `unit price`, `total price`, `shipping cost`, 
  `discount` to numerical format
- Ensured `returned` and `promotion` columns were stored as Text

### 2. Handling Missing Values
- `promotion` column contained blank values indicating no active 
  promotion — blanks retained intentionally as "No Promotion"
- No missing values found in critical columns (orderID, total price, 
  region, product)

### 3. Duplicate Check
- Checked for duplicate orderIDs across 2,000 records
- No duplicate records found

### 4. Calculated Columns Added
- `Delivery Days` — calculated as difference between `delivery date` 
  and `order date`
- `Delivery Bucket` — grouped delivery days into ranges:
  - 1–3 Days, 4–7 Days, 8–14 Days, 15+ Days
- `Is Returned` — converted `returned` column to binary (1 = Yes, 0 = No)

### 5. Consistency Checks
- Verified all regions matched expected values (North, East, West, 
  Central, South)
- Verified product names were consistent across all records
- Confirmed salesperson names had no spelling inconsistencies

---

## Tools Used
- Microsoft Excel (Power Query)
- Microsoft Power BI (Power Query Editor)

---

## Output
Clean dataset ready for exploratory data analysis and Power BI 
dashboard visualization.

---

---

## Author
**Onifade Oluwagbemiga**
Data Analytics Intern — DecodeLabs

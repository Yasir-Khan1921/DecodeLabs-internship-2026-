# 📊 DecodeLabs Data Analytics Internship — Project 1
## Data Cleaning and Preparation

---

### 🎯 Objective
Perform comprehensive data cleaning and preparation on a real-world e-commerce orders dataset to ensure data quality, consistency, and readiness for downstream analysis. This project demonstrates essential data wrangling skills including handling missing values, removing duplicates, correcting data formats, and validating data integrity.

---

### 📁 Dataset Description

| Property | Details |
|----------|--------|
| **File Name** | `Dataset for Data Analytics.xlsx` |
| **Records** | 1,200 orders |
| **Features** | 14 columns |
| **Source** | E-commerce orders data |
| **Date Range** | January 2023 – June 2025 |

#### Columns:
| # | Column | Type | Description |
|---|--------|------|-------------|
| 1 | OrderID | String | Unique order identifier |
| 2 | Date | DateTime | Order date |
| 3 | CustomerID | String | Customer identifier |
| 4 | Product | String | Product name (Monitor, Phone, Tablet, Chair, Printer, Laptop, Desk) |
| 5 | Quantity | Integer | Items ordered |
| 6 | UnitPrice | Float | Price per unit |
| 7 | ShippingAddress | String | Delivery address |
| 8 | PaymentMethod | String | Payment type (Debit Card, Online, Credit Card, Gift Card, Cash) |
| 9 | OrderStatus | String | Order status (Shipped, Cancelled, Returned, Delivered, Pending) |
| 10 | TrackingNumber | String | Shipment tracking ID |
| 11 | ItemsInCart | Integer | Total items in customer's cart |
| 12 | CouponCode | String | Discount coupon applied (SAVE10, FREESHIP, WINTER15) |
| 13 | ReferralSource | String | How the customer found the store |
| 14 | TotalPrice | Float | Total order value |

---

### 📋 Steps Performed

1. **Import Libraries** — Loaded Pandas, NumPy, and configured the environment.
2. **Load Dataset** — Read the Excel file into a Pandas DataFrame.
3. **Initial Exploration** — Displayed first 5 rows, `.info()`, `.describe()`, and column details.
4. **Missing Value Identification** — Used `isnull().sum()` to detect 309 missing values in `CouponCode`.
5. **Missing Value Handling** — Filled `CouponCode` nulls using **Mode** (most frequent value), appropriate for categorical data.
6. **Duplicate Detection** — Used `duplicated().sum()` — found 0 duplicates.
7. **Duplicate Removal** — Applied `drop_duplicates()` as a best-practice safeguard.
8. **Data Format Corrections:**
   - Converted `Date` column to `YYYY-MM-DD` string format.
   - Stripped leading/trailing whitespace from all text columns.
   - Standardized text capitalization to Title Case.
   - Verified numerical columns have correct `int64`/`float64` data types.
9. **Final Verification** — Confirmed:
   - ✅ Zero missing values
   - ✅ Zero duplicate rows
   - ✅ Dates in YYYY-MM-DD format
   - ✅ Correct data types
10. **Export** — Saved the cleaned dataset as `cleaned_dataset.csv`.

---

### 🛠️ Tools Used

| Tool | Purpose |
|------|--------|
| **Python 3** | Programming language |
| **Pandas** | Data loading, manipulation, cleaning |
| **NumPy** | Numerical operations and analysis |
| **Jupyter Notebook** | Interactive development and documentation |

---

### 📊 Results

| Metric | Before Cleaning | After Cleaning |
|--------|-----------------|----------------|
| Total Records | 1,200 | 1,200 |
| Missing Values | 309 | 0 |
| Duplicate Rows | 0 | 0 |
| Date Format | datetime64 | YYYY-MM-DD |
| Text Consistency | Mixed | Title Case |
| Data Types | Verified | Correct |

---

### 📝 Change Log

| Change ID | Description | Impact | Status |
|-----------|------------|--------|--------|
| CL-001 | Loaded dataset from Excel file | Established raw data baseline with 1,200 records | ✅ Completed |
| CL-002 | Identified 309 missing values in CouponCode | Revealed data quality gap in coupon tracking | ✅ Completed |
| CL-003 | Filled CouponCode nulls with Mode | Restored 309 records; no data loss | ✅ Completed |
| CL-004 | Checked for duplicate rows | Confirmed 0 duplicates | ✅ Completed |
| CL-005 | Executed drop_duplicates() | Deduplication pipeline in place | ✅ Completed |
| CL-006 | Converted Date to YYYY-MM-DD | Standardized date format | ✅ Completed |
| CL-007 | Stripped whitespace from text | Eliminated matching errors | ✅ Completed |
| CL-008 | Standardized text to Title Case | Consistent capitalization | ✅ Completed |
| CL-009 | Verified numerical data types | Confirmed correct types | ✅ Completed |
| CL-010 | Final verification passed | All quality checks passed | ✅ Completed |
| CL-011 | Saved cleaned_dataset.csv | Deliverable ready | ✅ Completed |

---

### 🎯 Conclusion

This project successfully demonstrates a professional, end-to-end data cleaning pipeline on a real-world e-commerce dataset. All 309 missing values were handled using statistically appropriate techniques (Mode for categorical data), data formats were standardized, and comprehensive validation confirmed the dataset is clean and analysis-ready.

The cleaned dataset (`cleaned_dataset.csv`) is ready for downstream analysis tasks including exploratory data analysis, visualization, and modeling.

---

### 📂 Project Files

| File | Description |
|------|-------------|
| `Data_Cleaning_and_Preparation.ipynb` | Main Jupyter Notebook with code, output, and documentation |
| `Dataset for Data Analytics.xlsx` | Original raw dataset |
| `cleaned_dataset.csv` | Final cleaned dataset |
| `README.md` | Project documentation |

---

*Submitted by: Yasir Khan | DecodeLabs Data Analytics Internship | June 2026*


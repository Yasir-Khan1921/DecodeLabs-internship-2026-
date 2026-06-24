#  DecodeLabs Data Analytics Internship — Project 2
## Exploratory Data Analysis (EDA)

---

###  Objective
Perform a complete Exploratory Data Analysis (EDA) on the cleaned e-commerce orders dataset to understand patterns, trends, distributions, outliers, and statistical relationships between variables. This project demonstrates essential data analysis skills including calculating descriptive statistics, evaluating distribution skewness, detecting outliers using the IQR method, analyzing correlation, and creating data visualizations to drive business insights.

---

###  Dataset Description

| Property | Details |
|----------|--------|
| **File Name** | `cleaned_dataset.csv` |
| **Records** | 1,200 orders |
| **Features** | 14 columns |
| **Source** | Cleaned e-commerce orders data from Project 1 |
| **Date Range** | January 2023 – June 2025 |

#### Columns Analyzed:
| Column | Type | Description |
|--------|------|-------------|
| **Quantity** | Integer | Number of units purchased in the order |
| **UnitPrice** | Float | Price per single unit of the product |
| **ItemsInCart** | Integer | Total items in the user's cart at checkout |
| **TotalPrice** | Float | Total value of the transaction (`Quantity` × `UnitPrice`) |

---

###  Steps Performed

1. **Introduction** — Defined EDA, project objectives, and described the business purpose of the dataset.
2. **Import Libraries** — Loaded `pandas`, `numpy`, `matplotlib.pyplot`, and `seaborn` with custom plotting themes.
3. **Load Dataset** — Loaded `cleaned_dataset.csv` and verified dimensions (1,200 × 14).
4. **Dataset Information** — Inspected data types, detailed column definitions, checked and verified zero duplicate rows.
5. **Missing Values Analysis** — Confirmed zero missing values across all columns.
6. **Descriptive Statistics** — Evaluated mean, median, standard deviation, and quartiles using `df.describe()`.
7. **Distribution Analysis** — Plled Histograms with KDE curves to evaluate skewness.
   - *Quantity*, *UnitPrice*, and *ItemsInCart* are symmetrical (skewness $\approx 0$).
   - *TotalPrice* is right-skewed (skewness $= 0.8914$).
8. **Outlier Detection** — Created Boxplots and calculated limits using the **IQR method**:
   - $\text{Lower Bound} = Q1 - 1.5 \times \text{IQR}$
   - $\text{Upper Bound} = Q3 + 1.5 \times \text{IQR}$
   - Identified **8 high-value outliers** in `TotalPrice` (orders exceeding \$3,330.41).
9. **Correlation Analysis** — Computed correlation matrix and created a Heatmap:
   - Found strong positive correlation between `Quantity` and `ItemsInCart` ($r = 0.6501$).
   - Confirmed no correlation between `Quantity` and `UnitPrice` ($r = 0.0146$).
10. **Relationship Analysis** — Plotted Scatter plots and a comprehensive Pairplot categorized by order fulfillment status.
11. **Key Findings & Recommendations** — Formulated actionable business strategies based on statistical results.

---

###  Tools Used

| Tool | Purpose |
|------|--------|
| **Python 3** | Programming language |
| **Pandas** | Tabular data manipulation and summary stats |
| **NumPy** | Array computations and mathematical skewness |
| **Matplotlib** | Custom visualization canvas layouts |
| **Seaborn** | Distribution plots, heatmaps, boxplots, and pairplots |
| **Jupyter Notebook** | Portfolio-ready interactive presentation |

---

###  Key Visualizations & Analysis

#### 1. Skewness Summary
- **Quantity**: $0.0279$ (Symmetrical)
- **UnitPrice**: $-0.0265$ (Symmetrical)
- **ItemsInCart**: $0.0009$ (Symmetrical)
- **TotalPrice**: $0.8914$ (Moderately Right-Skewed)

#### 2. Outlier Bounds (IQR Method)
- **TotalPrice limits**: Lower bound = -\$1341.41, Upper bound = \$3330.41.
- **Outliers count**: 8 transactions (0.67% of orders) ranging between \$3,334.00 and \$3,456.40. These represent large quantity orders of high-end Monitors and Laptops.

#### 3. Correlation Strengths
- **Quantity & ItemsInCart**: $0.6501$ (Strong positive correlation)
- **UnitPrice & TotalPrice**: $0.7171$ (Strong positive correlation)
- **Quantity & TotalPrice**: $0.6153$ (Strong positive correlation)
- **Quantity & UnitPrice**: $0.0146$ (No correlation)

---

###  Key Business Recommendations

1. **Leverage Bulk Purchase Discounts**: Since there is currently no correlation between UnitPrice and Quantity purchased ($r = 0.0146$), introduce tiered pricing (e.g. "Order 3+ items and get 15% discount") to encourage bulk purchases.
2. **Promotions based on Cart Sizes**: Given the strong correlation between Quantity of the primary item and the total items in the cart ($r = 0.6501$), implement cross-selling bundle recommendations in the checkout flow.
3. **VIP Loyalty Segments**: Target the customers behind the 8 high-value outliers with VIP loyalty bonuses to maximize customer retention and lifetime value.

---

###  Project Files

| File | Description |
|------|-------------|
| `Data_Analytics_EDA.ipynb` | Executed Jupyter Notebook with code, plots, and analysis |
| `cleaned_dataset.csv` | Input cleaned e-commerce dataset |
| `README_EDA.md` | Markdown documentation of the project |

---

*Submitted by: Yasir Khan | DecodeLabs Data Analytics Internship | June 2026*


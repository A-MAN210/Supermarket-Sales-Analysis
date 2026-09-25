# Supermarket Sales Analysis

## AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026 | BharatCares

### Project
**Supermarket Sales Analysis — Data Analytics Capstone Project**

## 1. Project Overview

This project analyses 500 supermarket sales transactions across four branches/cities: Jaipur, Delhi, Mumbai, and Bengaluru.

The project follows a reproducible analytics workflow:

**Data loading → Data-quality validation → Exploratory Data Analysis → Observations → Insights → Hypotheses → Recommendations**

The analysis examines:
- monthly revenue variation
- product performance
- branch performance
- category contribution
- payment-method usage
- Member vs. Normal customer transactions
- customer ratings
- the linear association between rating and transaction sales value

All numerical results were calculated from the supplied dataset with Python and cross-checked before being included in the report.

## 2. Project Objective

The objective is to convert raw supermarket transaction data into clear, evidence-based business insights that can support decisions about products, branches, categories, payments, customer types, and customer satisfaction.

## 3. Dataset

**Dataset file:** `SUPER MARKET DATA.xlsx`

**Source:** Google Sheet supplied in the internship/project brief; the submitted Excel workbook is the local export used for reproducible analysis.

The workbook contains:
- 500 transactions
- 13 columns
- 4 branches/cities
- 8 product categories
- 20 unique products
- 2 customer types: Member and Normal
- 4 payment methods: UPI, Card, Net Banking, Cash
- Date range: 1 January 2026 to 1 July 2026
- July is a partial month containing 7 transactions, all dated 1 July

### Expected Dataset Columns

`Invoice ID`, `Date`, `Branch`, `City`, `Customer Type`, `Gender`, `Product`, `Category`, `Quantity`, `Unit Price`, `Payment`, `Rating`, `Sales`

### Dataset Link

The supplied workbook is an Excel export of the project dataset. The original Google Sheets URL is not embedded in the workbook or in the submitted project files, so no URL is fabricated here. If the internship coordinator separately provides the original Google Sheets URL, it can be added to this section without changing the analysis.

## 4. Data Quality Validation

The notebook verifies:
- required columns are present
- missing values
- duplicate Invoice IDs
- invalid dates
- non-positive quantities
- invalid unit prices/sales
- ratings outside the 0–5 range
- `Sales = Quantity × Unit Price` to 2 decimal places
- partial calendar months

For the supplied dataset:
- Missing values: **0**
- Duplicate Invoice IDs: **0**
- Sales formula mismatches: **0**
- Invalid dates: **0**
- Quantities ≤ 0: **0**
- Unit prices < 0: **0**
- Sales < 0: **0**
- Ratings outside 0–5: **0**
- July 2026: **7 transactions**, all on 1 July, therefore excluded from complete-month comparisons

## 5. Main Findings

- Total sales: **₹244,411.08**
- Highest complete month: **April 2026 — ₹52,569.77**
- Lowest complete month: **February 2026 — ₹30,068.15**
- Highest-selling product: **Cheese — ₹27,906.30**
- Highest-selling branch: **Branch C, Mumbai — ₹72,469.45**
- Lowest-selling branch: **Branch A, Jaipur — ₹52,357.08**
- Highest-selling category: **Beverages — ₹56,108.24**
- Payment methods are closely distributed: UPI 127, Net Banking 126, Card 125, Cash 122
- Member transactions: 296 transactions and ₹143,009.30 revenue
- Normal transactions: 204 transactions and ₹101,401.78 revenue
- Overall average rating: **3.99 / 5**
- Rating–sales Pearson correlation: **−0.047**, indicating little linear association in this dataset; it does not prove independence or causation

## 6. Important Limitations

The dataset does not contain:
- customer IDs
- cost or profit/margin
- discounts
- inventory
- promotions
- staffing information
- store footfall

Therefore, the analysis cannot establish individual customer retention/lifetime value, profitability, or the causal reason for branch/category differences.

July is also a partial month, so it is excluded from month-to-month comparisons.

## 7. Technologies Used

- Python 3.10+
- Pandas
- Matplotlib
- OpenPyXL
- Jupyter Notebook / Google Colab

## 8. Responsible AI Use

AI was used as a supporting tool for brainstorming analytical questions, structuring the project, and refining hypothesis wording.

AI was **not treated as the source of truth for numerical results**. Calculations, validation checks, statistics, and charts were produced from the supplied dataset using Python.

Where the data cannot establish causation, the report explicitly labels explanations as hypotheses and identifies the additional evidence needed to test them.

## 9. How to Run

### Google Colab

1. Open `AmanKumawat_SupermarketSalesAnalysis.ipynb`.
2. Upload `SUPER MARKET DATA.xlsx` into the Colab session.
3. Install dependencies if necessary:

```bash
!pip install -r requirements.txt
```

4. Run all notebook cells from top to bottom.

### Local Jupyter

```bash
pip install -r requirements.txt
jupyter notebook
```

Place `SUPER MARKET DATA.xlsx` in the same working directory as the notebook and run all cells.

## 10. Submission Files

The Google Form requires four files:

| File | Purpose |
|---|---|
| `AmanKumawat_SupermarketSalesAnalysis.ipynb` | Complete executable analysis notebook |
| `requirements.txt` | Python dependencies |
| `AmanKumawat_SupermarketSalesAnalysis_ProjectReport.docx` | Complete project report |
| `README.md` | Project documentation and run instructions |

The dataset workbook is used by the notebook but is not one of the four upload fields shown in the form.

## 11. Final Submission Checklist

- [ ] `AmanKumawat_SupermarketSalesAnalysis.ipynb`
- [ ] `requirements.txt`
- [ ] `AmanKumawat_SupermarketSalesAnalysis_ProjectReport.docx`
- [ ] `README.md`
- [ ] `SUPER MARKET DATA.xlsx` kept available for notebook execution

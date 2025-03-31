
# Loan-Level Risk Segmentation for MBS Structuring

This project analyzes 2016 single-family conforming loan-level data from Fannie Mae and Freddie Mac. The goal is to understand borrower risk characteristics and simulate the creation of mortgage-backed securities (MBS) pools based on credit and collateral quality.

## ✅ Project Steps

### Step 1: Load & Inspect Data
- Loaded FNMA and FHLMC loan-level CSV files.
- Inspected column names, missing values, and data types.

### Step 2: Data Cleaning
- Renamed important columns (e.g., `Income`, `UPB`, `LoanPurpose`).
- Converted columns to numeric types and handled missing values.

### Step 3: Descriptive Statistics
- Explored borrower characteristics:
  - Avg income and loan size by purpose
  - First-time homebuyer distribution
  - Loan size by occupancy
  - Top origination states

### Step 4: Risk Bucketing
- Created borrower risk tiers based on:
  - Estimated FICO (via income ratio)
  - Estimated LTV (via UPB / income)
- Labeled loans into categories like:
  - `Prime / Low LTV`
  - `Near-Prime / Medium LTV`
  - `Subprime / High LTV`

### Step 5: Pool-Level Aggregation
- Aggregated loan-level metrics by RiskTier:
  - Avg FICO, LTV, UPB, Income
  - Total loan count and UPB
- Identified risk patterns useful for securitization

### Step 6: Synthetic MBS Pools
- Defined 4 hypothetical loan pools:
  - **Pool A**: Prime / Low LTV — ideal for AAA tranches
  - **Pool B**: Near-Prime / Medium LTV — solid mezzanine risk
  - **Pool C**: Subprime / High LTV — high risk, equity tranche
  - **Pool D**: Prime / High LTV — high credit, high leverage
- Summarized and compared pool characteristics

## 📈 Next Steps
- Visualize pool comparisons with bar charts
- Optionally apply the pipeline to Freddie Mac loans
- Expand to risk modeling or performance analysis with more data

---

Prepared for interview discussion and MBS structuring analysis.

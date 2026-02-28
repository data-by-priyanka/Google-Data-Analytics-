# Verification

**Verification** is the process of confirming that data cleaning was executed correctly and that the resulting dataset is accurate and reliable.

It involves:
- Comparing the cleaned dataset to the original raw dataset
- Identifying patterns in previous errors
- Performing manual spot checks
- Reviewing whether the data supports the business objective

Verification ensures that your cleaned data is credible and appropriate for analysis.

---

# Reporting After Cleaning

Reporting demonstrates:
- Accountability
- Transparency
- Trustworthiness
- Alignment with stakeholders

Common reporting strategies:
- Data-cleaning reports
- Documentation of cleaning steps
- Changelog tracking

---

# Changelog

A **changelog** is a file that records modifications made to a project in chronological order.

It typically includes:
- Version number
- Date
- Added changes
- Updated changes
- Removed elements

Changelogs help:
- Track how datasets evolved
- Revisit earlier versions
- Debug errors
- Communicate changes clearly

---

# Verification Process

## Step 1: Compare With Raw Data

- Review original dirty dataset
- Identify common data issues
- Confirm corrections were applied properly

---

## Step 2: Big-Picture Review

Take a problem-first approach:

1. What business problem are you solving?
2. What is the project goal?
3. Is the cleaned dataset capable of solving the problem?

Clean data is only useful if it aligns with business objectives.

---

# Useful Functions During Verification

## COUNTA vs COUNT (Spreadsheet)

- `COUNTA(range)` → Counts all non-empty values.
- `COUNT(range)` → Counts only numerical values.

---

## CASE Statement (SQL)

Used to correct inconsistencies such as misspellings.

```sql
SELECT
  CASE
    WHEN column_name = 'Jon' THEN 'John'
    ELSE column_name
  END AS corrected_name
FROM table_name;
```

`CASE` evaluates conditions and returns corrected values.

---

# Documentation

**Documentation** tracks:
- Changes
- Additions
- Deletions
- Corrections

Benefits:
- Recover from errors
- Inform team members
- Evaluate data quality
- Maintain transparency

---

# Version Tracking Tools

## In Spreadsheets

- Version History
- Show Edit History (cell-level tracking)

---

## In SQL (Example: BigQuery)

- Query History
- Ability to review or revert previous queries

---

# Why Documentation Matters

Documentation allows you to:

- Identify recurring data issues
- Improve data collection processes
- Update validation rules
- Refine quality control systems
- Collaborate better with data engineers or data owners

Sometimes cleaning reveals systemic issues that require changes upstream.

---

# Key Insight

Clean data is important.

But documenting *how* you cleaned it:
- Builds trust
- Improves reproducibility
- Strengthens team collaboration
- Enhances long-term data quality

Verification is not optional.  
It’s what separates analysis from guesswork.

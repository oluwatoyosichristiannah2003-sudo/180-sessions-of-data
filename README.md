# 180-Session Data Analysis Journey

Documenting 180 focused, 1-hour sessions building foundational to advanced data analytics skills from scratch.

### The Roadmap
* **Phase 1 (Sessions 1–45):** Spreadsheets, Data Hygiene & Validation (Excel)
* **Phase 2 (Sessions 46–95):** Relational Databases & Cohort Extraction (SQL)
* **Phase 3 (Sessions 96–150):** Data Wrangling & Applied Biostatistics (Python)
* **Phase 4 (Sessions 151–180):** Interactive Dashboards & Capstones (Power BI)

---

## Session Logs

### Phase 1: Spreadsheets & Data Hygiene (Excel)

* **Session 1: Grid Mechanics & Table Basics**
  * Cell formatting (`Ctrl + 1`), thousand separators, column autofit, and row/column navigation.
  * Column shifting and hiding/unhiding ranges.
  * Converted ranges into structured tables with dynamic Total Rows and conditional formatting.

* **Session 2: Freezing Panes & Multi-Level Sorting**
  * Built and expanded a 5-column clinic cohort dataset to 15 records.
  * Pinned header context using Freeze Panes (`View` → `Freeze Top Row`).
  * Executed multi-level sorting (`Department` A–Z, then `Age` descending).
  * Handled dynamic table aggregates (calculated mean cohort age: 42.87).

* **Session 3: Formula Syntax & Basic Aggregations**
  - Integrated a `Billing_Amount` numeric field into the cohort model.
  - Implemented core aggregation functions: `=SUM()`, `=AVERAGE()`, `=MIN()`, and `=MAX()`.
  - Built an isolated KPI summary table for clinical revenue metrics ($25,900 total revenue, $1,726.67 mean charge).

* **Session 4 (Sun, Sep 20, 2026): Data Auditing with Excel Counting Functions**
  - Evaluated data integrity using `=COUNT()`, `=COUNTA()`, and `=COUNTBLANK()` across clinical cohort records.
  - Implemented conditional logic using `=COUNTIF()` and `=COUNTIFS()` to isolate active inpatient records and department-level admissions.
  - Audited missing discharge dates to identify unclosed clinical stays.

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

* **Session 4: Data Auditing with Excel Counting Functions**
  - Evaluated data integrity using `=COUNT()`, `=COUNTA()`, and `=COUNTBLANK()` across clinical cohort records.
  - Implemented conditional logic using `=COUNTIF()` and `=COUNTIFS()` to isolate active inpatient records and department-level admissions.
  - Audited missing discharge dates to identify unclosed clinical stays.

* **Session 5 (Mon, Sep 21, 2026): Cell Referencing Mechanics (Relative vs Absolute)**
  - Mastered formula locking mechanics (`$`) toggled via `F4`.
  - Built a calculated `Tax_Due` column referencing a static master tax rate cell (`$H$1` = 7.5%).
  - Evaluated coordinate shift behavior: allowed relative row index movement (`F2` to `F16`) while pinning lookup anchors (`$H$1`).
  - Total cohort billing: $25,900.00 | Total tax generated: $1,942.50.

* **Session 6 (Tue, Sep 22, 2026): Proportions, Rates & Percentage Modeling**
  - Modeled Chandoo's 5 core percentage scenarios across a 15-patient clinical cohort:
    1. Proportion of Total: `=Part / $Total$` (verified grand sum = 100.00%).
    2. % Change / Variance: `=(Current - Previous) / Previous`.
    3. Target Attainment: `=Current / Target`.
    4. Rate Application (+5% Fee Adjustment): `=Current * (1 + $Rate$)`.
    5. Discount Reduction (-10% Insurance Adjustment): `=Current * (1 - $Rate$)`.
  - Applied absolute cell referencing (`$`) to lock static total and rate parameters across row operations.
  - Cohort baseline: $25,900.00 | Adjusted (+5%): $27,195.00 | Discounted (-10%): $23,310.00.
* **Session 7 (Wed, Sep 23, 2026): Systems Engineering – Dynamic Atomic Habit Tracker**
  - Engineered an interactive daily accountability dashboard modeled on James Clear's *Atomic Habits* principles.
  - Tracked 10 keystone systems across spiritual, physical, academic, and professional pillars with defined baseline floors[cite: 4].
  - Excel Mechanics Applied:
    - Form control checkboxes mapped to dynamic boolean evaluation cells (`TRUE`/`FALSE`)[cite: 4].
    - Aggregate check-in counts using `=COUNTIF()`[cite: 4].
    - Monthly completion rate modeling: `=TOTAL / Days` formatted as percentage attainment[cite: 4].
    - Summary KPI cards tracking active habits against an 85% target threshold[cite: 4].
  - Deliverable: `atomic-habit-systems-tracker.xlsx`

* **Session 8 (Thu, Sep 24, 2026): Logical Conditions & The IF Function**
  - Focused on single-condition boolean evaluation: `=IF(logical_test, value_if_true, value_if_false)`.
  - Tested comparative evaluation rules (`>=`, `<`, `<>`) to classify patient demographics without manual sorting.
  - Implemented categorical segmentation: `=IF(C2>=65, "Senior", "Adult")`.
  - Audited boundary values (Age 64 vs 65) via `=COUNTIF()`: 7 Seniors, 8 Adults across 15 cohort records.
  - Deliverable: `Session-08-Logical-IF-Function.xlsx`
 
  - * **Session 9 (Fri, Sep 25, 2026): Multi-Tier Branching (=IFS & Nested IF)**
  - Explored sequential boolean logic evaluation across multi-category clinical thresholds.
  - Contrasted legacy Nested `IF` syntax against modern `=IFS()` linear pair evaluation.
  - Implemented directional sequencing (lowest-to-highest) to categorize patient `Systolic_BP`:
    `=IFS(D2<120, "Normal", D2<=129, "Elevated", D2>=130, "High")`
  - Evaluated boundary evaluation order to eliminate overlapping range bugs: prevented early false-positive triggers by testing `<120` prior to `<=129`.
  - Audited 15-patient cohort distributions via `=COUNTIF()`: 4 Normal, 5 Elevated, 6 High.
  - Deliverable: `Session-09-Multi-Tier-IFS.xlsx`

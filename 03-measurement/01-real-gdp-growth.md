# Indicator 1 — Real GDP Growth

**Status:** Draft specification; not yet approved for classification.

## Concept and purpose
Measure the change in the volume of economic output after accounting for changes in prices.

## Operational definition
Real GDP growth is the percentage change in Nigeria's inflation-adjusted GDP between two specified periods, using the latest available official national-accounts series. Record the comparison period, data source, publication date, data vintage, methodology, and revision status.

Initial monitoring measures:
- Annual real GDP growth, comparing annual real GDP with the previous year.
- Quarterly year-on-year real GDP growth, comparing a quarter with the same quarter in the previous year.
- Quarter-on-quarter growth may be considered later, but must be clearly distinguished from seasonally adjusted and annualized growth.

## Formula
For comparable real GDP values in periods t and t-1:

`Growth (%) = (Real GDP_t / Real GDP_(t-1) - 1) × 100`

The comparison period must be explicit.

**Annual real GDP growth:**

`Growth (%) = [(Real GDP in year t / Real GDP in year t−1) − 1] × 100`

**Quarterly year-on-year real GDP growth:**

`Growth (%) = 100 × [(Real GDP in quarter t / Real GDP in the same quarter of the previous year) − 1]`

This formula compares the same quarter across two years. Quarter-on-quarter growth instead compares the quarter with the immediately preceding quarter; it is a different measure and must not be presented as year-on-year growth. The seasonal-adjustment status of the NBS quarterly series remains unverified.

Do not calculate annual real GDP growth by summing quarterly constant-price GDP values unless the official aggregation method has been verified. Use an officially published annual growth series or document and verify the annual calculation method first.

## Required metadata
- Economy and geographic coverage
- Statistical agency and series name
- Observation period and publication date
- Unit and reference/base year, if applicable
- Revisions or methodology changes
- Data vintage or release edition
- Observation status, such as preliminary, revised, or estimate, where the source provides it
- Historical methodology or rebasing changes
- Seasonal-adjustment status
- Direct source URL or document reference

## Preferred sources
- Primary source: Nigeria's National Bureau of Statistics (NBS), using its official GDP reports, tables, and methodology documentation.
- Cross-check: International Monetary Fund (IMF) World Economic Outlook database.
- Do not silently combine NBS and IMF values. Record the source and investigate discrepancies.

### Official source references

- [NBS GDP methodology](https://www.nigerianstat.gov.ng/page/gdp-methodology)
- [NBS GDP publication catalogue and quarterly reports](https://microdata.nigerianstat.gov.ng/index.php/catalog/147)
- [NBS 2025 GDP rebasing report](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1256/GDP_Rebasing_2025_%20Final.pdf)
- [NBS GDP Q1 2025 tables (`Q1_2025_GDP_Estimates.xlsx`)](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1259/Q1_2025_GDP_Estimates.xlsx)
- [NBS GDP Q4 2024 tables (`Q4_GDP_2024.xlsx`)](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1158/Q4_GDP_2024.xlsx)
- [NBS 2025 GDP rebasing tables (`2019-2024_rebased_figures.xlsx`)](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1257/2019-2024_rebased_figures.xlsx)

NBS is the primary source for Nigeria's GDP estimates. The NBS GDP catalog also lists the Q2 2026 GDP release and its downloadable report package; see the catalog for the current release file.

## Verified Findings and Evidence Status

### Directly reported by NBS

- The 2025 GDP rebasing adopted **2019 as the new base year**. The NBS *Rebasing Nigerian Gross Domestic Product Report 2025*, Methodology section, describes the rebasing and its coverage.
- The Q1 2025 workbook, Sheet 1 section **“Gross Domestic Product At 2019 Constant Basic Prices”** and Sheet 3 **“real gdp growth rate %,”** reports real GDP growth at 2019 constant prices from **Q1 2024 through Q1 2025**.
- The NBS Q2 2026 GDP workbook reports quarterly real GDP growth from **Q1 2024 through Q2 2026**. The NBS GDP catalog identifies the Q2 2026 release; the workbook is part of its downloadable release materials.
- The NBS 2025 rebasing workbook, `2019-2024_rebased_figures.xlsx`, includes annual real GDP growth figures for **2020–2024**.
- The NBS Q4 2024 workbook, `Q4_GDP_2024.xlsx`, reports GDP at **2010 constant prices**. The newer rebased workbooks use **2019 constant prices**.
- The NBS Q1 2025 GDP Report, Preface and Overview, says previous quarterly estimates were benchmarked to rebased annual estimates to align the old series and provide new quarterly series. This documents NBS's stated rebasing approach, but does not establish the full back-series coverage or prove that every historical growth estimate is directly comparable.

### Interpretation and recommended procedure

- The reviewed NBS releases show growth estimates under both the former 2010-price basis and the rebased 2019-price basis. Treat this as a **historical comparability issue requiring investigation**. The difference in base year alone does not establish that growth rates are incomparable, and the documents reviewed do not fully explain differences in growth rates between these releases.
- Use the 2019-constant-price NBS releases as the current candidate source for rebased observations, while recording release date and data vintage. Do not splice the 2010- and 2019-price series or infer a continuous retrospective series until NBS documentation supports that treatment.
- Calculate quarterly year-on-year growth only from comparable real GDP observations for the quarter and the same quarter one year earlier, using the stated formula. Do not infer seasonal adjustment or annualize quarter-on-quarter change.
- Use the published annual growth figures for 2020–2024 as the verified annual observations in that workbook. Do not derive annual growth by summing quarterly constant-price values before establishing NBS's official annual aggregation method.

### Evidence not established by the reviewed materials

The reviewed workbooks and reports do not establish the earliest observation in the complete retrospectively rebased quarterly series, the quarterly series' seasonal-adjustment status, a complete revision policy or data-vintage archive, or the historical effect of rebasing on quarterly growth estimates. These remain open research questions, not established facts.

## Revision and comparability rules
- Prefer the latest available internally consistent official series for current historical analysis.
- Preserve earlier releases where available for future real-time historical testing.
- Record revisions, methodological breaks, and rebasing changes.
- Do not join historical series across methodological changes until comparability has been checked.
- Never interpret a statistical revision automatically as a real economic shock.

## Interpretation cautions
- Real GDP growth is not the same as productivity growth.
- GDP growth does not directly measure GDP per capita, household welfare, or income distribution.
- Aggregate growth can conceal differences between sectors.
- Growth alone does not establish financial health or identify the cause of an economic change.
- One observation must not determine an economic-state classification.
- Revisions can materially change the historical picture.
- Different quarterly and annual growth measures can tell different stories.

## Open Questions for Future Research

- What is the earliest observation in the complete retrospectively rebased quarterly series?
- What is the seasonal-adjustment status of the quarterly series?
- What is NBS's revision policy, including how preliminary estimates and data vintages are identified and preserved?
- What are the historical effects of the 2025 rebasing on quarterly growth estimates, and what official method supports comparisons across the former 2010-price and new 2019-price series?
- What is the official method for calculating annual real GDP growth from quarterly data?
- Which exact IMF comparison series should be used, and what are its definitions, price basis, frequency, vintage, and metadata?
- Which historical testing period is defensible given the verified coverage and methodological changes?

## Next action
Continue verifying the NBS series and resolve the open questions above, beginning with full rebased quarterly coverage, seasonal adjustment, revisions, and comparability. Do not classify Nigeria's economic state until measurement and historical testing are sufficiently established.

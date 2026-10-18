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

`Growth (%) = [(Real GDP in quarter t / Real GDP in the same quarter of the previous year) − 1] × 100`

The quarterly year-on-year formula compares the same quarter across two years, while quarter-on-quarter growth uses the immediately preceding quarter and is a different measure.

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

### Source references to verify

- [NBS GDP methodology](https://www.nigerianstat.gov.ng/page/gdp-methodology)
- [NBS GDP publication catalogue and quarterly reports](https://microdata.nigerianstat.gov.ng/index.php/catalog/147)
- [NBS 2025 GDP rebasing report](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1256/GDP_Rebasing_2025_%20Final.pdf)

These are initial source references. The exact GDP tables, series, historical coverage, and revision practices have not yet been fully verified.

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

## Open questions
- Which exact NBS quarterly and annual GDP tables and series should be used?
- What historical coverage is available on a consistent methodological basis?
- What is the seasonal-adjustment status of the quarterly series?
- How are preliminary observations and revisions documented?
-  How should data before and after the 2025 GDP rebasing, which uses 2019 as the new base year, be compared?
- Which historical test window is suitable?

## Next action
Verify the current NBS quarterly and annual real GDP series. Document their exact source details, historical coverage, seasonal-adjustment status, revision practices, and comparability after rebasing. Do not classify Nigeria's economic state until measurement and historical testing are sufficiently established.

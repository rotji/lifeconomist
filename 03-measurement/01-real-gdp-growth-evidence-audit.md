# Indicator 1 — Real GDP Growth: Evidence Audit and Measurement Decisions

**Audit date:** 2026-10-30  
**Status:** Desk evidence audit; specification remains draft and is not approved for economic-state classification.  
**Scope:** Resolve what the available NBS source catalogue and rebasing documentation establish, distinguish verified facts from open questions, and set the next research sequence. This is not a fresh independent extraction of every value in the latest workbook.

## 1. Executive finding

The project has enough evidence to define a provisional measurement design, but not enough to approve a fully reproducible, real-time historical indicator series.

The best-supported initial design is:

1. **Primary headline measure:** NBS-published annual real GDP growth on the rebased 2019-price basis, with the exact publication and data vintage recorded.
2. **Quarterly companion measure:** NBS-published quarterly year-on-year real GDP growth from one internally consistent release series.
3. **Not yet approved:** Quarter-on-quarter growth, because the seasonal-adjustment status and appropriate treatment have not been established.
4. **Not permitted:** Silent splicing of 2010-price and 2019-price series, or combining NBS and IMF observations without an explicit reconciliation.
5. **Not permitted:** Economic-state classification from this indicator alone. Indicator approval requires data-quality checks, historical testing and integration with the broader framework.

This is a provisional research decision, not proof that all historic observations are comparable.

## 2. Source inventory and evidence status

| Question | Evidence currently available | Status | Consequence |
|---|---|---|---|
| What is the official source for Nigeria's GDP estimates? | NBS GDP collection and its official reports/tables. The collection lists quarterly GDP releases and downloadable report packages. | Established | Use NBS as the primary series. |
| What is the current rebased reference year? | NBS's 2025 rebasing report identifies 2019 as the new base year and describes the rebasing exercise and expanded benchmark information. | Established | Record 2019-price basis for the rebased series. |
| What annual growth figures are reported in the rebasing summary? | NBS reports real GDP growth of -6.96% (2020), 0.95% (2021), 4.32% (2022), 3.04% (2023), and 3.38% (2024). | Established as published values in the rebasing summary | Treat these as source-reported observations, retaining the report vintage; do not assume they can never be revised. |
| Is a Q2 2026 release available? | NBS GDP collection search results identify the Q2 2026 report package, dated 2026-08-31, with a PDF report and workbook. | Established at catalogue level | Use the release package as the latest located quarterly candidate as of this audit date; inspect the actual workbook before ingestion. |
| What quarterly observations are in the Q2 2026 workbook? | The existing indicator research record reports quarterly real GDP growth observations from Q1 2024 through Q2 2026. This audit has not independently re-extracted every workbook cell. | Previously recorded; re-extraction pending | Verify the workbook tabs, series labels, first and last periods, and missing values before declaring coverage complete. |
| Does the public methodology page fully reflect the rebased series? | The NBS GDP methodology page still describes a series at constant 2010 prices, while the 2025 rebasing report and newer quarterly releases use the 2019 reference year. | Documentation mismatch observed | Treat the older static methodology page as background, not as sufficient evidence for the current series definition. Resolve against the latest release methodology. |
| Are quarterly observations seasonally adjusted? | No explicit statement establishing the adjustment status has been found in the reviewed materials. | Unresolved | Do not interpret quarter-on-quarter change as an underlying trend or annualize it. |
| Is there a complete public revision policy and data-vintage archive? | The reviewed source pages establish release availability but do not provide a complete, verified policy and vintage archive. | Unresolved | Preserve each downloaded release and document changes between releases. |
| Can 2010-price and 2019-price series be joined? | NBS describes a rebasing and benchmark process; earlier and newer releases use different reference years. A base-year change alone does not prove that growth rates are incomparable, nor does it by itself establish that a splice is safe. | Unresolved for the proposed series | Do not splice until the overlap, back-series method and official comparability guidance are documented. |
| What IMF series should be used for comparison? | The indicator specification names IMF WEO as a possible cross-check but does not yet identify an exact series, vintage and transformation. | Unresolved | Keep IMF outside the primary time series until an explicit series mapping is recorded. |

## 3.1 Follow-up check — Q2 2026 release headline (2026-10-30)

The NBS catalogue entry was rechecked. It lists a 1.07 MB ZIP release dated 2026-08-31 and names two contents: `Q2_2026_GDP_Report_.pdf` and `Q2 2026 GDP_w.xlsx`. The release is discoverable at catalogue level, but this environment could not retrieve the ZIP bytes through either the direct download attempt or the web-open route. **No workbook cells, sheet names, formulas, or internal series labels have therefore been inspected in this follow-up.**

A separate public report of the NBS release gives the headline quarterly year-on-year real GDP growth as **4.43% for Q2 2026**, compared with **3.89% for Q1 2026** and **4.23% for Q2 2025**. This is a useful external headline cross-check, not a substitute for checking the NBS workbook itself. Sources: [Voice of Nigeria, 1 September 2026](https://von.gov.ng/nigerias-gdp-growth-accelerates-to-4-43-in-q2-2026/) and [Reuters, 31 August 2026](https://www.reuters.com/world/africa/nigerias-q2-gdp-growth-443-yy-stats-office-2026-08-31/).

### Interim validation record

| Check | Result | Evidence status |
|---|---|---|
| Q2 2026 release package exists in NBS catalogue | Yes; release date 2026-08-31; ZIP listing names PDF and Excel workbook | Verified at catalogue level |
| Published Q2 2026 headline growth | 4.43% year-on-year in real terms | Cross-checked through public reporting of the NBS release; workbook not inspected |
| Q1 2026 comparison | 3.89% year-on-year | Cross-checked through public reporting of the NBS release; not a vintage reconciliation |
| Q2 2025 comparison | 4.23% year-on-year | Cross-checked through public reporting of the NBS release; not a vintage reconciliation |
| Workbook tabs, cells, formulas, full history, missing values, units and footnotes | Not inspected because the source ZIP could not be retrieved in this execution environment | **Open — Task 1 incomplete** |
| Revisions between Q1/Q2 2026 or earlier releases | Not tested | Open |
| Seasonal-adjustment statement | Not established by this check | Open |

**Interpretation boundary:** The reported move from 3.89% to 4.43% is a 0.54 percentage-point increase in the year-on-year growth rate. It does not mean output grew 0.54% quarter-on-quarter, and it does not establish that the underlying series is seasonally adjusted. The rate compares Q2 2026 real output with Q2 2025 real output, according to the published comparison basis.

**Next operational step:** Obtain the ZIP or workbook through a retrievable route (for example, a user-provided upload if the official link continues to fail), then inspect the workbook directly. Do not mark the workbook validation complete until the actual file has been read and the report headline reconciled to its exact series and period.

## 3. Primary-source references

- [Voice of Nigeria: Q2 2026 GDP growth headline (1 September 2026)](https://von.gov.ng/nigerias-gdp-growth-accelerates-to-4-43-in-q2-2026/) — secondary reporting of NBS's published headline; not a workbook substitute.
- [Reuters: Nigeria's Q2 GDP growth 4.43% (31 August 2026)](https://www.reuters.com/world/africa/nigerias-q2-gdp-growth-443-yy-stats-office-2026-08-31/) — independent report of the NBS release; not a workbook substitute.
- [NBS GDP collection and related materials](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/related-materials) — quarterly releases and downloadable source packages.
- [NBS Q2 2026 release package](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1433) — catalogue-listed PDF and Excel workbook; release date shown as 2026-08-31.
- [NBS 2025 GDP rebasing report](https://microdata.nigerianstat.gov.ng/index.php/catalog/147/download/1256/GDP_Rebasing_2025_%20Final.pdf) — 2019 reference year, benchmark design, and published annual growth summary.
- [NBS GDP methodology page](https://www.nigerianstat.gov.ng/page/gdp-methodology) — useful background on quarterly national accounts and production-method compilation, but its displayed 2010-price description does not by itself specify the newer rebased series.
- [World Bank: Why do countries revise their national accounts?](https://datahelpdesk.worldbank.org/knowledgebase/articles/680284-why-do-countries-revise-their-national-accounts) — background on revisions, rebasing and possible breaks; general guidance, not evidence of NBS's exact policy.

## 4. Measurement decisions to adopt provisionally

### 4.1 Keep annual and quarterly indicators distinct

Annual growth compares annual real GDP in year (y) with year (y-1). Quarterly year-on-year growth compares a quarter with the same quarter one year earlier. They are related but not interchangeable, and a quarterly year-on-year series is not a substitute for the annual series.

### 4.2 Use the published rate when NBS publishes it

For the initial indicator, store the official NBS growth rate as the source observation. Independently recalculate it from published real GDP levels only when the relevant levels, period definitions and rounding rules are available. Compare the recalculated value to the published rate and record any difference rather than silently overwriting the official value.

### 4.3 Treat source release as part of the observation

A stored observation should carry, at minimum:

- economy = Nigeria;
- indicator and frequency = annual or quarterly;
- reference period;
- measure = real GDP growth;
- comparison basis = annual year-on-year or quarterly year-on-year;
- source agency and source table/sheet;
- price/reference-year basis = 2019 for the rebased candidate;
- published value and unit;
- release/publication date;
- date the project retrieved the source;
- source URL and local filename;
- provisional/revised/final label, if stated;
- source vintage and methodology/rebasing notes;
- verification status and any unresolved comparability flag.

The release date and retrieval date are different fields: the former identifies when the agency published the data; the latter records when the project acquired that edition.

### 4.4 Do not confuse a statistical revision with a new economic event

A revision may reflect later source data, a benchmark update, a methodological change, or a correction. Preserve old vintages when possible so later analysis can distinguish what was known at the time from what is known after revision.

### 4.5 Do not infer seasonal adjustment

Quarter-on-quarter growth should remain outside the approved core specification until the exact series' seasonal-adjustment status and official calculation basis are established. Annual and same-quarter-year-on-year comparisons can be used provisionally, while still recording the limitation that the underlying series methodology and revisions require validation.

## 5. Remaining research tasks, in priority order

This order reflects known dependencies and evidence value; it is not an obligation to finish the entire audit immediately. On return, first verify whether the workbook, source releases, or relevant methods have changed, then resume from the first unresolved task whose dependencies and current value justify attention. Do not repeat completed checks without a reproducibility, contradiction, or new-evidence reason. Record any changed conclusion and review downstream effects on the indicator specification, source-vintage treatment, historical tests, and any later state assessment. See the [project-wide Continuity, Pause, and Revision Principle](../RESEARCH-METHODOLOGY.md#continuity-pause-and-revision-principle).

This order reflects known dependencies and evidence value; it is not an obligation to finish the entire audit immediately. On return, first verify whether the workbook, source releases, or relevant methods have changed, then resume from the first unresolved task whose dependencies and current value justify attention. Do not repeat completed checks without a reproducibility, contradiction, or new-evidence reason. Record any changed conclusion and review downstream effects on the indicator specification, source-vintage treatment, historical tests, and any later state assessment. See the [project-wide Continuity, Pause, and Revision Principle](../RESEARCH-METHODOLOGY.md#continuity-pause-and-revision-principle).

### Task 1 — Extract and validate the latest release workbook

Download the Q2 2026 package; identify the workbook tabs and exact growth-rate series; capture the first and last observation, all periods, blank cells, units, price basis and any footnotes. Cross-check the report's headline against the workbook. Record the file and retrieval date. This task is not complete merely because the catalogue lists the package.

### Task 2 — Verify quarterly history and back-series coverage

Compare the Q2 2026 workbook with the Q1 2025, Q2 2025, Q3 2025, Q4 2025 and Q1 2026 release packages. Establish which historic quarters appear in each edition, whether old observations were revised, and whether the current rebased quarterly series reaches earlier than Q1 2024. Do not infer absence from one workbook alone.

### Task 3 — Resolve seasonal-adjustment status

Search the current rebased quarterly report, workbook notes and any technical documentation for explicit statements about seasonal adjustment, adjustment methods and annualization. If the documentation remains silent, record “not stated in reviewed documentation” and ask NBS for clarification rather than guessing.

### Task 4 — Establish revision and vintage treatment

Document whether NBS identifies preliminary/revised estimates, which periods may be revised, whether superseded workbooks remain accessible, and whether there is a published revisions policy. Until resolved, archive each source release with retrieval metadata and compare overlapping observations between vintages.

### Task 5 — Resolve rebasing comparability

Build a comparison table from overlapping 2010-price and 2019-price releases where the same periods and measure are published. Record level differences, growth-rate differences, the rebasing/benchmarking method and any official linking guidance. Do not decide that the series can or cannot be spliced solely because the base year changed.

### Task 6 — Define the IMF cross-check

Choose the exact IMF series and record its frequency, concept, unit, price basis, vintage/date, and whether values are observed estimates or projections. Compare only like with like and keep IMF data as a separately sourced cross-check, not a silent substitute for NBS.

### Task 7 — Historical test and approval gate

Once the above tasks are completed, test for missing periods, duplicate periods, unexplained jumps, revisions, formula agreement, and break sensitivity. Compare real-time vintages with latest revised history if feasible. Approve the indicator only after the team can reproduce its source values and explain the known limitations.

## 6. Approval gate

Indicator 1 remains **draft / not approved for state classification** until:

- the selected annual and quarterly series are precisely identified;
- source observations can be reproduced from retained official releases;
- the history and price/reference-year basis are documented;
- seasonal-adjustment status is explicitly resolved or quarterly quarter-on-quarter growth is excluded;
- revision and vintage risks have a documented handling procedure;
- rebasing/comparability limits are documented;
- historical validation is completed and reviewed.

Even after indicator approval, GDP growth alone cannot establish an economic state or prove the cause of a change. It must be interpreted alongside the other core indicators, supporting measurements, and evidence about economic mechanisms.

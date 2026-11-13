# Global Financial System Source and Measurement Register

**Status:** Initial source discovery and candidate-series mapping; not a completed series-level audit.  
**Started:** 2026-11-13  
**Parent:** [Global Financial System Exploration Map](GLOBAL-FINANCIAL-SYSTEM-EXPLORATION-MAP.md)  
**Purpose:** Identify real, accessible official data collections that may support the map's questions. Preserve definitions and boundaries before extracting, comparing, combining, or calculating observations.

## 1. How to read this register

This is a source-discovery register, not a global financial database and not a declaration that the listed sources are fully comparable or complete.

Status labels:
- **Identified:** An official dataset or statistical collection has been located and its broad purpose confirmed.
- **Candidate:** Potentially useful for a defined analytical object, but detailed series, coverage, definitions, and access still need examination.
- **Audit pending:** The individual series metadata, reporting population, classifications, revisions, and downloadable observations have not yet been fully checked.
- **Not established:** Do not infer availability, coverage, or comparability from a source-family name alone.

A source collection may contain many series with different coverage and quality. Audit at series level before use.

## 2. Minimum metadata required for every selected series

| Field | Required record |
|---|---|
| Register ID | Stable internal identifier |
| Source owner | Institution responsible for publication |
| Dataset / table / series | Exact official name and identifier |
| Direct source | Dataset page and, where available, series or API URL |
| Measurement object | What is actually being measured |
| Stock or flow | Position at a date, transaction over a period, rate, index, or other |
| Sector / counterparty | Institutional sector and counterparty definition |
| Residence basis | Residence, nationality, parent location, custody, or other |
| Instrument / category | Instrument and classification used |
| Unit and currency | Native units, scale, currency, and conversion basis |
| Valuation | Market, nominal, book, face, or other basis |
| Frequency and dates | Frequency, first/last observation, and observation date convention |
| Geographic coverage | Reporting economies, aggregates, and missing economies |
| Publication lag | Time between observation and release |
| Revisions / vintages | Revision policy and availability of historical vintages |
| Methodology | Manual, compilation method, estimation and adjustments |
| Access and licence | API, bulk download, registration, restrictions, permitted reuse |
| Known limitations | Gaps, breaks, nonresponse, estimates, confidentiality, comparability |
| Audit status | Identified, candidate, audited, rejected, or superseded |
| Audit date | Date metadata and actual data were checked |

Do not fill missing metadata by assumption. Use **unknown**, **not stated**, or **not yet checked**.

## 3. Initial official source inventory

### 3.1 International Monetary Fund (IMF)

#### IMF Monetary and Financial Statistics (MFS) — Monetary Aggregates
- **Register ID:** IMF-MFS-MA
- **Official source:** https://data.imf.org/en/Datasets/MFS_MA
- **Object:** Monetary aggregates compiled from standardized reporting forms while also reflecting country-specific components aligned with national definitions.
- **Potential use:** Country-level money measures and their components; comparison of monetary structures where definitions permit.
- **Known caution:** National definitions and components can differ. Do not assume an identically named aggregate is fully comparable across countries without checking metadata and country practices.
- **Frequency shown by IMF catalogue:** Annual, monthly, quarterly.
- **Status:** Identified; series-level audit pending.

#### IMF Monetary and Financial Statistics (MFS) — Financial Corporations
- **Register ID:** IMF-MFS-FC
- **Official source:** https://data.imf.org/en/Datasets/MFS_FC
- **Object:** Consolidated balance sheets of central banks, other depository corporations (ODCs), and other financial corporations (OFCs), including financing to nonresidents and domestic nonfinancial sectors.
- **Potential use:** Financial-sector balance-sheet positions and financing relationships.
- **Known caution:** Sector coverage, consolidation, instrument detail, and country reporting must be checked before interpreting as a complete national financial balance sheet.
- **Frequency shown by IMF catalogue:** Annual, monthly, quarterly.
- **Status:** Identified; series-level audit pending.

#### IMF Balance of Payments (BOP)
- **Register ID:** IMF-BOP
- **Official source:** https://data.imf.org/Datasets/BOP
- **Object:** Transactions between residents and nonresidents over a period, including current, capital, and financial accounts.
- **Potential use:** Cross-border flows, including trade, income, transfers, and financial transactions.
- **Known caution:** BOP is a flow statement, not an end-period stock statement. Check BPM vintage, reporting coverage, directional conventions, and revisions.
- **Frequency shown by IMF catalogue:** Annual and quarterly.
- **Status:** Identified; series-level audit pending.

#### IMF International Investment Position (IIP)
- **Register ID:** IMF-IIP
- **Official source:** https://data.imf.org/Datasets/IIP
- **Object:** At a point in time, residents' financial assets that are claims on nonresidents (plus reserve-asset monetary gold) and residents' liabilities to nonresidents.
- **Potential use:** External asset and liability stocks, instrument composition, and net international investment position.
- **Known caution:** It is an external balance-sheet view, not a complete national balance sheet. Reconcile stock changes with financial transactions, exchange-rate changes, price changes, and other volume changes where possible.
- **Status:** Identified; series-level audit pending.

#### IMF Portfolio Investment Positions by Counterpart Economy (PIP; formerly CPIS)
- **Register ID:** IMF-PIP
- **Official source:** https://data.imf.org/en/Datasets/PIP
- **Object:** Participating economies' holdings of portfolio investment securities by counterpart economy, separately requesting equity and investment fund shares, long-term debt, and short-term debt.
- **Potential use:** Geographic and instrument distribution of cross-border portfolio asset positions.
- **Known caution:** Voluntary participation and reporting coverage matter. This is portfolio investment, not all cross-border financial claims. Position changes include valuation effects as well as transactions.
- **Frequency shown by IMF catalogue:** Annual and half-yearly.
- **Status:** Identified; series-level audit pending.

#### IMF Quarterly Government Finance Statistics (QGFS) / Government Finance Statistics
- **Register ID:** IMF-QGFS
- **Official catalogue:** https://data.imf.org/en/Datasets
- **Object:** Government revenue, expenditure, net lending/borrowing, financing transactions, and balance-sheet information at different government coverage levels.
- **Potential use:** Public-sector fiscal flows and selected asset/liability positions.
- **Known caution:** Confirm whether the observation covers budgetary central government, central government, or general government; frequency and reporting availability can vary. Do not treat appropriations as executed expenditure.
- **Status:** Identified in IMF catalogue; exact table/series selection and coverage audit pending.

### 3.2 Bank for International Settlements (BIS)

The BIS Data Portal provides multiple distinct statistical collections. They must not be collapsed into one generic measure of global finance.

Official catalogue: https://data.bis.org/topics  
Statistics overview and documentation: https://www.bis.org/statistics  
Bulk downloads: https://data.bis.org/bulkdownload

#### BIS Locational Banking Statistics (LBS)
- **Register ID:** BIS-LBS
- **Object:** International banking activity from the residence perspective, organized by the location of the banking office; includes geographical and currency composition of banks' assets and liabilities and intragroup business.
- **Potential use:** Cross-border bank claims and liabilities by residence, counterparty, and currency.
- **Known caution:** Residence/location view; intragroup positions are included. Do not confuse with consolidated banking-group risk exposures.
- **Latest bulk-download release observed during discovery:** 29 October 2026.
- **Status:** Identified; detailed series and reporting-population audit pending.

#### BIS Consolidated Banking Statistics (CBS)
- **Register ID:** BIS-CBS
- **Object:** Worldwide consolidated positions of internationally active banking groups headquartered in reporting countries.
- **Potential use:** Country-risk and consolidated banking-group exposure analysis.
- **Known caution:** Parent-headquarters/consolidation perspective differs from LBS residence perspective. Immediate-counterparty and ultimate-risk bases are distinct.
- **Latest bulk-download release observed during discovery:** 29 October 2026.
- **Status:** Identified; detailed series and reporting-population audit pending.

#### BIS Credit to the Non-Financial Sector
- **Register ID:** BIS-CREDIT-NFS
- **Object:** Borrowing activity of government and private nonfinancial sectors.
- **Potential use:** Credit/debt stocks, sector comparisons, credit-to-GDP measures, and debt-service analysis.
- **Known caution:** Inspect instrument, borrower-sector, lender, valuation, and GDP denominator definitions. Do not assume the series is identical to domestic bank lending.
- **Status:** Identified; detailed series and methodology audit pending.

#### BIS Global Liquidity Indicators (GLI)
- **Register ID:** BIS-GLI
- **Official source:** https://data.bis.org/topics/GLI
- **Object:** Credit to non-bank borrowers, covering bank loans and funding from international debt securities; focuses on foreign-currency credit in US dollars, euros, and Japanese yen to nonresidents outside the respective currency areas.
- **Potential use:** Cross-border foreign-currency credit and global funding conditions.
- **Known caution:** It is not all global liquidity, all money, or all credit. The foreign-currency/nonresident boundary is essential. Separate bank loans from international debt securities and residents from nonresidents.
- **Frequency shown by BIS:** Quarterly.
- **Latest release observed during discovery:** 29 October 2026.
- **Status:** Identified; detailed series audit pending.

#### BIS Debt Securities Statistics and International Debt Securities
- **Register ID:** BIS-DEBT-SEC
- **Object:** Borrowing through debt capital markets, with domestic and international issuance distinguished; international debt securities are BIS-compiled using security-level commercial data.
- **Potential use:** Outstanding securities, issuance, currency, market, and issuer-sector composition.
- **Known caution:** Domestic and international definitions differ; issuance flows and outstanding stocks must not be mixed. Review source construction and commercial-vendor coverage for international series.
- **Status:** Identified; detailed series audit pending.

#### BIS Debt Service Ratios (DSR)
- **Register ID:** BIS-DSR
- **Object:** Income used for interest payments and amortisations.
- **Potential use:** Debt-service burden for covered sectors and economies.
- **Known caution:** Check sector coverage, income denominator, model/estimation method, and frequency before comparison.
- **Status:** Identified; detailed methodology audit pending.

#### Other BIS collections to consider later
- Derivatives statistics (exchange-traded and OTC; turnover, notional amounts, and gross market values are different objects).
- Central-bank total assets and policy rates.
- Exchange rates and effective exchange rates.
- Payment statistics and financial market infrastructures.
- Residential and commercial property prices.
- These are candidates, not yet audited series.

### 3.3 World Bank

#### Financial Development Data (FinData)
- **Register ID:** WB-FINDATA
- **Official source:** https://data.worldbank.org/collections/findata
- **Methodology:** https://documents.worldbank.org/en/publication/documents-reports/documentdetail/099101926140040193
- **Object:** Financial-system development indicators across banks, non-bank financial institutions, equity markets, and debt markets, assessed through depth, access, efficiency, and stability.
- **Coverage described by World Bank:** Up to 218 economies; annually updated; data extending back to 1980. The portal also describes 34 core indicators and composite indices, with actual coverage varying by indicator.
- **Potential use:** Cross-country structural comparison and financial-system development context.
- **Known caution:** Composite indices are constructed measures, not raw financial stocks or flows. Inspect the underlying indicator definition, data treatment, coverage, and index construction. Do not use an overall index as a substitute for specific financial quantities.
- **Status:** Identified; indicator-level audit pending.

#### World Development Indicators (WDI) and International Debt Statistics (IDS)
- **Register ID:** WB-WDI-IDS
- **Official catalogue:** https://databank.worldbank.org/databases
- **Object:** Broad national development and macroeconomic indicators; IDS provides external debt statistics and related debt information.
- **Potential use:** Country context, GDP denominators, selected external-debt stocks and flows, and development-finance context.
- **Known caution:** WDI aggregates and indicators draw from multiple original sources. Record the original provider and definition. IDS has its own reporting and coverage rules. Do not assume WDI's inclusion makes every series equally current or comparable.
- **Status:** Identified; specific indicators and series audit pending.

### 3.4 Organisation for Economic Co-operation and Development (OECD)

#### Institutional Investors' Assets and Liabilities
- **Register ID:** OECD-II-AL
- **Official source:** https://data-explorer.oecd.org/
- **Observed table:** Institutional Investors' Assets and Liabilities.
- **Object:** Financial assets and liabilities of investment funds, insurance corporations, and pension funds by financial instrument; net financial worth and nonfinancial assets where available.
- **Potential use:** Institutional balance-sheet composition and comparison of investor sectors/instruments.
- **Known caution:** OECD table notes that data are non-consolidated unless otherwise specified. Coverage is OECD reporting economies and may vary; it is not a complete global institutional-investor census. Do not sum without considering counterpart positions and consolidation.
- **Status:** Identified; country and series coverage audit pending.

## 4. First-pass analytical crosswalk

This crosswalk identifies candidate sources only. It does not claim that any one source answers the whole question.

| Question / object | Candidate collections | Key boundary to preserve |
|---|---|---|
| Monetary aggregates | IMF MFS Monetary Aggregates; national central banks | Country-specific monetary definitions and institutional coverage |
| Financial-sector balance sheets | IMF MFS Financial Corporations; national financial accounts | Sector coverage, consolidation, counterpart positions |
| Cross-border transactions | IMF BOP | Period flows, resident/nonresident basis |
| External asset/liability stocks | IMF IIP | End-period external positions, not total national wealth |
| Portfolio holdings by counterpart | IMF PIP | Voluntary reporting, portfolio-only scope, valuation effects |
| Government finances | IMF QGFS/GFS; national treasuries | Government perimeter, cash/accrual basis, execution |
| Cross-border bank positions | BIS LBS | Residence of banking office; intragroup inclusion |
| Consolidated bank exposures | BIS CBS | Banking-group consolidation and risk basis |
| Nonfinancial-sector credit | BIS Credit to Non-Financial Sector | Borrower sectors, instruments, lender scope |
| Foreign-currency global credit | BIS GLI | USD/EUR/JPY, nonbank borrowers, nonresident boundary |
| Debt securities | BIS debt securities; national debt offices | Domestic/international classification, stocks/issuance |
| Debt-service burden | BIS DSR; national debt statistics | Sector, income denominator, methodology |
| Financial development structure | World Bank FinData | Indicator vs composite index; variable coverage |
| External debt | World Bank IDS; IMF and national sources | Debtor coverage, creditor basis, instrument, valuation |
| Institutional investor balance sheets | OECD institutional investors; national financial accounts | Non-consolidated/consolidated; geographic coverage |

## 5. Priority for the next audit pass

Do not attempt to download every dataset at once. The next useful step is to select a small, complementary starter set and inspect exact series metadata and observations.

A defensible initial pilot could include:
1. **IMF MFS Monetary Aggregates** — monetary stocks and country definitions.
2. **IMF MFS Financial Corporations** — financial-sector balance-sheet structure.
3. **BIS Credit to the Non-Financial Sector** — credit stocks and borrower sectors.
4. **IMF BOP and IIP** — external transaction flows and end-period external positions.
5. **BIS LBS and CBS** — two different views of international banking exposures.

For each selected collection, choose a small number of economies only after checking availability. Nigeria may be included as an initial test case, but global scope must be preserved; do not treat Nigeria's data availability as representative of all countries. Include at least one economy with strong reporting coverage as a methodological comparison if useful, and record why it was selected.

Before extracting data, answer:
- What is the exact series/table identifier?
- What is the precise definition and accounting boundary?
- What is the observation date or period?
- What unit, currency, scale, and valuation basis apply?
- Which sectors and instruments are included/excluded?
- Which countries report, and what is missing?
- Are there breaks, revisions, estimates, or changes in methodology?
- Can the same object be independently checked or reconciled?
- What question will the observation help answer?

## 6. Important distinctions and unresolved issues

- MFS monetary aggregates are not the same thing as total financial-sector assets or global wealth.
- BOP records transactions over time; IIP records external asset/liability positions at a date.
- IIP is not a complete national balance sheet and does not capture all domestic assets and liabilities.
- BIS LBS and CBS use different organizational perspectives and cannot be treated as duplicate versions of one measure.
- BIS GLI is a defined foreign-currency credit measure, not a universal liquidity aggregate.
- Credit stocks, debt securities outstanding, issuance flows, and market valuations are distinct.
- Institutional investors' assets under management, balance-sheet assets, commitments, uncalled commitments, and deployed capital are not interchangeable.
- Composite financial-development indices are not direct measurements of financial wealth, credit, or investable capital.
- A global total must not be constructed by summing datasets with overlapping coverage or incompatible perimeters.
- The actual latest observations, country coverage, release vintages, and series-level metadata remain to be verified in the next audit stage.

## 7. Discovery sources reviewed

The following official pages were reviewed for this first-pass inventory (accessed 2026-11-13):

- IMF Datasets catalogue: https://data.imf.org/en/Datasets
- IMF MFS Financial Corporations: https://data.imf.org/en/Datasets/MFS_FC
- IMF BOP: https://data.imf.org/Datasets/BOP
- IMF IIP: https://data.imf.org/Datasets/IIP
- IMF PIP: https://data.imf.org/en/Datasets/PIP
- BIS statistics overview: https://www.bis.org/statistics
- BIS Data Portal topics: https://data.bis.org/topics
- BIS Global Liquidity Indicators: https://data.bis.org/topics/GLI
- BIS bulk downloads: https://data.bis.org/bulkdownload
- World Bank FinData: https://data.worldbank.org/collections/findata
- World Bank FinData methodology: https://documents.worldbank.org/en/publication/documents-reports/documentdetail/099101926140040193
- World Bank DataBank: https://databank.worldbank.org/databases
- OECD Data Explorer: https://data-explorer.oecd.org/

This list records discovery references, not a complete bibliography or series-level audit. The linked dataset pages and metadata should be revisited when the individual series are selected.

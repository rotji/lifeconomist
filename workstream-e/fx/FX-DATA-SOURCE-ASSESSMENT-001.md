# FX Data Source Assessment 001 — Historical Cross-Rates vs Executable Quotes

**Programme:** E-FX-001  
**Workstream:** E — Opportunity Intelligence and Economic Application  
**Assessment date:** 2026-10-27  
**Status:** Initial source screening; terms and technical coverage require verification before operational use  
**Purpose:** Identify low-cost sources for the first mathematical/network tests and clearly mark the limits of each source.

## 1. Decision summary

Use official and low-cost daily reference series to validate cross-rate arithmetic, inspect historical currency relationships and build the initial network dataset. Do **not** use daily reference/midpoint data to claim executable triangular arbitrage. That claim requires time-aligned bid/ask prices and proof that the relevant transactions can be executed under the same practical conditions.

Initial source roles:
- **ECB reference rates:** a candidate official daily reference series for euro-based historical comparisons.
- **Bank of Canada daily rates:** a candidate multi-currency historical reference series with CSV/JSON/XML access.
- **CBN NFEM data:** a Nigeria-specific official-market reference for USD/NGN context and market activity; not a full global cross-rate feed or a guaranteed customer-executable quote.
- **FXAPI free tier:** a possible convenience source for daily historical/mid-market data and matrix calculations, subject to its published terms and data-source limitations.
- **Executable quote sources:** not yet selected. This remains a separate research task.

## 2. Source screening

### A. European Central Bank (ECB)

Link: https://data.ecb.europa.eu/methodology/exchange-rates

The ECB explains that reference rates are published on working days, normally around 16:00 CET. Its euro reference rates are informational averages of buying and selling rates and do not necessarily represent prices at which transactions occurred or could be conducted.

**Useful for**
- Daily historical comparisons for supported currencies.
- Constructing a coherent reference-rate cross-rate network around EUR.
- Descriptive analysis and checking arithmetic/data transformations.

**Not sufficient for**
- Intraday triangular arbitrage.
- Reconstructing executable bid/ask spreads.
- Assuming a user can transact at the reference rate.

**Initial judgement:** Strong candidate for official reference-data validation, not for execution claims.

### B. Bank of Canada

Links:
- https://www.bankofcanada.ca/rates/exchange/daily-exchange-rates/
- https://www.bankofcanada.ca/rates/exchange/background-information-on-foreign-exchange-rates/

The Bank of Canada provides daily, monthly and annual exchange-rate data, with CSV, JSON and XML formats available through its data services. Its published rates are indicative rates derived from aggregated financial-institution price quotes. The bank explicitly warns that they may not reflect rates at which transactions were or could be conducted.

**Useful for**
- A second official source for historical cross-checking.
- Multi-currency daily reference-rate research.
- Testing whether the same broad movement appears in another independently published dataset.

**Limitations**
- Indicative rather than executable bid/ask data.
- Rates are expressed as foreign currency units converted into Canadian dollars; transformations must preserve quote direction.
- Publication frequency and timing are not designed to detect fleeting arbitrage.

**Initial judgement:** Strong candidate for a second reference series and quote-convention checks.

### C. Central Bank of Nigeria (CBN), NFEM

Link: https://www.cbn.gov.ng/rates/ExchRateByCurrency.html

The CBN page publishes Nigerian Foreign Exchange Market (NFEM) rates for naira per US dollar and includes fields such as high, low, closing and simple average rates, plus market turnover/deal information. Its page describes the NFEM rate as derived from volume-weighted average market activity and as the official rate for the day.

**Useful for**
- Nigeria-specific official-market context.
- Examining USD/NGN reference-rate changes and published market activity.
- Building a Nigeria-focused question register about market structure and access.

**Limitations**
- It does not by itself provide simultaneous bid/ask quotes for the complete set of global currency pairs.
- The published official daily rate should not be assumed to be the price offered to a particular retail customer or SME.
- It is not sufficient to test a global three-currency executable loop.

**Initial judgement:** Relevant to the Nigeria lens, but not the sole FX dataset.

### D. FXAPI free tier (commercial provider)

Links:
- https://fxapi.com/free-exchange-rate-api/
- https://fxapi.com/

The provider advertises a free plan with a limited monthly request allowance, historical daily exchange rates and cross-rate/matrix endpoints. Its product information describes the data as mid-market reference rates and explicitly excludes bid/ask spreads and trade execution.

**Useful for**
- Quick programmatic prototypes and multi-currency matrix calculations.
- Comparing a convenience dataset against official reference data.
- Testing a simple ingestion process without initially paying for data.

**Limitations and checks before use**
- It is a third-party data provider, not an official central bank.
- Mid-market data cannot establish executable arbitrage.
- Verify current free-tier quotas, historical coverage, licensing, terms of use, source methodology, timestamps and supported currencies before relying on it.
- Do not commit to a paid tier before proving that the missing data is worth paying for.

**Initial judgement:** Candidate for convenience/prototyping only, with source cross-checking.

## 3. Fit-for-purpose matrix

| Research question | ECB | Bank of Canada | CBN NFEM | FXAPI free |
|---|---|---|---|---|
| Hand-check cross-rate arithmetic | Yes | Yes | Limited to available series | Yes |
| Daily historical descriptive analysis | Yes | Yes | Yes, for published NGN/USD series | Advertised |
| Global multi-currency reference network | Partial, supported currencies | Partial, supported currencies | No, not by itself | Advertised |
| Time-aligned executable bid/ask loop | No | No | No, not from the daily page alone | No |
| Nigeria official-market context | Limited | Limited | Yes | Depends on supported data and methodology |
| Proof of a tradeable profit | No | No | No | No |

"Yes" here means potentially fit for the stated reference-data task, subject to field availability and data-quality checks; it does not imply that a complete validated dataset has already been downloaded or audited.

## 4. Proposed staged data design

### Dataset 1 — Daily reference rates
Fields:
- observation date and published timestamp if available
- source and source series ID
- base currency and quote currency
- rate and units
- rate type (reference, indicative, mid, bid, ask, close, etc.)
- methodology and source link
- missing/holiday flag
- ingestion timestamp and transformation notes

Use this dataset for cross-rate calculations and broad economic relationships, clearly labelled as reference data.

### Dataset 2 — Executable quote observations
Required fields:
- precise timestamp and timezone
- provider/venue and instrument
- pair, base and quote currency
- bid and ask
- quote size/tier and whether the quote is firm or indicative
- fees, commissions and conversion charges
- eligibility and availability to the intended customer
- quote expiry, execution/settlement conditions and evidence link

This dataset is required before any claim of executable triangular arbitrage can be tested credibly.

### Dataset 3 — Economic variables (later stage)
- central-bank policy rates and dated decisions
- market yields where suitable
- inflation, employment, growth and trade releases
- commodity series relevant to a stated hypothesis
- event timestamp, release value, consensus expectation if reliably sourced, and revisions

Every series must record units, frequency, release timestamp, revision policy and source.

## 5. Methodological warning

Reference-rate networks can demonstrate mathematical relationships and support historical analysis, but they can also produce misleading "opportunities" if source rates are published at different times, use different calculation methods, or are not executable. For real arbitrage, the prices must be simultaneously available, correctly sided (bid/ask), sufficiently large for the intended trade, accessible to the same actor, and profitable after all costs and operational constraints.

A historical predictive strategy is a different claim from arbitrage. It requires a pre-specified signal, an appropriate benchmark, chronological out-of-sample testing, realistic costs and risk reporting.

## 6. Next actions

1. Obtain a small sample of ECB and Bank of Canada daily series for the initial core currencies.
2. Compare overlapping dates and verify pair orientation and cross-rate calculations independently.
3. Check what currencies and history are available from the CBN page and record any extraction limitations.
4. Inspect FXAPI documentation and sample responses only if needed for convenient matrix retrieval; verify licensing and data definitions first.
5. Keep a separate investigation open for accessible, time-stamped executable bid/ask quotes, including whether any such source is legally and practically accessible from Nigeria.
6. Update the source register with tested coverage, actual fields, missingness, and provenance once sample data is inspected.

## 7. Evidence references

- ECB exchange-rate methodology: https://data.ecb.europa.eu/methodology/exchange-rates
- Bank of Canada daily exchange rates: https://www.bankofcanada.ca/rates/exchange/daily-exchange-rates/
- Bank of Canada methodology and limitations: https://www.bankofcanada.ca/rates/exchange/background-information-on-foreign-exchange-rates/
- CBN exchange rates / NFEM: https://www.cbn.gov.ng/rates/ExchRateByCurrency.html
- FXAPI free exchange-rate API: https://fxapi.com/free-exchange-rate-api/
- FXAPI general product description: https://fxapi.com/

This assessment is a first-pass desk review of the linked pages. Before building on a source, verify current terms, download a sample, inspect fields and compare it against an independent source.

## 8. Change history

- **2026-10-27:** Initial screening of candidate official and low-cost reference-rate sources. No executable bid/ask data source selected; no arbitrage opportunity established.

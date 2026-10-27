# Research Log

## 2026-10-13 — Initial workspace
- **Goal:** Establish durable records for the Economic State Transition Model.
- **Completed:** Project overview, current state, methodology, decision register, and measurement templates.
- **Key result:** The next research task is to operationally define Real GDP growth.
- **Open questions:** Initial test economy; preferred data source; frequency and historical window.
- **Next action:** Specify Indicator 1 before collecting observations for classification.

## 2026-10-27 — FX Opportunity Intelligence Programme initiated
- **Workstream:** E — Opportunity Intelligence and Economic Application.
- **Goal:** Establish a durable, broad investigation plan for foreign-exchange opportunities before committing to a trading strategy or risking capital.
- **Completed:** Added `workstream-e/fx/FX-OPPORTUNITY-INTELLIGENCE-PROGRAMME.md` and updated `CURRENT-STATE.md`.
- **Scope:** Mathematical cross-rate/network consistency; economic connections and transmission; information/event timing; conversion frictions and market access; fully funded currency rotation; broker-based FX products as a separate track; and potential FX intelligence products/services.
- **Decision principle:** Global investigation with Nigeria-specific access and business questions; public/historical data and simulations first; no use of the available $20 for initial tests.
- **Current evidence status:** Programme plan only. No executable arbitrage, predictive pattern, trading strategy or commercial service has been validated.
- **First practical task:** Specify and hand-check a three-currency cross-rate calculation, then define the data needed to evaluate bid/ask executable discrepancies.
- **Open questions:** Reliable low-cost historical bid/ask data; quote conventions and timestamps; realistic costs and provider access; measurable economic mechanisms; customer-validated FX problems.
- **Next action:** Build the first cross-rate calculation specification and source register, then record the initial evidence and results in the FX programme folder.

## 2026-10-27 — FX cross-rate consistency exercise 001
- **Goal:** Validate quote conventions and calculation steps before using real market observations.
- **Completed:** Added `workstream-e/fx/FX-CROSS-RATE-EXERCISE-001.md` with synthetic EUR/USD, USD/JPY and EUR/JPY quotes, implied midpoint calculation, both executable loop directions and a minimum real-quote data schema.
- **Result:** Synthetic implied EUR/JPY midpoint was approximately 164.9600 versus a direct midpoint of 165.10. When bid/ask sides were used for each loop, USD 1 returned approximately USD 0.999818 in one direction and USD 0.998125 in the other, before additional fees. Neither loop was profitable in this example.
- **Evidence status:** Calculation method demonstrated with invented data only. No current market discrepancy or trading opportunity was tested.
- **Key lesson:** A midpoint discrepancy is not proof of executable arbitrage; quote direction, bid/ask, timestamps, transaction size, provider access and all costs matter.
- **Next action:** Assess accessible historical FX data sources and determine whether they provide bid/ask quotes, timestamps and sufficient pair coverage. Keep reference/mid data distinct from executable quotes.

## 2026-10-27 — FX data source assessment 001
- **Goal:** Identify accessible historical reference data for cross-rate and network tests while preserving the distinction between reference rates and executable quotes.
- **Completed:** Added `workstream-e/fx/FX-DATA-SOURCE-ASSESSMENT-001.md`, screening ECB, Bank of Canada, CBN NFEM and FXAPI.
- **Initial judgement:** ECB and Bank of Canada are candidates for official daily reference-rate analysis; CBN NFEM is useful for Nigeria-specific official-market context; FXAPI may be convenient for low-cost prototyping but provides mid-market reference data, not executable bid/ask quotes.
- **Key limitation:** These sources, as reviewed, do not establish executable triangular arbitrage. Real execution analysis requires time-aligned bid/ask quotes, trade size, access conditions and all-in costs.
- **Evidence status:** Desk review of source descriptions only; sample data have not yet been ingested or independently reconciled.
- **Next action:** Inspect a small overlapping sample of reference rates, verify pair orientation and cross-rate formulas, and separately investigate whether accessible executable bid/ask data can be obtained lawfully from Nigeria.

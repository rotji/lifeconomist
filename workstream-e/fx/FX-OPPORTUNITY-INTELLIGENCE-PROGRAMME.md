# Foreign-Exchange Opportunity Intelligence Programme

**Programme ID:** E-FX-001  
**Workstream:** E — Opportunity Intelligence and Economic Application  
**Status:** Approved investigation plan; no FX opportunity or strategy validated  
**Created:** 2026-10-27  
**Scope:** Global FX markets, with Nigeria-specific access, conversion and business-use cases included from the beginning  
**Capital constraint:** Initial research and testing should not require risking the user's available $20. Use public data, historical analysis, spreadsheets and simulation first.

## 1. Purpose

Investigate the foreign-exchange (FX) system broadly enough to discover, verify, compare and test potential opportunities to create or capture economic value. The programme must not assume that a pattern is profitable merely because it is mathematically interesting, historically visible, or widely discussed.

The work covers both:
- **Trading/investment hypotheses:** potential opportunities from prices, currency movements, information, relationships and market structure.
- **Commercial/intelligence hypotheses:** services that help individuals or businesses understand currency exposure, compare lawful conversion options, reduce avoidable costs, monitor relevant developments or make better FX decisions.

The programme is research-first. No real-money trade is required to begin.

## 2. Core research question

Can we use mathematical relationships, economic mechanisms, observable information, market frictions and customer problems to identify an FX opportunity that is (a) demonstrable, (b) accessible, (c) economically meaningful after costs and risks, and (d) testable with limited resources?

Every candidate must end in one of these states:
- **Unexamined lead**
- **Observed phenomenon**
- **Hypothesis formulated**
- **Evidence gathered**
- **Test in progress**
- **Supported within stated limits**
- **Rejected / not supported**
- **Deferred for missing data or access**
- **Commercially promising but not validated**

Do not label an opportunity "profitable" or "validated" without an explicit test, cost treatment, suitable comparison and out-of-sample or forward validation appropriate to the claim.

## 3. Research tracks

The tracks run concurrently and may inform one another. Their different mechanics and claims must not be conflated.

### Track A — Mathematical relationships and pricing consistency

Investigate:
1. Bilateral exchange rates and quote conventions.
2. Implied cross-rates calculated from two other pairs.
3. Triangular currency loops and their theoretical consistency.
4. Larger currency networks and overlapping loops.
5. Bid/ask differences, quote timestamps, stale data and source incompatibility.
6. Provider/venue differences and whether a price is actually executable.
7. Net returns after spreads, fees, transfer costs, slippage, latency, limits and settlement constraints.

**Central distinction:** A cross-rate discrepancy is an observation; an executable arbitrage opportunity is a stronger claim. Never calculate a tradable profit using mid-prices alone when executable bid/ask quotes are needed.

For currencies A, B and C, define quote direction explicitly before calculating a loop. Keep units visible and verify the multiplication/division direction with a simple test. For an exchange-rate network, a closed loop should return to the starting currency at the same value in a perfectly consistent frictionless system. Real-world costs generally make small discrepancies non-exploitable.

### Track B — Economic connections and transmission mechanisms

Test relationships involving:
1. Central-bank policy and expected policy paths.
2. Nominal yields, real yields, rate differentials and carry.
3. Inflation, inflation surprises and purchasing-power measures.
4. Employment, growth, productivity, fiscal and trade data.
5. Commodities and currencies exposed to commodity exports/imports.
6. Global dollar funding, liquidity, credit conditions and risk appetite.
7. Portfolio flows, debt service, foreign borrowing and capital allocation.
8. Geopolitical events, sanctions, tariffs, intervention and capital controls.
9. Currency regimes: floating, managed, pegged and restricted markets.
10. Market positioning and expectations where reliable public evidence exists.

For each relationship, state the proposed mechanism, direction (if hypothesized), lag, time horizon, conditions where it may fail, alternative explanations and evidence that would disconfirm it. Correlation is not proof of causation, and relationships may change across regimes.

### Track C — Information timing and event studies

Investigate currency responses to:
- Central-bank decisions and forward guidance.
- Inflation, labour, growth and trade releases.
- Revisions to economic data.
- Fiscal, regulatory, geopolitical and trade-policy announcements.
- Unexpected shocks and changes in market expectations.

Record event time, the expected result where reliably available, actual result, surprise measure, instrument, pre-event price, immediate reaction and subsequent changes at pre-defined horizons. Avoid look-ahead bias, survivorship bias and choosing the event window only after seeing the result. Compare results with a baseline and account for transaction costs before proposing a strategy.

### Track D — Market access and real-world currency friction

Investigate:
- Customer-facing conversion quotes and spreads.
- Fees, minimum charges, limits and hidden conversion steps.
- Availability and eligibility for each currency.
- Transfer/settlement time, failed transfers and counterparty/custody risk.
- Difference between official/reference rates, indicative quotes and executable rates.
- Lawful access from Nigeria and relevant provider terms or regulatory restrictions.
- Currency needs of importers, exporters, travellers, students, remote workers and other potential users, without assuming these groups have a validated unmet need.

Do not treat an official or reference rate as a rate a specific person can necessarily obtain. Provider comparisons must record quote time, direction (buy/sell), amount, fees, eligibility, settlement and evidence source. Do not recommend evading capital controls, KYC, sanctions or other legal restrictions.

### Track E — Fully funded currency holding and rotation

This track examines a strategy where the user actually holds a currency-denominated balance or cash and exchanges it into another currency, without leverage. Example hypothesis: rotate between currencies based on relative strength over a 2–3 day horizon.

Test:
- Whether the balance is genuinely denominated in the currency and withdrawable as such.
- Currency-pair selection and decision rule.
- Entry/exit timing and how a signal is formed using only information available at that time.
- Total conversion cost in both directions and any custody/transfer/minimum fees.
- Performance against holding the starting currency and simple baselines.
- Drawdowns, adverse moves, frequency of switching and sensitivity to costs.
- Whether the strategy works out of sample and in different market conditions.

Do not assume frequent switching is advantageous. With small balances, fixed fees and spreads can dominate the result. Begin with a historical or paper ledger, not live transactions.

### Track F — Broker-based FX products and trading

Keep this distinct from Track E. Before evaluating any broker strategy, identify the exact instrument and contract: for example, a CFD, rolling spot product or another derivative. Verify jurisdictional availability, contract specifications, leverage, margin, liquidation rules, spreads, commissions, overnight financing, execution, withdrawal rules and counterparty/regulatory status.

A forecast about the underlying currency does not by itself establish that a broker trade is suitable or profitable. Model leverage and losses explicitly. Do not place real-money trades during initial research; do not use borrowed funds or treat the user's $20 as a requirement to trade.

### Track G — FX intelligence products and business opportunities

Investigate potential customer problems such as:
- Monitoring FX conversion costs for a defined business use case.
- Alerts for exchange-rate, policy or supplier-currency changes.
- Currency exposure and scenario analysis for businesses.
- Provider/route comparison where data and lawful access permit.
- FX event briefs or decision-support research for a defined customer segment.
- Data-quality, quote-comparison or cross-rate monitoring tools.

For each candidate, identify a specific customer, the decision/problem, existing alternatives, how often the problem occurs, cost of the problem, evidence that the customer would use the service, willingness to pay, delivery effort, data licensing and liability risks. A useful analysis is not automatically a viable business; customer discovery or a paid pilot is needed.

## 4. Currency-network model

Use a network perspective, but distinguish the following:
- **Nodes:** currencies or, where needed, currency instruments/accounts.
- **Edges:** quoted exchange rates, each with quote direction, timestamp, source, bid, ask, units and access conditions.
- **Loops:** closed conversion paths used to test mathematical consistency.
- **Economic links:** hypotheses about common drivers or transmission between currencies.
- **Market-access links:** actual providers and routes available to a defined user.
- **Customer links:** entities with currency exposure or a decision problem.

For n currencies, there are n(n-1)/2 possible unique bilateral pairs if every pair is available. This combinatorial count is not a claim that all pairs are liquid or directly tradable. A currency network can be analysed as a whole; it is not necessary to enumerate every possible subset manually. Begin with a small core group, validate data and methods, then expand.

Initial research universe (subject to data quality): USD, EUR, JPY, GBP, CHF, CAD, AUD and CNY. Expand to additional currencies based on a specific hypothesis and available reliable data. Treat CNY onshore/offshore and other restricted or segmented markets carefully; instruments that look similar may not be interchangeable.

## 5. Nigeria-specific lens

Nigeria is an initial test case, not a limit on global scope. Examine:
- Official/reference market data versus customer-executable rates.
- Legal and practical access to conversion providers and currency balances.
- Provider spreads, fees, transfer rails, availability and settlement.
- Import/export and other business exposures where evidence supports a real problem.
- The difference between formal market quotes and any other observed price series; document definitions, legality, access and comparability before comparing them.

Potential starting sources include the Central Bank of Nigeria (CBN) for official market information and the Bank for International Settlements (BIS) for global FX market structure. Other sources may include national central banks, statistical agencies, official release calendars, reputable historical market-data providers and provider fee schedules. Record source, URL, timestamp/date accessed, units, methodology and limitations for every important claim. No source is assumed sufficient for all tracks.

## 6. Initial investigation phases

### Phase 0 — Set up the research record
- Preserve this programme plan in GitHub.
- Maintain a question register, hypothesis register, source register, experiment log and decision log.
- Label each statement as observation, source-backed fact, inference, hypothesis or decision.

### Phase 1 — Establish a mathematical baseline
- Define quote conventions and calculate cross-rates for a small currency group.
- Build hand-checkable examples before automating.
- Determine what fields are required to test executable rather than theoretical arbitrage.
- Record what the available data can and cannot establish.

### Phase 2 — Build an economic relationship map
- Select a small number of explicit mechanisms.
- Define measurable variables, data frequency, lags and horizons.
- Explore relationships descriptively before testing predictive claims.
- Keep hypotheses and outcome periods separate to reduce overfitting.

### Phase 3 — Test timing and strategy hypotheses
- Predefine signal, entry, exit, holding period, benchmark and costs.
- Use chronological training/test separation or walk-forward tests where suitable.
- Include no-trade and simple baseline comparisons.
- Report failures, missing data and negative results, not only successful cases.

### Phase 4 — Measure execution and customer friction
- Collect time-stamped, comparable provider quotes only where legitimately accessible.
- Calculate all-in conversion costs for explicit amounts and directions.
- Investigate customer problems separately from proprietary trading hypotheses.

### Phase 5 — Evaluate and decide
- Compare opportunities by evidence, net economics, access, risks, capital requirements, repeatability and customer value.
- Choose only the next experiment justified by the evidence.
- Keep the user's $20 untouched unless a separate, explicit decision is made after paper testing and costs/risk are understood.

These phases are an ordering for dependable work, not a rigid waterfall. A strong lead from any track may justify moving directly to a small test while other tracks continue.

## 7. Standard hypothesis record

For every candidate, record:
- **ID and title**
- **Track(s)**
- **Date raised**
- **Observation and source**
- **Hypothesis**
- **Proposed mechanism**
- **Currency pair(s), instrument/provider and quote direction**
- **Time horizon**
- **Data required and known limitations**
- **Test design and benchmark**
- **All costs and execution assumptions**
- **Risk, confounders and disconfirming evidence**
- **Results, including negative or inconclusive outcomes**
- **Status**
- **Decision and next step**
- **Links to related findings and relevant Workstreams A–D**

## 8. Opportunity evaluation scorecard

Do not collapse the scorecard into a false-precision single number. Assess each dimension qualitatively with supporting evidence:
1. Existence: is the phenomenon observed?
2. Mechanism: is there a plausible, testable explanation?
3. Data quality: are the observations fit for this claim?
4. Access: can the intended user lawfully and practically act?
5. Net economics: what remains after all material costs?
6. Robustness: does the result persist out of sample or across conditions?
7. Downside: what losses, operational failures or legal risks are possible?
8. Resource fit: can it be tested with current time, tools and capital?
9. Commercial value: is there an identifiable customer and demonstrated need?
10. Falsifiability: what result would make us reject the hypothesis?

## 9. Operating rules

- Explore all major tracks in parallel, but work on a small number of explicit questions at a time.
- Separate global market findings from Nigeria-specific execution claims.
- Separate actual currency ownership/rotation from broker derivatives.
- Distinguish reference, indicative, mid, bid and ask prices.
- Include transaction costs, slippage, timing, settlement and access in any net-profit claim.
- Avoid hindsight, look-ahead bias, cherry-picked windows and overfitting.
- Do not invent data, prices, provider access or returns.
- Use public and low-cost data first; avoid paid data until its value is demonstrated.
- No live trading is needed to make progress.
- Preserve negative findings and revise hypotheses rather than hiding failed tests.
- Feed relevant learning back to Workstreams A (concepts), B (measurement), C (monitoring) and D (footprint intelligence).
- Only promote an idea to a recommendation when evidence supports the exact claim and its stated limitations.

## 10. Initial open questions

1. Which historical FX datasets provide consistent timestamps, bid/ask data and broad pair coverage at no cost or low cost?
2. Which cross-rate calculations can be independently hand-verified?
3. Which apparent discrepancies are caused by quote conventions, timing, source mismatch or non-executable rates?
4. Which economic mechanisms are most measurable with public data and clear hypotheses?
5. Can any 2–3 day currency-rotation rule outperform a sensible baseline after realistic costs?
6. What real FX conversion problem can a Nigerian individual or SME verify and quantify?
7. Which potential intelligence output would materially improve a specific customer's decision?
8. Which data or execution gaps are genuinely blocking, and which can be handled with a simple spreadsheet or manual observation?

## 11. First practical task

Begin with a **cross-rate consistency notebook or spreadsheet specification**, not a trading bot:
- Choose three currencies and explicitly define quote direction.
- Calculate the implied third cross-rate.
- Add bid/ask and timestamp fields to the data schema.
- Demonstrate the calculation with synthetic values clearly labelled as examples.
- List the additional evidence needed before calling any difference executable.
- Then extend to a small multi-currency network and record the first evidence-backed result.

This is a method-validation exercise. Synthetic examples establish calculation logic only; they are not evidence of a current market opportunity.

## 12. Source and evidence starting points

- Central Bank of Nigeria (CBN): https://www.cbn.gov.ng/
- CBN exchange-rate information: https://www.cbn.gov.ng/rates/ExchRateByCurrency.html
- Bank for International Settlements (BIS): https://www.bis.org/
- BIS foreign exchange statistics and Triennial Survey: https://www.bis.org/statistics/rpfx22.htm

Verify the current page, relevant date, definitions and data availability before using any source in a specific finding. Update this list as sources are assessed; inclusion here does not imply that every source supports every claim.

## 13. Change history

- **2026-10-27:** Initial programme specification created. All tracks are research directions; no FX opportunity or strategy has been validated.
- **2026-10-27:** Added [FX Cross-Rate Exercise 001](FX-CROSS-RATE-EXERCISE-001.md), a synthetic worked example showing implied cross-rate calculation and both bid/ask conversion-loop directions. No live-market opportunity was established.

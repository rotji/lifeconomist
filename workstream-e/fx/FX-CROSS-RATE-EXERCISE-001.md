# FX Cross-Rate Exercise 001 — Three-Currency Consistency

**Programme:** E-FX-001  
**Workstream:** E — Opportunity Intelligence and Economic Application  
**Date:** 2026-10-27  
**Status:** Calculation method demonstrated with synthetic data; no live-market conclusion  
**Purpose:** Establish a transparent, hand-checkable method for implied cross-rates and executable triangular conversion loops before gathering real quotes.

## 1. Research question

Given quotes for EUR/USD, USD/JPY and EUR/JPY, are the quotes mathematically consistent, and does either direction of a three-currency conversion loop produce more of the starting currency after crossing the quoted bid/ask prices?

This exercise validates the calculation procedure only. The prices below are invented examples, not live quotes or claims about current market conditions.

## 2. Quote conventions

For this exercise:
- **EUR/USD** means USD per EUR. A quote of 1.1000 means one euro is worth 1.1000 US dollars.
- **USD/JPY** means JPY per USD.
- **EUR/JPY** means JPY per EUR.
- **Bid** is the price at which the quote provider buys the base currency from the customer.
- **Ask** is the price at which the quote provider sells the base currency to the customer.
- A customer buying the base currency pays the ask; a customer selling the base currency receives the bid.

Always verify quote conventions and provider definitions in real data before calculating.

## 3. Synthetic input quotes

| Pair | Bid | Ask | Midpoint |
|---|---:|---:|---:|
| EUR/USD | 1.1000 | 1.1002 | 1.1001 |
| USD/JPY | 149.90 | 150.00 | 149.95 |
| EUR/JPY | 165.00 | 165.20 | 165.10 |

All three quotes are assumed to be simultaneous and available from one hypothetical provider solely for this worked example. Real comparisons must verify timestamps, venue/provider, trade size, eligibility and executability.

## 4. Calculate the implied cross-rate

Because EUR/USD is USD per EUR and USD/JPY is JPY per USD, multiplying cancels USD:

`(USD/EUR) × (JPY/USD) = JPY/EUR`

Using midpoints:

`Implied EUR/JPY = 1.1001 × 149.95 = 164.959995 JPY per EUR`

The direct EUR/JPY midpoint is:

`(165.00 + 165.20) / 2 = 165.10 JPY per EUR`

The direct midpoint is therefore about 0.140005 JPY per EUR above the implied midpoint, or approximately 0.0849% relative to the implied midpoint.

**Interpretation:** this is a midpoint difference in a synthetic example. It is not, by itself, an arbitrage opportunity. Midpoints are not necessarily executable, and the difference may be smaller than the costs of trading through the bid and ask.

## 5. Test both executable loop directions

Start with USD 1.00. Ignore any additional commission or transfer fee for the moment; the bid/ask prices already create a spread cost. This is still only a simplified synthetic calculation.

### Loop A — USD → EUR → JPY → USD

1. Buy EUR with USD at the EUR/USD ask: `EUR = 1 / 1.1002`.
2. Sell EUR for JPY at the EUR/JPY bid: `JPY = (1 / 1.1002) × 165.00`.
3. Buy USD with JPY at the USD/JPY ask: `USD final = 165.00 / (1.1002 × 150.00)`.

Final amount:

`USD final ≈ 0.9998182`

Return on the starting USD 1:

`(0.9998182 − 1) × 100 ≈ −0.01818%`

### Loop B — USD → JPY → EUR → USD

1. Sell USD for JPY at the USD/JPY bid: `JPY = 149.90`.
2. Buy EUR with JPY at the EUR/JPY ask: `EUR = 149.90 / 165.20`.
3. Sell EUR for USD at the EUR/USD bid: `USD final = (149.90 / 165.20) × 1.1000`.

Final amount:

`USD final ≈ 0.9981253`

Return on the starting USD 1:

`(0.9981253 − 1) × 100 ≈ −0.18747%`

### Result of this example

Neither direction returns more than the starting USD amount before any additional fees. The midpoint discrepancy did not translate into a profitable executable loop under these assumed bid/ask quotes.

This demonstrates why we must evaluate both directions with the correct bid/ask side rather than infer profits from midpoint differences.

## 6. What this result establishes — and what it does not

**Established by the worked calculation**
- Quote units and direction determine whether rates multiply or divide.
- Two rates can be combined to derive an implied third cross-rate.
- A direct midpoint can differ from an implied midpoint.
- Bid/ask spreads can eliminate an apparent discrepancy.
- The loop should be calculated in both directions using executable sides.

**Not established**
- That a current FX market has an exploitable discrepancy.
- That all three quotes are available simultaneously to one customer.
- That a provider will accept the relevant transaction sizes and complete all legs at the displayed prices.
- That execution latency, slippage, fees, limits, settlement and counterparty risk are negligible.
- That this method predicts future currency movements.

## 7. Minimum real-quote data schema

For each quote, capture:

| Field | Why it matters |
|---|---|
| Observation ID | Unique record identifier |
| Timestamp with timezone | Check simultaneity and staleness |
| Provider / venue | Identify where the quote is available |
| Instrument / pair | Identify the quoted currencies and instrument |
| Base currency | Avoid quote-direction errors |
| Quote currency | Define the price units |
| Bid | Customer's executable sell side, subject to provider convention |
| Ask | Customer's executable buy side, subject to provider convention |
| Quote size / tier | Prices can depend on transaction size |
| Fees and other charges | Calculate all-in economics |
| Customer eligibility / location | Confirm access from the user's jurisdiction |
| Firm or indicative status | An indicative quote may not be executable |
| Expiry / validity | Determine whether the quote is still live |
| Settlement / transfer constraints | Capture practical execution conditions |
| Evidence link or screenshot reference | Allow independent verification |

Use a consistent timestamp and provider where possible. If comparing across providers, record each provider's quote time and terms; do not silently assume quotes can be executed simultaneously.

## 8. Next investigation

1. Identify accessible sources of historical FX rates and determine whether they supply bid/ask prices or only reference/mid rates.
2. Determine whether time-stamped executable quotes can be collected lawfully and consistently from providers accessible to a customer in Nigeria.
3. Create a small spreadsheet with explicit quote conventions, formulas for implied rates, both loop directions and transaction costs.
4. Test with real observations only when the source fields support the intended claim.
5. Record the first real-data finding as supported, rejected or inconclusive. Do not convert a synthetic calculation into a market finding.

## 9. Evidence classification

- **Method:** Demonstrated with arithmetic and synthetic input.
- **Market observation:** None in this exercise.
- **Opportunity claim:** None.
- **Next step:** Data-source assessment and real-quote schema validation.

## 10. Change history

- **2026-10-27:** Initial worked example created. Synthetic quotes only; both conversion loops return less than the starting amount before additional fees.

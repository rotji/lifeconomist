# Depth Audit — Workstream A Groups 22–24

**Date:** 2026-10-30  
**Scope:** Bullet-by-bullet review of Groups 22–24 against Concepts 29–31 and related notes.  
**Purpose:** Verify conceptual coverage, strengthen specific explanatory gaps in existing notes, and keep measurement, temporal inference and distributional incidence distinct from unsupported claims about current events or named actors.

## 1. Status definitions

- **Explicitly covered:** The note directly explains the topic and its main boundaries.
- **Partially covered:** The topic appears but an important mechanism, test or boundary needs clarification.
- **Cross-linked:** Another concept is the primary home; use a cross-link rather than duplicating it.
- **Not yet covered:** No adequate treatment was found in the reviewed notes.

## 2. Group 22 — Economic measurement, evidence and inference

**Primary note:** [Concept 29 — Economic Measurement, Evidence and Inference](concepts/economic-measurement-evidence-and-inference.md). Related concepts include Concepts 13, 19, 26 and 30; formal indicator definitions remain in Workstream B.

| Roadmap bullet | Status | Evidence and boundary |
|---|---|---|
| Concepts versus indicators versus proxies | Explicitly covered | Concept 29 distinguishes constructs, variables, measures, indicators, proxies, estimates and targets. A proxy is not automatically a valid substitute for the construct. |
| Operational definitions, units and denominators | Explicitly covered | Concept 29 requires the target population/entity, geography, period, unit, denominator and inclusion rules to be specified. |
| Stocks, flows, rates, ratios and indices | Explicitly covered | Concept 29 distinguishes quantities measured at a point in time from quantities over a period and from derived ratios or indices. |
| Nominal/real, gross/net and per-capita measures | Explicitly covered | Concept 29 explains price adjustment, gross/net boundaries and aggregate versus per-capita interpretations. |
| Measurement error, missingness and revisions | Explicitly covered | Concept 29 covers missingness, survivorship, revisions and the need to preserve historical vintages where decision-time information matters. |
| Comparability, classification and methodology changes | Explicitly covered | Concept 29 identifies classification, methodology, deflator, coverage and definition changes that can break comparisons. |
| Correlation, causation, mechanisms and confounding | Explicitly covered | Concept 29 distinguishes association, plausible mechanisms, prediction and causal inference; it identifies confounding and reverse causality. |
| Leading, coincident and lagging indicators | Explicitly covered / cross-linked | Concept 29 introduces indicator timing; Concept 30 develops timing, lags and real-time evaluation. A leading relationship alone does not establish reliable prediction. |
| Uncertainty, confidence, sensitivity and triangulation | Explicitly covered | Concept 29 separates data quality from claim confidence and explains source dependence, uncertainty and triangulation. |
| Model risk, overfitting and limits of inference | Explicitly covered | Concept 29 addresses models, composite scores, overfitting and inferential limits. |
| Alert thresholds, false alarms and missed events | **Strengthened by targeted addition** | New subsection defines false positives/negatives, sensitivity, precision and specificity, explains rare-event alert limits and connects threshold choice to error costs. |

### Group 22 conclusion

Group 22 is conceptually covered, with a targeted addition on alert error metrics and decision thresholds. Remaining work is implementation-specific: define each target event, label and evaluation window; preserve decision-time data; test outside the tuning sample; compare against a baseline; and choose thresholds in light of false-alarm and missed-event costs. The concept note does not substitute for a formal indicator specification or validation report.

## 3. Group 23 — Time, cycles and economic transmission

**Primary note:** [Concept 30 — Time, Cycles and Economic Transmission](concepts/time-cycles-and-economic-transmission.md). Related concepts include Concepts 13, 16–18, 21, 24 and 29.

| Roadmap bullet | Status | Evidence and boundary |
|---|---|---|
| Short-run fluctuations versus long-run trends | Explicitly covered | Concept 30 distinguishes cycles, trends, seasonality, one-off shocks and structural breaks. |
| Business cycles and financial cycles | Explicitly covered | Concept 30 explains possible macro-financial feedbacks without treating cycles as fixed or inevitable laws. |
| Lags, leads, timing and expectations | Explicitly covered | Concept 30 distinguishes different time stamps, lag types, anticipation and adjustment delays. |
| Feedback loops, amplification and dampening | Explicitly covered | Concept 30 explains reinforcing and balancing loops and how delays can change their behavior. |
| Stocks, flows, accumulation and adjustment | Explicitly covered | Concept 30 explains stock-flow timing and adjustment processes. |
| Monetary, fiscal, credit and exchange-rate transmission | Explicitly covered | Concept 30 maps potential channels; an illustrative path is not proof that a particular policy caused an observed outcome. |
| Shocks, propagation, adaptation and persistence | Explicitly covered | Concept 30 covers exposure, propagation and recovery, with attention to alternative explanations. |
| Cyclical versus structural pressures | Explicitly covered | Concept 30 distinguishes temporary fluctuations from persistent changes and measurement breaks. |
| Hysteresis, scarring and path dependence | Explicitly covered | Concept 30 explains how temporary shocks can leave lasting effects through skills, investment, balance sheets and institutional adjustment. |
| Forecasts, scenarios and future uncertainty | **Real-time validation strengthened by targeted addition** | New subsection explains data leakage, chronological evaluation, realistic information sets, baseline comparisons and the need to assess false alarms, missed events and lead time. |

### Group 23 conclusion

Group 23 is conceptually covered, with a targeted addition on real-time forecast evaluation and data leakage. Remaining work is to preserve publication dates and historical data vintages, define the actual decision-time information set, use appropriate chronological or rolling evaluation, compare against simple baselines and assess stability across periods. A variable preceding another does not automatically forecast it reliably or cause it.

## 4. Group 24 — Distribution of economic power and opportunity

**Primary note:** [Concept 31 — Distribution of Economic Power and Opportunity](concepts/distribution-of-economic-power-and-opportunity.md). Related concepts include Concepts 6, 12, 15, 20, 23 and 26.

| Roadmap bullet | Status | Evidence and boundary |
|---|---|---|
| Income distribution versus wealth distribution | Explicitly covered | Concept 31 separates flows of income from accumulated assets and liabilities. |
| Ownership versus control versus influence | Explicitly covered | Concept 31 distinguishes legal title, operational authority, voting rights, influence, benefit and risk. |
| Bargaining, market and institutional power | Explicitly covered | Concept 31 distinguishes negotiation leverage from market-wide power and institutional authority. Concentration is a reason to investigate, not proof of abuse. |
| Access to credit, markets, information and infrastructure | Explicitly covered | Concept 31 distinguishes nominal availability from usable access, affordability, reliability and practical ability to benefit. |
| Economic inclusion, exclusion and segmentation | Explicitly covered | Concept 31 explains barriers, segmentation and unequal practical options. |
| Rent extraction, economic rents and productive returns | Explicitly covered | Concept 31 distinguishes returns above an opportunity-cost benchmark from accounting profit and does not treat every rent as wrongdoing. |
| Inequality, mobility and intergenerational transfer | Explicitly covered | Concept 31 covers multiple mobility measures and asset/network transmission across generations. |
| Who pays, benefits and bears risk | **Strengthened by targeted addition** | New subsection gives a practical incidence-analysis sequence from legal payer/recipient through pass-through, indirect effects, time horizon, heterogeneity and evidence. |
| Geographic concentration and regional disparities | Explicitly covered | Concept 31 connects location to infrastructure, services, customer access, finance and the practical opportunity set. |
| Agency, collective action and limits of individual influence | Explicitly covered | Concept 31 covers alternatives, collective action and how coordination may alter bargaining options. |

### Group 24 conclusion

Group 24 is conceptually covered, with a targeted addition on distributional incidence. Remaining work is empirical: specify the counterfactual, identify the direct legal flows, estimate or observe pass-through, map downstream effects, separate immediate from long-run impacts, and disaggregate results where data allow. The party that first pays or receives a payment is not necessarily the party that ultimately bears the cost or captures the benefit.

## 5. Targeted changes made during this audit

1. **Concept 29 — Economic Measurement, Evidence and Inference:** Added decision thresholds, false positives and false negatives, sensitivity, precision, specificity, rare-event alert limits, out-of-sample testing and decision-specific error costs.
2. **Concept 30 — Time, Cycles and Economic Transmission:** Added real-time evaluation, data leakage, decision-time information sets, chronological testing, baseline comparison and forecast error assessment.
3. **Concept 31 — Distribution of Economic Power and Opportunity:** Added a structured distributional-incidence method covering baseline/counterfactual, direct effects, pass-through, indirect effects, time horizon, heterogeneous impacts and evidence uncertainty.

No current alert performance, cycle forecast, inequality estimate, policy incidence result or claim against a named actor was asserted as verified.

## 6. Remaining evidence and implementation work

- **Measurement and alerts:** Define event labels, population, evaluation window, threshold, base rate, error costs, data vintage and baseline. Evaluate precision/recall and false alarms in the intended operational setting.
- **Cycles and forecasting:** Record source publication times, revisions, data availability at each decision point, evaluation periods, baseline forecasts and stability across regimes.
- **Distributional incidence:** Define the counterfactual and relevant population, map legal and economic flows, estimate pass-through and indirect effects, and state which effects are observed, modelled or hypothetical.
- **Evidence discipline:** Preserve the distinction between a mechanism, association, forecast, causal estimate and normative recommendation. Record source dates, assumptions, uncertainty and alternative explanations.

## 7. Audit decision and next step

Groups 22–24 are **conceptually covered**, with targeted additions made to Concepts 29, 30 and 31. Remaining work is formal measurement, validation and evidence-based application to particular indicators, forecasts or distributional questions. No new numbered concept is justified by this audit.

**Next action:** Audit the roadmap's explicitly defined Group 25 — Commonly Confused Terms: Comparison Register (Concept 32). Its purpose and term clusters are specified in the roadmap. After that audit, reconcile the full concept inventory and audit sequence.

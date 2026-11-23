# Lifeconomist Universal Knowledge and Standards Retrieval Architecture

**Status:** Approved architectural direction; design and documentation stage only. No universal retrieval software has been implemented.  
**Version:** 0.1  
**Date:** 2026-11-23  
**Scope:** Cross-domain; applies to all Lifeconomist workstreams and domain investigations.

## 1. Purpose

Lifeconomist investigates interconnected real-world systems across economics, finance, healthcare, agriculture, environment, law, energy, education, infrastructure, technology, population and other domains. It must retrieve relevant established knowledge when a practical question requires it.

The user should not have to memorize standards, manuals, chapter numbers, classifications, institutions, source URLs or retrieval commands. Lifeconomist should identify potentially relevant knowledge from the task, retrieve authoritative material, explain why it matters, and help apply it with evidence and stated limitations.

The 2025 System of National Accounts (2025 SNA) is the first documented retrieval design example. It is not the only system and does not define the architecture for every domain.

## 2. Governing principle

**Discover before inventing; retrieve before repeating; verify before applying.**

For each real-world question:
1. Understand the question and the reality being investigated.
2. Identify relevant domains, concepts, measurement objects and decisions.
3. Search the knowledge and standards registry for established frameworks, classifications, methods, protocols, legal instruments, datasets and authoritative guidance.
4. Retrieve relevant material from authoritative sources and existing project notes.
5. Check scope, definitions, version, jurisdiction, applicability and limitations.
6. Apply the guidance to the task and its evidence.
7. Identify gaps that existing systems do not resolve.
8. Develop new methods only where a genuine gap is established and justified.
9. Preserve meaningful applications and lessons so the work is reusable.

This does not mean every question must use an international standard. A resource may be unavailable, unsuitable, outdated, contested, jurisdiction-specific or too broad. Record that finding rather than forcing a fit.

## 3. Architecture at a glance

The capability has three connected levels.

### Level 1 — Universal retrieval engine

One shared entry point and workflow for searching, selecting, verifying and applying knowledge. It should support natural-language questions, contextual suggestions and task-linked retrieval.

### Level 2 — Domain knowledge registries

Organized collections of resources by domain, such as:
- Economic and financial systems.
- Environment, climate and ecosystems.
- Healthcare, public health and biological systems.
- Agriculture, food and land systems.
- Law, justice and governance.
- Energy and natural resources.
- Population, society and demographics.
- Education, skills and labour.
- Transport, infrastructure and logistics.
- Technology, digital systems and science.
- Other domains as justified by research.

Domains are navigation aids, not isolated silos. A cross-domain resource should be linked from relevant domains rather than duplicated.

### Level 3 — Individual framework records

Each framework, standard, classification, methodology, protocol, dataset family or other knowledge resource receives a structured record using the [Framework and Knowledge Resource Record Template](FRAMEWORK-AND-KNOWLEDGE-RESOURCE-RECORD-TEMPLATE.md).

The record identifies what the resource is, what it covers, what it does not cover, who maintains it, its authoritative source, version, status, related resources, retrieval cues and application history.

## 4. What counts as a knowledge resource

Do not label every resource a standard. The registry may include distinct resource types:

- **Accounting or statistical system:** integrated concepts, accounts, rules and tables, e.g. SNA.
- **Statistical standard or manual:** agreed definitions, compilation methods or reporting guidance.
- **Classification:** structured categories for consistent identification, e.g. disease or industry classifications.
- **Measurement framework:** concepts and indicators for assessing a phenomenon.
- **Methodology or protocol:** procedures for collecting, compiling, testing or interpreting evidence.
- **Legal or regulatory framework:** binding or jurisdiction-specific rules and instruments.
- **Dataset or data platform:** published observations, metadata and access methods; not automatically a standard.
- **Index or composite measure:** a constructed measure with its own methodology and limitations.
- **Scientific or technical reference:** authoritative research, methods or technical guidance.

A resource may belong to more than one type. Record its actual nature instead of treating unlike resources as equivalent.

## 5. Shared retrieval experience

The eventual Lifeconomist workspace should provide three complementary ways to retrieve knowledge.

### A. Natural-language retrieval

A user asks an ordinary question such as "How should we measure water availability?", "What standards help us understand hospital expenditure?", "How do we classify agricultural production?" or "Which methods support comparison of criminal justice systems?"

The system searches relevant domain registries and returns a short, ranked set of useful resources.

### B. Contextual suggestions

When a task, dataset, indicator or investigation appears to involve an established framework, the system may offer a small, explainable suggestion.

Example: a food-production investigation may surface agricultural census methods, SNA production concepts, water accounting or land/ecosystem measurement. It should explain why each resource may apply and allow the user to dismiss it.

### C. Task-linked retrieval

A current investigation, indicator specification, report or decision can request a check for relevant standards and methods without requiring the user to restate the context.

The user remains in control. Retrieval must not interrupt work or silently impose a framework.

## 6. Shared retrieval and application workflow

1. **Parse the task:** identify the question, real-world object, domain(s), geography/jurisdiction, time period, intended decision and required evidence.
2. **Discover candidate resources:** search the registry using concepts, synonyms, classifications, domain tags and retrieval cues.
3. **Rank relevance:** consider the task's purpose, resource scope, authority, jurisdiction, version and known limitations. Do not rank by name recognition alone.
4. **Retrieve existing project knowledge:** check indexes, previous lessons, applications and source assessments before creating new notes.
5. **Verify the source:** consult the authoritative publication or responsible institution. Confirm version/date and exact passages or definitions before technical use.
6. **Explain relevance:** state why the resource applies, what it can contribute and what it cannot establish.
7. **Cross-check complementary resources:** identify other frameworks needed for dimensions outside the first resource's scope.
8. **Apply to evidence:** map definitions and methods to actual data, identify missing fields, assumptions, quality issues and uncertainty.
9. **Record the application:** save meaningful new findings, decisions, corrections or reusable mappings; link existing records instead of duplicating them.
10. **Review and maintain:** monitor changes to authoritative versions and assess whether updates affect existing applications.

A retrieval result is guidance for investigation, not automatic proof that a dataset is valid or a conclusion is correct.

## 7. Minimum framework record

Every substantive resource record should contain, where applicable:
- Stable resource ID and preferred title.
- Resource type and domain(s).
- Responsible institution or issuing authority.
- Purpose and real-world questions it addresses.
- Scope, units of analysis and coverage.
- What it does not cover or cannot establish.
- Concepts, definitions, classifications and measurement methods.
- Geographic and jurisdictional applicability.
- Official source and access location.
- Version, publication date, effective date and update status.
- Related and complementary resources.
- Search terms, synonyms and practical retrieval cues.
- Evidence, data and metadata requirements.
- Known limitations, comparability issues and uncertainty.
- Project documentation and prior application links.
- Verification status, last checked date and next action.

Unknown fields must remain explicitly unknown or pending. Do not fill gaps by assumption.

## 8. Cross-domain coordination

A real-world investigation may require several resources at once. Lifeconomist should:
- Retrieve each resource for the dimension it actually covers.
- Preserve its own definitions, units, classifications and accounting boundaries.
- Identify overlaps, differences and incompatible assumptions.
- Map relationships without merging methods.
- Avoid double-counting the same phenomenon.
- Explain when two resources measure different things despite similar labels.
- Distinguish measurement results from causal explanations and decisions.

For example, a food-system investigation could need agricultural production statistics, environmental accounts, national accounts, health and nutrition classifications, transport evidence and legal requirements. No single one replaces the others.

## 9. Authority, evidence and version governance

- Prefer the issuing institution's official publication or maintained source.
- Record secondary explanations as secondary sources, not as the authority itself.
- Confirm whether a resource is adopted, recommended, experimental, superseded, under revision or jurisdiction-specific.
- Keep publication date, version and effective date distinct.
- Verify exact technical passages before applying paragraph-level rules.
- Preserve source provenance, observation dates, definitions, methods, revisions and access/licensing restrictions.
- Do not infer global adoption from publication or endorsement.
- Do not infer operational implementation in Nigeria or another country without evidence.
- Record disagreements between authorities and unresolved methodological questions.
- Review affected project applications when an important resource changes.

## 10. Relationship to Lifeconomist workstreams

The retrieval capability is cross-cutting infrastructure, not a new workstream.

- **A — Deep Conceptual Foundations:** retrieves established concepts, theory and mechanisms while preserving critical examination.
- **B — Measurement:** retrieves definitions, classifications, units, formulas, compilation methods, data standards and validation requirements.
- **C — Evidence-Based Monitoring:** retrieves relevant indicators, official data systems, metadata and interpretation guidance.
- **D — Footprint Intelligence:** retrieves source methods, entity classifications, geospatial and technical standards, and evidence protocols.
- **E — Opportunity Intelligence and Economic Application:** retrieves sector rules, market structures, institutional requirements and relevant evidence; it does not turn a framework into a business opportunity automatically.

The five workstreams retain their existing boundaries and governance.

## 11. Relationship to existing SNA retrieval design

The [SNA Contextual Retrieval System](SNA-CONTEXTUAL-RETRIEVAL-SYSTEM.md) remains the first detailed domain-specific retrieval specification. It should eventually operate as a specialist collection within the universal retrieval architecture.

The existing SNA resources retain separate roles:
- [2025 SNA Application and Retrieval Index](2025-SNA-APPLICATION-AND-RETRIEVAL-INDEX.md): chapter-level navigation.
- [2025 SNA Study and Resumption Checkpoint](2025-SNA-STUDY-AND-RESUMPTION-CHECKPOINT.md): detailed study history and stopping point.
- [SNA Contextual Retrieval System](SNA-CONTEXTUAL-RETRIEVAL-SYSTEM.md): SNA-specific user experience and feature design.

Do not rewrite or duplicate the SNA archive to fit this architecture. Link and reuse it.

## 12. Implementation sequence

**Phase 0 — Documentation and inventory (current phase)**
- Establish this architecture.
- Establish the shared framework record template.
- Create an initial cross-domain registry with honest status labels.
- Link existing Lifeconomist records and SNA retrieval resources.
- Identify gaps in current domain documentation.

**Phase 1 — Curated searchable foundation**
- Convert validated resource records into a consistent, searchable knowledge store.
- Add aliases, domain tags, retrieval cues, source versions and links.
- Test manual natural-language retrieval against real Lifeconomist questions.

**Phase 2 — Unified user entry point**
- Add a persistent "Find relevant knowledge" control.
- Search across domain registries and return concise explanations and authoritative links.
- Keep SNA as a specialist collection within the shared experience.

**Phase 3 — Context-aware retrieval**
- Add explainable task-aware suggestions and task-linked checks.
- Retrieve multiple complementary resources when a question crosses domains.
- Allow dismissals and relevance feedback.

**Phase 4 — Evidence-grounded application**
- Connect retrieved guidance to current datasets, indicator specifications and investigations.
- Surface missing evidence, uncertainty, conflicting definitions and scope limits.
- Save validated applications and update resource records.

Build only when the relevant capability is understood and there is a practical use case. Use existing search, document and retrieval infrastructure before developing custom software.

## 13. Initial acceptance criteria

The universal retrieval capability is ready for an initial practical test when:
- A user can ask a question in ordinary language without knowing a framework's name.
- It can identify relevant resources across more than one domain when appropriate.
- It explains why each resource was suggested.
- It distinguishes standards, classifications, methodologies, datasets, legal instruments and indices.
- It links to authoritative sources and identifies the applicable version.
- It shows scope and limitations, including what a resource cannot answer.
- It checks existing project records before creating duplicate notes.
- It can combine complementary guidance without merging incompatible definitions.
- The user can dismiss suggestions and continue uninterrupted.
- No feature is described as implemented until software and acceptance tests confirm it.

## 14. Immediate next actions

1. Maintain the initial [Knowledge and Standards Registry](KNOWLEDGE-AND-STANDARDS-REGISTRY.md) as a discovery inventory, not a claim of completed research.
2. Audit existing Lifeconomist repository records; link them rather than recreating them.
3. Verify candidate international frameworks from responsible institutions before promoting them from candidate to verified records.
4. Select one practical cross-domain investigation to test manual retrieval.
5. Expand the registry based on real questions and identified gaps, not an arbitrary target number.

## 15. Governing safeguards

This architecture is a proposed design, not an implemented software system, complete global standards catalogue or claim that all domains have one universal standard. The registry is deliberately open-ended. Coverage, authority, technical quality, country adoption and operational availability must be assessed resource by resource.

Follow Lifeconomist's existing principles: Reality First; Evidence and Verification; Reuse Before Repetition; Capability Before Technology; Assemble Before Building; Complexity Only When Justified; and continuity without loss of knowledge.

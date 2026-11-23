# Lifeconomist Feature Specification — Contextual SNA Retrieval Assistant

**Status:** Approved design direction; specification only. No software implementation has been built yet.  
**Version:** 0.1  
**Date:** 2026-11-23

## 1. Purpose

Lifeconomist should make its SNA foundation available at the moment it is useful. The user should not need to memorize lesson numbers, paragraph references, special commands or a retrieval procedure.

The system should recognize when a task may involve national-accounting concepts and offer a simple way to retrieve relevant SNA guidance. It should preserve the user's ability to work practically without forcing a theoretical lesson.

Working name: **SNA Context Assistant**.

## 2. Core user experience

The user works normally in Lifeconomist. When a task, question, dataset, indicator or design decision appears to involve an SNA concept, the interface may show a small, non-blocking prompt:

> **SNA guidance may be relevant**
>
> This task appears to involve sector classification and cross-border transactions.
>
> [Find relevant SNA guidance] [Not now]

The user does not have to know the chapter number or remember a command. Selecting the retrieval action opens a compact panel with:
- the likely topic and why it was suggested;
- relevant chapter(s), with exact paragraphs only after source verification;
- links to previously recorded lessons, if any;
- the official source location;
- a short explanation in plain language;
- an option to apply the rule to the current task;
- any unresolved questions or limitations.

The prompt should never interrupt work or imply that the user has made an error.

## 3. Three ways to retrieve

### A. Contextual suggestion (automatic assistance)

When the user is working on a task, the system analyses the task description, relevant field names, selected indicators or workflow context for likely SNA concepts. If confidence is sufficient and the topic is relevant, it offers one small suggestion.

Examples:
- A government-debt analysis may surface financial accounts, balance sheets, government sector and financial-instrument guidance.
- A farm production/value-added analysis may surface production accounts, enterprises/establishments, supply-use tables and labour.
- A cross-border capital-flow analysis may surface residence, transactions between residents and non-residents, financial accounts and globalization.

Suggestions must be explainable: show what in the task caused the suggestion. Avoid broad or repeated pop-ups.

### B. Always-available retrieval control (manual fallback)

Provide a persistent control in the Lifeconomist workspace, such as **SNA Help** or **Find SNA guidance**. It opens a search panel. The user can type naturally, e.g.:
- "I am analysing government debt."
- "How should I classify this transfer?"
- "What is the difference between market and nominal value?"
- "Which SNA rules apply to informal businesses?"

The user should not need to remember a fixed phrase or lesson number.

### C. Task-linked retrieval (on demand)

Every relevant Lifeconomist task, indicator specification or analytical report may offer **Check SNA relevance**. This explicitly checks the current task without requiring the user to explain it again.

## 4. Retrieval workflow behind the interface

1. **Understand the task:** identify the economic activity, unit, sector, transaction, stock/flow, instrument, geography and measurement question where relevant.
2. **Search the index:** query the 39-chapter Application and Retrieval Index and any later paragraph-level mappings.
3. **Search the lesson archive:** retrieve existing lessons from the SNA study checkpoint or future structured lesson records.
4. **Verify the authority:** open the exact paragraph(s) in the official 2025 SNA White Cover PDF. Never rely on a chapter title or an old paraphrase alone for a technical decision.
5. **Check related standards:** identify whether BPM7, Government Finance Statistics, Monetary and Financial Statistics, SEEA, ILO standards or another framework is also relevant.
6. **Explain only what is needed:** produce a short, plain-language explanation first. Offer deeper technical detail only when useful or requested.
7. **Apply with evidence:** map the rule to the actual data or decision, identify missing information and state assumptions.
8. **Record learning:** if a new issue was resolved, update the retrieval index and/or create a focused lesson or application record. Do not duplicate existing lessons.

## 5. Suggested retrieval panel

The panel should use a compact structure:

1. **Why this appeared** — one sentence explaining the detected connection.
2. **Relevant SNA location** — chapter title and verified paragraph numbers.
3. **What it means** — plain-language explanation.
4. **How it affects this task** — concrete implication for the current analysis.
5. **Evidence needed** — data fields, definitions or source documents required.
6. **Confidence and open issues** — distinguish verified rules from assumptions or unresolved matters.
7. **Source and prior learning** — official source link and link to the existing lesson record.

Suggested actions:
- **Apply to this task**
- **Explain more simply**
- **Show the original SNA text**
- **Save this application**
- **Not relevant**

## 6. Trigger design and safeguards

- Use contextual suggestions only when relevance is meaningful; do not show a prompt for every word that resembles an SNA term.
- Prefer a small inline suggestion or side panel over a blocking modal.
- Do not repeat the same suggestion within the same task unless the task materially changes.
- Provide a clear "Not relevant" / dismiss option.
- Do not infer a technical conclusion from keyword matching alone.
- Show the reason for each suggestion and allow the user to inspect the source.
- Exact paragraph references must be verified against the official edition in use.
- Preserve uncertainty, data-quality limitations and differences between statistical standards.
- Never present a lesson as completed merely because the system retrieved it.
- Do not force the user to memorize chapter numbers, prompt templates or retrieval commands.
- The user can always ignore the suggestion and continue the practical work.

## 7. Minimum viable implementation sequence

Build only after the relevant Lifeconomist workspace architecture is ready. Avoid premature complexity.

**Phase 1 — Searchable foundation**
- Store the chapter index and lesson metadata in a structured, searchable format.
- Keep the official source URL and version with each record.
- Add a manual "Find SNA guidance" search control.
- Search by natural-language topic and return likely chapters and recorded lessons.

**Phase 2 — Task-aware suggestions**
- Pass the current task description and relevant metadata to the retrieval service.
- Return a small set of likely SNA references with an explanation of relevance.
- Require user selection before applying detailed guidance.

**Phase 3 — Evidence-grounded application**
- Retrieve the exact official paragraph text or trusted source excerpt.
- Generate a task-specific explanation and evidence checklist.
- Save the application and update the index where appropriate.

**Phase 4 — Improve carefully**
- Evaluate missed relevant references and false suggestions.
- Add more precise topic-to-paragraph mappings based on actual Lifeconomist use cases.
- Expand only when there is evidence that additional complexity is useful.

## 8. Suggested technical-neutral architecture

The capability can be assembled from:
- **Knowledge store:** official-source metadata, chapter index, paragraph mappings, lesson records and application records.
- **Retriever:** natural-language search over chapter/topic/paragraph metadata and lesson records.
- **Task context:** current task description, data schema, indicator definitions and workflow stage.
- **Relevance selector:** ranks candidate references and explains why they may apply.
- **Source verifier:** confirms exact paragraph and edition before presenting technical claims.
- **Explanation/application layer:** plain-language guidance, evidence checklist and task application.
- **User interface:** persistent retrieval control plus non-blocking contextual suggestion.
- **Feedback and governance:** dismissal, relevance feedback, source versioning and no-duplication checks.

This follows Lifeconomist's established principles: capability before technology; assemble before building; introduce complexity only when justified.

## 9. Initial acceptance criteria

The feature is ready for an initial practical test when:
- A user can describe a task in ordinary language without knowing any SNA terminology.
- The system can suggest relevant chapters without requiring memorized commands.
- The suggestion explains why it appeared.
- A user can open the relevant lesson and official source.
- Exact paragraph references are source-verified.
- The user can dismiss the suggestion and continue without interruption.
- The system checks existing records before creating new lesson content.
- The system can save a task-specific application without duplicating the foundation archive.

## 10. Relationship to the existing SNA documentation

- Chapter navigation: `2025-SNA-APPLICATION-AND-RETRIEVAL-INDEX.md`
- Detailed study archive: `2025-SNA-STUDY-AND-RESUMPTION-CHECKPOINT.md`
- Feature design: this document.

These documents have separate responsibilities. The index points to knowledge; the checkpoint preserves lessons; this specification describes how the future Lifeconomist interface should make that knowledge appear when relevant.

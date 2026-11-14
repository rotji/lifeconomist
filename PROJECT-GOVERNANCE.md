# Lifeconomist Project Governance

**Version:** 1.0  
**Status:** Adopted  
**Adopted:** 2026-11-14  
**Project owner:** The project owner retains final authority over material project decisions.  
**Applies to:** All Lifeconomist workstreams, programmes, research domains, experiments, publishing activities, project records, collaborators, and future areas of work.

## 1. Purpose and relationship to the universal standard

This charter adopts the Universal Project Governance Standard v1.0 as the project-specific governance arrangement for Lifeconomist. It translates the universal principles into a proportionate operating framework suited to Lifeconomist's existing architecture.

This charter is the authoritative home for Lifeconomist-wide governance authority, project information classifications, decision and change governance, collaboration boundaries, review, and adoption rules. It does not replace the substantive research methods or operational protocols that govern particular activities.

The governance structure has three levels:

1. **Universal Project Governance Standard:** the reusable framework that can be adopted by different projects.
2. **This Lifeconomist Project Governance Charter:** the project-specific adoption and authority arrangement.
3. **Operational protocols, methodologies, architectures, and research artifacts:** the practical rules and substantive knowledge for particular project activities.

Where a project-wide governance question arises, use this charter. Where a question concerns how a particular research or operational activity is performed, use the relevant methodology or protocol. Avoid creating duplicate rules in multiple documents; link to the authoritative location.

## 2. Governing principles

Lifeconomist adopts the following project-wide principles:

### 2.1 Reality-first and evidence discipline

Keep concepts, models, measurements, claims, and decisions connected to observable reality. Distinguish what is directly established from what is inferred, interpreted, hypothesized, estimated, proposed, or unknown. Preserve source provenance, dates, definitions, assumptions, limitations, uncertainty, and contradictory evidence where relevant.

A plausible mechanism is not proof of causation. A trace is not proof of the event or interpretation it appears to suggest. A documented design is not proof of implementation, and implementation is not proof of validation or effectiveness.

### 2.2 Interconnected investigation without forced connections

Investigate relevant entities, roles, dependencies, layers, flows, mechanisms, feedback, and consequences across domains when they materially help answer the question. Do not assume every possible connection is relevant or established. Expand or narrow an investigation in response to evidence and a testable reason.

### 2.3 Continuity without unnecessary repetition

Reuse existing valid work before starting equivalent work. Resume from the actual records and artifacts rather than relying on memory or a single summary. Revisit prior work when material new evidence, changed circumstances, contradictions, improved definitions or methods, or a demonstrated gap justifies review. Preserve the history and explain consequential revisions.

The operational rules are in [PROJECT-RECORDS-AND-CONTINUITY-PROTOCOL.md](PROJECT-RECORDS-AND-CONTINUITY-PROTOCOL.md).

### 2.4 Evolution without loss of knowledge

Lifeconomist may change its scope, methods, priorities, architecture, and applications as understanding develops. Change should improve the project without silently erasing relevant history, hiding uncertainty, or treating earlier work as if it never existed. Preserve prior decisions and explain material revisions.

### 2.5 Proportionality and purposeful resource use

Apply governance effort in proportion to the significance, risk, reversibility, cost, and reach of the activity. Do not create a register, meeting, approval gate, document, or process merely for administrative completeness. Use the lightest process that preserves accuracy, safety, traceability, and useful continuity.

### 2.6 Adaptability without loss of direction

Lifeconomist can explore new domains and opportunities without assuming that every discovery requires a new workstream, product, indicator, or programme. First determine whether the discovery fits an existing capability or record. Add structure only when it solves a demonstrated need.


### 2.7 Development first; governance in the background

Lifeconomist is an active research and development project, not a governance-administration project. Governance exists to support useful work, protect continuity, and prevent avoidable errors; it must not compete with the work it is meant to support.

- Proceed with useful exploration, research, experimentation, analysis, and building without first completing governance or documentation steps that are not genuinely needed.
- Apply governance quietly as a set of safeguards and shared expectations, not as a recurring checklist, approval ritual, or separate workstream.
- Do not interrupt routine development to update governance documents, registers, logs, or summaries. Make a record when the work produces something worth preserving or when a material decision, risk, change, or handoff genuinely requires it.
- Do not create governance tasks, reviews, meetings, forms, approvals, or documents solely to demonstrate compliance or administrative completeness.
- Keep routine, reversible work moving within the existing approved direction. Seek the project owner's decision only when a matter genuinely crosses the material-authority boundary in this charter.
- If governance itself begins slowing, distracting from, or duplicating useful project work, treat that friction as a reason to simplify how the rules are applied—not as a reason to add another layer.

The default is to continue the project. Governance intervention is the exception and must have a clear practical reason.

## 3. Project information classification

Use the following classifications to communicate the governance status of project components, directions, decisions, and activities. Apply them where the status could otherwise be misunderstood; do not force a label onto every paragraph or routine note.

| Classification | Meaning | What it does not mean |
|---|---|---|
| **Verified Current Reality** | A project condition, artifact, implementation, result, or capability directly checked against relevant records or evidence and confirmed as currently existing. | It does not mean the capability is effective, complete, safe, or independently validated unless that has separately been established. |
| **Approved Direction** | A material project direction, scope, method, architecture, or decision explicitly authorised by the project owner or validly delegated authority. | It does not mean the direction has been implemented or that its assumptions are proven. |
| **Proposed Information** | An idea, design, recommendation, candidate method, possible programme, or suggested change awaiting a decision or further development. | It is not an approved commitment, current capability, or verified finding. |
| **Unresolved Information** | A question, uncertainty, dependency, conflict, missing evidence, or decision that remains open. | It must not be silently filled with an assumption or presented as settled. |
| **Historical Information** | A previous state, superseded decision, former method, completed phase, or past condition retained for traceability and context. | It is not automatically current or still authoritative. |

### 3.1 Keep project status separate from research evidence status

These classifications describe the **governance status of project information**. They must not replace or be confused with the evidence labels used inside research.

Research artifacts must use evidence descriptions appropriate to their subject, such as directly observed, officially reported, independently corroborated, calculated, estimated, interpreted, hypothesized, disputed, unverified, or unknown. The research methodology and the relevant domain protocol govern those labels.

For example, a programme may be an **Approved Direction** while a hypothesis inside it remains **Unverified**. A published report may be a **Verified Current Reality** as an existing artifact while one of its claims remains disputed or uncorroborated.

### 3.2 Status changes

Change a status when the underlying facts or authorisation change. Preserve the prior status where it matters to project history. Do not promote a proposal to an approved direction because it appears in a document, or promote an approved design to an implemented capability merely because work has begun.

## 4. Project documentation governance

The repository is the durable project record. Each document should have a clear role and an authoritative home.

- **README.md:** project identity, purpose, high-level architecture, and navigation.
- **PROJECT-GOVERNANCE.md (this charter):** project-wide governance, status classifications, authority, decision and change rules, collaboration boundaries, and governance review.
- **RESEARCH-METHODOLOGY.md:** research and development workstream responsibilities, shared reasoning principles, and research methods.
- **PROJECT-RECORDS-AND-CONTINUITY-PROTOCOL.md:** record hierarchy, preservation, resumption, pauses, handoffs, and continuity operations.
- **DECISION-REGISTER.md:** material decisions, reasons, alternatives, and revisit conditions.
- **RESEARCH-LOG.md:** meaningful chronological research and project events.
- **CURRENT-STATE.md:** concise, derived navigation snapshot; it may lag and is not proof that no later work occurred.
- **Workstream, programme, architecture, methodology, and research artifacts:** authoritative detail for their stated domains and subjects.
- **Git history and diffs:** technical record of repository changes, not independent validation of research claims.

Do not duplicate entire policies, findings, or histories across documents. Where another document needs to refer to a rule, link to its authoritative home and add only the operational detail needed locally.


**Documentation principle — document to support development, not to interrupt it.** Documentation is a means of preserving useful knowledge, explaining consequential decisions, enabling continuity, and making work independently understandable. It is not an end in itself. Create or update a document when there is substantive knowledge, a material decision or change, a meaningful result, a necessary handoff, or a practical need for future work to rely on the information. Use the existing appropriate record; do not create a new document or update multiple records just because an activity occurred. Routine exploration, conversation, minor edits, and ordinary development may proceed without a documentation event. Capture important outcomes at a natural point in the work, with enough detail for their intended future use and no more ceremony than necessary.

## 5. Research and information management

Research must follow [RESEARCH-METHODOLOGY.md](RESEARCH-METHODOLOGY.md) and the relevant domain-specific method. Methods may differ across economics, finance, technology, physical systems, environment, biology, markets, and other domains; a single universal research procedure must not be forced onto materially different subjects.

For substantive research, preserve the question and scope, method, sources and dates, definitions, assumptions, findings, reasoning, uncertainty, limitations, contradictions, and unresolved questions as appropriate.

Before starting a new investigation:
1. Identify the question and the decision or understanding it is intended to support.
2. Check relevant existing artifacts, decisions, methods, and checkpoints.
3. Reuse valid work and identify genuine gaps.
4. Define what evidence could support, weaken, or disconfirm the proposed explanation.
5. Choose a method proportionate to the question, risk, and available resources.
6. Record substantive outcomes in the appropriate durable artifact.

A new discovery may update earlier work, but it does not automatically invalidate it. Assess the effect on the specific definitions, observations, calculations, conclusions, decisions, and dependent artifacts involved.

## 6. Decision governance and authority

### 6.1 Project owner

The project owner retains final authority over material decisions affecting Lifeconomist's purpose, scope, governance, workstream architecture, major methods, priorities, commitments, material resource or risk exposure, and adoption or reversal of project-wide rules.

### 6.2 Routine research and operational choices

Routine, reversible choices needed to investigate an already authorised question may be made by the person or assistant conducting the work, within the approved scope, methods, constraints, and available permissions. Examples include selecting a relevant source to inspect, testing a calculation, organising notes, or correcting a factual inconsistency after verification.

Routine research must not be blocked by unnecessary owner-approval gates. If a routine choice would materially alter scope, create a new commitment, expose the project to material risk, or change an approved direction, pause and seek the required decision.

### 6.3 Material decisions

Record material decisions in the Decision Register. A decision record should identify the decision, date, rationale, alternatives considered where useful, and conditions that would justify revisiting it.

A recommendation, discussion, draft, or assistant-generated suggestion is not an approved decision. Do not infer approval from silence or from the mere presence of a proposal in the repository.

### 6.4 AI and delegated collaborators

AI systems and collaborators may investigate, analyse, challenge, draft, recommend, and perform explicitly authorised changes. They must not claim project-owner authority, silently approve material direction, invent evidence, or present proposed work as completed. They must disclose uncertainty, verify repository writes, and report the exact files changed.

## 7. Change management

Apply change control in proportion to the change's significance and potential consequences.

For a material change:
1. Identify the reason, evidence, problem, or opportunity prompting it.
2. Inspect the relevant existing artifacts and dependencies.
3. Describe the proposed change and reasonable alternatives.
4. Assess effects on project purpose, workstreams, methods, research artifacts, measurements, decisions, dependencies, outputs, maintenance, security, and prior conclusions as relevant.
5. Identify what should be preserved, revised, linked, deprecated, or left unchanged.
6. Obtain project-owner approval when the change falls within material decision authority.
7. Implement the authorised change and update the appropriate records.
8. Verify the result and report what changed, what did not change, and any remaining limitations.

For research-definition or conclusion changes, preserve the prior version, revised version, reason, motivating evidence, and implications for earlier analyses. Follow the more specific change-control provisions in the relevant methodology or protocol.

Do not require a formal change proposal for routine corrections or low-impact reversible improvements. Do not make unrelated edits merely because a file is being updated.

## 8. Project structure and technical governance

Keep the A–E workstream architecture and cross-cutting programmes coherent, but allow new domains and capabilities to emerge when justified. A discovery does not automatically require a new workstream, repository, service, software component, indicator, or product.

Before creating a new structural element, check whether the need can be met through an existing workstream, programme, artifact, or capability. Define its purpose, boundaries, relationships, dependencies, owner, status, and maintenance implications at a level proportionate to its importance.

Technical implementation, access controls, data handling, deployment, backups, licensing, and maintenance must follow the applicable technical and security requirements. Do not imply that a documented architecture or proposed feature has been implemented.

## 9. Progress and performance management

Report progress honestly and distinguish:
- Research or discovery completed.
- A method or specification drafted.
- A design or direction approved.
- An implementation completed.
- An implementation tested.
- A result independently verified or validated.
- An outcome shown to be effective in its intended setting.

These are different states and must not be collapsed into a generic claim of completion. Use meaningful milestones and evidence rather than activity volume or document count as a proxy for progress.

Use CURRENT-STATE.md as a concise navigation snapshot when material changes warrant it. Use the Research Log for meaningful history and the relevant artifacts for substantive detail. Do not create a task or status update for every conversation or minor edit.

## 10. Audit and quality assurance

Use proportionate checks to confirm that:
- Important claims have appropriate evidence and provenance.
- Definitions, units, dates, calculations, and methods are internally coherent.
- Project statuses match actual records and implementation.
- Links, indexes, and references point to the intended artifacts.
- Decisions and material changes are traceable.
- Research conclusions acknowledge limitations and alternatives.
- No material content was silently lost during revision.
- Security, privacy, legal, ethical, and operational risks have been considered where relevant.

A review may be triggered by a material decision, release, handoff, contradiction, new evidence, high-impact change, or observed quality problem. Do not require a heavyweight audit for every routine activity. Governance compliance is not proof that research is correct or that a product or opportunity will succeed.

## 11. Risk, security, privacy, and compliance

Consider risk in proportion to the activity. Relevant safeguards may include lawful access, privacy, consent, data minimisation, secure credentials, licensing and intellectual-property rights, financial exposure, operational safety, regulatory obligations, research ethics, and reputational consequences.

Do not collect, expose, commit, or retain secrets or sensitive data unnecessarily. Do not bypass access controls or treat public availability as automatic permission for every use. Where requirements are uncertain or consequences material, investigate them before proceeding and record the limitation.

A formal risk register is not mandatory for every investigation. Use one when the scale, duration, dependencies, or consequences justify it, or when legal, contractual, safety, or operational requirements demand it.

## 12. Handover and independent understanding

Lifeconomist should remain understandable and resumable by a capable person or AI system that did not participate in the original conversation or activity.

For a substantial handoff, pause, or transfer, the records should make it possible to establish:
1. What the project is for.
2. What currently exists and has been verified.
3. Which directions and decisions are approved.
4. Which proposals and questions remain unresolved.
5. Which records are authoritative for the subject.
6. Which constraints, dependencies, and risks matter.
7. What work has actually been completed and what has not.
8. The next useful action or decision, if one is known.
9. What should not be repeated and what new evidence would justify revisiting it.

This is an independent-understanding test, not a mandatory form to complete after every conversation. Use the Continuity Protocol and relevant checkpoints to support it.

## 13. Governance review and amendment

Review this charter when material project evolution, repeated operational friction, ambiguity, duplication, a significant risk, a change in authority, or a demonstrated governance gap makes review useful.

A review should:
- Identify the specific problem or new requirement.
- Check existing provisions before adding another rule.
- Assess effects on connected records and operating methods.
- Preserve the prior decision and document material amendments.
- Obtain project-owner approval for changes to project-wide governance.

Do not revise governance merely to reflect every new idea. The goal is a durable, useful framework that can evolve without unnecessary bureaucracy or loss of project knowledge.

## 14. Adoption and governing statement

This charter is adopted as Lifeconomist's project-specific implementation of the Universal Project Governance Standard v1.0. Existing workstream definitions, research methods, continuity rules, and domain-specific architectures remain in force except where an authorised, explicit amendment says otherwise.

**Governing statement:** Lifeconomist will be developed through evidence-led investigation, clear authority, traceable decisions, honest status reporting, proportionate change, responsible collaboration, and continuity of knowledge. It will evolve as reality and evidence require, while preserving what has been learned and avoiding unjustified repetition. No proposal is an approval, no design is an implementation, no implementation is a validation, and no conclusion is stronger than the evidence that supports it.

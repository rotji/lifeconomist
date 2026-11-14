# Project Records and Continuity Protocol

**Status:** Governing project-wide protocol  
**Adopted:** 2026-11-12  
**Applies to:** All Lifeconomist workstreams, research programmes, domains, experiments, publishing activities, and future project areas.

## 1. Purpose

This protocol defines how Lifeconomist preserves knowledge, records research history, communicates its latest known position, and resumes work without relying on memory or perfect administrative discipline.

The project must remain usable even when work progresses but a summary file is not updated immediately. No single summary document is the sole source of truth for project progress.

The governing distinction is:

- **Research artifacts preserve knowledge.**
- **The research log preserves meaningful history.**
- **The current-state document supports navigation and resumption.**
- **Git history preserves the technical history of repository changes.**
- **The decision register preserves material project decisions and their rationale.**

These records complement one another; none substitutes for all the others.

## 2. Authority and source-of-truth hierarchy

When records disagree, do not automatically trust the newest-looking summary. Establish what actually happened by checking the relevant evidence.

Use this order according to the question being answered:

1. **Primary research artifacts and evidence records** are authoritative for the actual content, methods, source evidence, calculations, findings, limitations, and unresolved questions of that investigation.
2. **Decision Register** is authoritative for formally recorded material project decisions, including their rationale, alternatives, and revisit conditions. A decision does not turn an untested proposition into a finding.
3. **Research Log** is the chronological account of meaningful research activity, changes, discoveries, pauses, resumptions, and handoffs. It provides context and traceability, but a log entry does not override contradictory primary evidence.
4. **Current State** is a concise, derived overview of the latest known project position. It is a navigation aid, not an independent source of evidence and not proof that no later work occurred.
5. **Git commit history and diffs** establish when repository changes were committed and which files changed. They do not, by themselves, explain the research meaning or validate the content.

If these sources conflict, identify the conflict, inspect the relevant artifacts and Git history, resolve what can be resolved, and record material corrections. If the actual position cannot be established, label it **unverified** rather than guessing.

## 3. Research artifacts: preserve the substance

Substantive research belongs in the relevant durable artifact, not only in a chat transcript, Current State, or Research Log.

A research artifact should preserve the elements appropriate to its subject, such as:
- The question, scope, and purpose.
- Definitions, methods, assumptions, and units.
- Sources, dates, provenance, and evidence.
- Findings and the reasoning that supports them.
- Distinctions between verified facts, interpretations, hypotheses, proposals, and unknowns.
- Limitations, contradictions, uncertainty, and unresolved questions.
- Relevant changes to earlier conclusions and their implications.

Do not duplicate entire research findings in the log or Current State. Link to the substantive artifact instead.

## 4. Research Log: meaningful chronological history

The Research Log records **material research events**, not every conversation, edit, or minor activity.

Create or update an entry when an event materially affects what the project knows, what it is doing, or how future work should proceed. Examples include:
- A substantial investigation, source audit, analysis, or experiment.
- A meaningful discovery, negative result, contradiction, or failed hypothesis.
- Creation or material revision of a research artifact, method, programme, or checkpoint.
- A material decision, change of direction, pause, resumption, or closure.
- A change to a definition, measurement, conclusion, evidence assessment, or project boundary.
- A handoff that future work needs in order to resume without repeating completed work.

A log entry should normally state:
1. **Date and subject.**
2. **Purpose or trigger:** why the work occurred.
3. **Work performed:** what was actually examined or changed.
4. **Outcome:** what was established, learned, or not established.
5. **Artifacts:** links to the files, evidence records, or relevant commits.
6. **Status and next step:** what remains open, paused, completed, or awaiting a decision.

Use only the fields that are relevant. A short, precise entry is better than a long entry that obscures the outcome.

### What does not normally require a log entry

Do not create entries for routine conversation, minor wording edits, formatting, transient questions, or small corrections that do not materially affect meaning, evidence, decisions, or future work. Do record them if they reveal a consequential error or change.

The log is not a transcript, task checklist, or duplicate copy of every commit. It should explain the research significance of meaningful changes.

### Negative results and unfinished work

Record important unsuccessful attempts and negative results when they prevent repeated effort or change the next step. State what was attempted and what the result does and does not establish.

Never describe an incomplete task as completed. Preserve unresolved questions and failed access attempts where they matter to resumption.

## 5. Current State: derived navigation snapshot

`CURRENT-STATE.md` is retained because it helps a person or assistant orient quickly in a large repository. It is not required to be updated after every conversation or every unit of progress.

Update Current State when a **material change** affects the overall project picture or the next useful action, for example:
- A workstream or programme changes stage or status.
- A substantial milestone is completed.
- A new major programme, framework, or cross-project principle is adopted.
- A priority, pause, or resumption point materially changes.
- A previous summary becomes materially misleading.
- A new checkpoint changes how work should resume.

Do not update it for every small finding, minor correction, routine file edit, or discussion. Avoid duplicating detailed research content; summarize the position and link to the relevant source artifact, log entry, decision, or checkpoint.

### Staleness rule

A stale Current State is a known possibility, not a project failure. Its last-updated date must be honest. Do not infer that work stopped on that date.

When Current State has not been updated after subsequent work:
- Continue to treat the underlying artifacts, relevant log entries, decisions, and Git history as evidence of progress.
- Reconcile the summary when it is next materially useful.
- Do not backdate updates or pretend the summary was maintained continuously.
- If the latest position is uncertain, say so and investigate before changing it.

The absence of a Current State update must never erase, invalidate, or hide work that exists elsewhere in the repository.

## 6. Return and resumption procedure

At the start of a substantial return to Lifeconomist or a paused programme:

1. Read Current State for orientation, noting its last-updated date and treating it as provisional.
2. Read relevant recent Research Log entries and any named resumption checkpoint.
3. Open the actual research artifacts for the subject being resumed; verify completed work, open questions, evidence, and limitations.
4. Check the Decision Register for applicable decisions, constraints, and revisit conditions.
5. Inspect Git history or diffs when dates, file changes, or conflicts need verification.
6. Reconcile material discrepancies before deciding where to continue.
7. State the verified resumption point briefly, then proceed without repeating adequately completed work.

Do not read the entire repository on every return when the relevant records provide a reliable route to the work. Expand the review only when scope, conflict, or dependencies require it.

A paused task may remain paused indefinitely. Do not automatically restart it merely because it appears in Current State or the Research Log.

## 7. Recording pauses, resumptions, and handoffs

When pausing substantial work, preserve a useful checkpoint in the relevant programme or research artifact. It should state:
- What has been completed.
- What has not been investigated or validated.
- Important findings, decisions, constraints, and dependencies.
- The exact next useful action or decision, if known.
- What should not be repeated on return.
- Any conditions that would justify changing the proposed next step.

A Research Log entry should link to that checkpoint. Current State should link to it when the pause materially affects project navigation.

When resuming, verify the checkpoint against the actual artifacts and any material new evidence. The checkpoint is a guide, not permission to ignore changed circumstances.

## 8. Decisions and changes

Use the Decision Register for material choices about project architecture, scope, methods, priorities, governance, or operating rules. Do not use it as a general diary or for every research conclusion.

When a decision is reversed or materially revised:
- Preserve the original decision.
- Record the new decision separately.
- Explain the new evidence or reasoning.
- State what existing artifacts or work may be affected.

For material changes to a research definition or conclusion, follow the methodology's Change Control requirements: preserve the previous version, new version, reason, motivating evidence, and implications for earlier analyses.

## 9. Lightweight maintenance: significance over frequency

The required standard is **accurate, traceable records**, not constant administrative updates.

| Event | Research artifact | Research Log | Current State | Decision Register |
|---|---|---|---|---|
| Minor wording or formatting correction | Update only if needed | Normally no | No | No |
| Substantial new finding | Yes | Yes | If project position changes | Only if it changes a material decision |
| New or materially revised programme | Yes | Yes | Yes | Yes, if a material decision |
| Important failed test or negative result | Yes, where it belongs | Yes | If next action/status changes | If it changes a decision |
| Pause or resumption | Checkpoint where useful | Yes | If it changes the overall position | Only if a material decision |
| Material decision or reversal | Relevant artifact if needed | Yes | If project position changes | Yes |
| Routine conversation or exploratory question | Only if substantive knowledge is established | Normally no | No | No |

This table is a default, not a mechanical substitute for judgment. If an event materially affects future interpretation or resumption, preserve it in the appropriate record.

## 10. Responsibilities when using AI or other collaborators

Any person or assistant making a material change to Lifeconomist must:
- Inspect the relevant existing records before editing.
- Preserve existing content and conventions unless a justified change is intended.
- Write findings to the appropriate substantive artifact.
- Add a concise Research Log entry for material research events.
- Update Current State only when the significance criteria above are met.
- Update the Decision Register when a material project decision is made.
- Verify changes after writing and report exact files changed.
- Never claim that a file, log, checkpoint, or summary was updated unless the repository write succeeded and the result was checked.

If work progresses but a record is not updated immediately, do not conceal the omission or reconstruct details from guesswork. Recover the actual work from artifacts, evidence, conversation context where available, and Git history; then make a clearly dated reconciliation entry if the event is material.

## 11. Governing rule

**Lifeconomist must preserve continuity without depending on perfect memory or perfect administrative timing.**

Research artifacts preserve what is known. The Research Log preserves why and how the project changed. Current State helps locate the work but may lag. Decisions preserve deliberate choices. Git history preserves repository changes. On return, verify the underlying work and reconcile summaries; never repeat completed research solely because a summary is stale.

This protocol implements and operationalizes the existing Continuity, Pause, and Revision Principle. It does not create a new workstream or require every activity to follow a rigid linear sequence.


## 12. Development-first documentation: preserve what matters, then keep moving

Documentation must support the real work of Lifeconomist. It must not become a parallel activity that delays research, discovery, experimentation, analysis, or implementation.

Apply this principle in practice:

- **Work may proceed without administrative preparation.** Do not require a log entry, checkpoint, status update, approval form, or document before beginning or continuing ordinary work.
- **Document meaningful outcomes, not activity for its own sake.** Capture substantive findings, useful methods, important negative results, material decisions, consequential changes, and handoff information when they become worth preserving.
- **Use the lightest sufficient record.** Add the information to the existing relevant artifact where possible. Do not create a new document, duplicate content across records, or update every project summary for one development event.
- **Let documentation follow the work naturally.** It may be written during or after an activity when doing so is useful. It need not interrupt a productive investigation or build merely to satisfy a schedule.
- **Do not turn guidance into a mechanical checklist.** The event matrix and resumption procedure guide judgment; they are not forms that must be completed line by line for every task.
- **Keep routine work moving.** Routine, reversible choices within an approved scope do not require governance review. Escalate only a genuine material decision, significant risk, or authority boundary.
- **Simplify when records create friction.** If a documentation practice repeatedly delays work, duplicates existing information, or provides little future value, reduce or remove the burden while retaining any essential evidence, decision traceability, or continuity.

The practical test is: **Will this record materially help preserve knowledge, support a decision, prevent avoidable repetition, manage a real risk, or allow future work to continue accurately?** If not, do not create it merely for completeness.

This principle does not excuse losing important evidence or concealing material decisions. It sets the threshold for recording them so that documentation remains useful and proportionate.

**Default operating rule: continue useful project work; document what matters; do not let documentation become the work.**

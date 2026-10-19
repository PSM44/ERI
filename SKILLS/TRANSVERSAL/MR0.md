<!--
Skill package generated for transversal use.
Naming preserves the user's requested file names, including `Skiils`.
These documents are intended to be understandable by a blank AI agent and by a human collaborator.
-->
# MR0_Skiils.md — Integrated Management Review Skill

## 0. Skill identity

**Skill name:** MR.0 — Integrated Management Review  
**Abbreviation:** MR.0  
**Category:** Governance / management review / evidence reconciliation  
**Scope:** Transversal; not specific to NightShift or software.  
**Primary users:** Human decision-makers, project managers, AI assistants, orchestrators, analysts, technical leads, legal/finance/operations teams.  
**Core output:** A management-grade review that reconciles current truth, evidence, decisions, risks, roadmap impact, gates and next work.

## 1. Plain-language definition for humans

MR.0 is a structured review used to answer:

```text
Where are we really?
What is proven?
What is still uncertain?
What changed?
What decisions were made?
What risks remain?
What is blocked?
What can safely happen next?
Who must authorize the next step?
```

MR.0 is not a meeting summary and not a generic status report. It is a control artifact for keeping complex work honest and coherent.

Use MR.0 when a project has too many moving parts for informal memory to be reliable.

## 2. Technical definition for AI systems

For an AI system, MR.0 is a **fan-in reconciliation procedure**:

```text
inputs + evidence + decisions + risks + gates + roadmap
    -> reconciled current state
    -> readiness / no-go assessment
    -> next executable DAG
    -> authorization matrix
    -> handoff-ready management packet
```

The AI must distinguish:

- claim vs evidence;
- current state vs target state;
- recommendation vs authorization;
- completed vs partially completed;
- source-derived fact vs inference;
- active risk vs historical issue;
- decision vs suggestion;
- unknown vs pass.

## 3. When to use MR.0

Use MR.0 after or before:

1. A major milestone.
2. A long execution window.
3. A technical validation gate.
4. A legal or commercial decision gate.
5. A multi-party handoff.
6. A roadmap pivot.
7. A conflict between reports.
8. A release/deploy/freeze decision.
9. A high-cost or high-risk next step.
10. A context reset, new AI session or new responsible person.

Examples outside software:

- **Real estate closing:** reconcile PSA status, deposits, counsel comments, approvals, risks and next signatories.
- **Finance process:** reconcile funding memo, debt provider, board decisions, pending data and bank deliverables.
- **Academic project:** reconcile rubric, submitted work, professor feedback, next assignment and evidence.
- **Operations:** reconcile incidents, root cause, corrective actions, owner, deadline and risk.
- **AI autonomy project:** reconcile runs, commits, evidence, gates, authorization, runtime state and next DAG.

## 4. When not to use MR.0

Do not use full MR.0 for trivial tasks such as:

- one-off translation;
- short email drafting;
- simple calculations;
- isolated questions with no continuity impact.

For small tasks, use a simple answer or a short checklist. MR.0 is justified when coordination, evidence, risk or continuity matters.

## 5. Inputs required

Minimum inputs:

```text
PROJECT / MATTER =
DATE =
CURRENT OBJECTIVE =
LATEST KNOWN STATE =
AVAILABLE EVIDENCE =
OPEN DECISIONS =
RISKS / BLOCKERS =
REQUESTED NEXT STEP =
```

Optional but recommended:

```text
CANONICAL FILES =
COMMIT / VERSION / DOCUMENT REVISION =
OWNER / AUTHORITY =
DEADLINES =
BUDGET / COST CONSTRAINTS =
LEGAL / SECURITY / COMPLIANCE CONSTRAINTS =
```

If critical inputs are missing, ask targeted questions or mark the item as UNKNOWN.

## 6. Evidence hierarchy

When sources conflict, prefer stronger evidence. General hierarchy:

```text
1. Physical runtime/process/listener evidence.
2. Executable logs with timestamp, PID, exit code or transaction ID.
3. Durable state, checkpoint, manifest or signed document.
4. Test results / regression reports.
5. Git/document diff, SHA, tracked version.
6. Official email/document/source from responsible party.
7. Structured specialist report.
8. Narrative summary.
9. Memory or assumption.
```

Rules:

- Absence of evidence is not PASS.
- A confident statement is not evidence.
- A tool report is evidence only within its observed scope.
- If evidence is stale, say so.
- If the result depends on current public facts, verify externally.

## 7. Standard MR.0 structure

A complete MR.0 should include these sections:

```markdown
# MR.0 — Integrated Management Review

## 1. Executive status
## 2. Scope and authority
## 3. Current state
## 4. Evidence reviewed
## 5. Decisions accepted
## 6. Open decisions
## 7. Risks, blockers and unknowns
## 8. Readiness matrix
## 9. Roadmap impact
## 10. Active DAG / next work graph
## 11. Authorization matrix
## 12. Closed gates
## 13. Next eligible nodes
## 14. Handoff requirements
## 15. Terminal convergence statement
```

## 8. Readiness matrix template

```markdown
| Dimension | Status | Evidence | Gap | Next action |
|---|---:|---|---|---|
| Objective clarity | PASS/PARTIAL/FAIL | | | |
| Evidence sufficiency | PASS/PARTIAL/FAIL | | | |
| Legal/compliance | PASS/PARTIAL/FAIL | | | |
| Technical readiness | PASS/PARTIAL/FAIL | | | |
| Runtime/process readiness | PASS/PARTIAL/FAIL | | | |
| Rollback/abort path | PASS/PARTIAL/FAIL | | | |
| Owner/authority | PASS/PARTIAL/FAIL | | | |
| Cost/time constraints | PASS/PARTIAL/FAIL | | | |
| User acceptance | PASS/PARTIAL/FAIL | | | |
```

## 9. Authorization matrix template

```markdown
| Action | Current status | Who can authorize | Evidence required | Notes |
|---|---:|---|---|---|
| Read-only audit | Allowed / gated | | | |
| Evidence-only commit | Allowed / gated | | | |
| Source mutation | Allowed / gated | | | |
| Deletion / cleanup | Gated | | | |
| Deployment / release | Gated | | | |
| Long execution window | Gated | | | |
| Legal/commercial commitment | Gated | | | |
```

## 10. MR.0 output schema for AI

```text
TARGET=MR0_REVIEW
PROJECT=
DATE=
STATUS=
CURRENT_STATE=
PROVEN=
PARTIAL=
UNKNOWN=
CONFLICTS=
DECISIONS_ACCEPTED=
DECISIONS_OPEN=
RISKS=
BLOCKERS=
READINESS_MATRIX=
ROADMAP_IMPACT=
NEXT_DAG=
AUTHORIZATIONS_REQUIRED=
CLOSED_GATES=
NEXT_ELIGIBLE_NODES=
HANDOFF_REQUIRED=
TERMINAL_CONVERGENCE=
```

## 11. Quality criteria

An MR.0 is acceptable only if:

```text
- current state is explicit;
- evidence and claims are separated;
- uncertainty is preserved;
- decisions are explicit;
- risks are not buried;
- roadmap impact is visible;
- next actions are actionable;
- authorization boundaries are clear;
- no closed gate is advanced silently;
- a new person or AI can continue safely from it.
```

## 12. Common failure modes

Avoid:

1. Writing a polished narrative without evidence.
2. Turning MR.0 into a chronological diary.
3. Treating a recommendation as authorization.
4. Hiding partial failures.
5. Collapsing risks into “pending.”
6. Ignoring stale or conflicting sources.
7. Producing a roadmap with no current-state truth.
8. Producing a next step without owner or gate.
9. Using internal jargon without definition.
10. Omitting what must not be done.

## 13. Examples

### Bad MR.0 statement

```text
Everything looks good. We should continue to the next phase.
```

Problem: no evidence, no gate, no readiness matrix, no risk.

### Good MR.0 statement

```text
STATUS=PARTIAL_READY
Evidence confirms X and Y. Z remains unknown because source A and source B conflict.
Recommended next node is read-only audit before execution.
Execution remains gated by HUMAN authorization.
```

## 14. Relation to HO.1, ROADMAP and AI Dictionary

- **MR.0** reconciles current management truth.
- **HO.1** transfers minimum continuity to a new session/person/AI.
- **ROADMAP** defines direction, phases, dependencies and gates.
- **AI Dictionary** standardizes vocabulary and prevents role/term confusion.

MR.0 often produces updates for the other three.

## 15. Final rule

If the MR.0 cannot clearly answer “what is true, what is uncertain, what is next, and who can authorize it,” it is not complete.
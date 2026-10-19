<!--
Skill package generated for transversal use.
Naming preserves the user's requested file names, including `Skiils`.
These documents are intended to be understandable by a blank AI agent and by a human collaborator.
-->
# HO.1_Skiils.md — Handoff One Skill

## 0. Skill identity

**Skill name:** HO.1 — Handoff One  
**Category:** Continuity / session transfer / operational handoff  
**Scope:** Transversal; applicable to any long-running project or process.  
**Primary users:** Humans, AI assistants, project managers, technical leads, lawyers, analysts, operators, specialists.  
**Core output:** A compact but complete handoff that allows safe continuation without relying on memory.

## 1. Plain-language definition for humans

HO.1 is the minimum high-quality handoff needed so that another person or AI can continue the work without losing:

- objective;
- current state;
- evidence;
- gates;
- authority;
- risks;
- next action;
- prohibitions.

HO.1 is designed for continuity. It is not a full report and not a history of everything that happened.

## 2. Technical definition for AI systems

For an AI, HO.1 is a **state transfer contract**.

It must preserve enough information to continue safely in a new context:

```text
current state + evidence pins + authority + gates + next DAG + stop rules
```

The AI must treat HO.1 as an operational input, not as proof by itself. If HO.1 conflicts with physical evidence or newer source material, reconcile before acting.

## 3. When to use HO.1

Use HO.1:

1. Before ending a long session.
2. Before switching AI models or tools.
3. Before handing work to a specialist.
4. After a milestone or commit.
5. Before a high-risk action.
6. Before a meeting where another person must continue.
7. When context is too large and must be compressed.
8. When a project has multiple workstreams or gates.

Examples outside software:

- **Legal transaction:** pass counsel status, documents, signatories, closing conditions and open risks.
- **Finance:** pass bank package status, missing data, version of model, credit memo owner and next action.
- **Academic work:** pass rubric, current draft, professor feedback and next deliverable.
- **Operations:** pass incident state, workaround, root-cause hypotheses, pending owner and stop rule.

## 4. When not to use HO.1

Do not create a full HO.1 for trivial one-step tasks unless the user explicitly requests a handoff.

For simple tasks, a short “next step” note is enough.

## 5. HO.1 minimum fields

A valid HO.1 should answer:

```text
PROJECT=
TASK_OR_THREAD=
DATE=
CURRENT_OBJECTIVE=
CURRENT_STATE=
LATEST_VERIFIED_EVIDENCE=
AUTHORITY_MODEL=
OPEN_GATES=
CLOSED_GATES=
RISKS=
NEXT_ACTION=
DO_NOT=
STOP_IF=
```

For software or AI projects, add:

```text
ROOT=
BRANCH=
HEAD=
RUNTIME_STATE=
EVIDENCE_PATHS=
PROMPT_FILES=
COMMIT_STATUS=
```

For legal/commercial projects, add:

```text
DOCUMENT_VERSION=
PARTIES=
COUNSEL=
DEADLINES=
SIGNATORIES=
APPROVALS=
FUNDS_STATUS=
```

## 6. Standard HO.1 template

```markdown
# HO.1 — Handoff One

## 1. Identity
PROJECT=
TASK=
DATE=
OWNER=
HANDOFF_FROM=
HANDOFF_TO=

## 2. Objective
CURRENT_OBJECTIVE=
SUCCESS_CRITERIA=

## 3. Current state
STATUS=
PROVEN=
PARTIAL=
UNKNOWN=

## 4. Evidence pins
EVIDENCE=
VERSION / HEAD / DOCUMENT REVISION=
SOURCE_PATHS=

## 5. Authority and gates
AUTHORITY_MODEL=
OPEN_GATES=
CLOSED_GATES=
AUTHORIZATIONS_REQUIRED=

## 6. Active DAG
NEXT_NODE=
PARALLEL_NODES=
DEPENDENCIES=

## 7. Prohibitions
DO_NOT=

## 8. Risks and stop rules
RISKS=
STOP_IF=

## 9. Next action
NEXT_ACTION=
NEXT_PROMPT_OR_INSTRUCTION=

## 10. Terminal convergence
TERMINAL_CONVERGENCE=
```

## 7. HO.1 output schema for AI

```text
TARGET=HO1_HANDOFF
PROJECT=
DATE=
STATUS=
AUTHORITY=
CURRENT_STATE=
LATEST_EVIDENCE=
OPEN_GATES=
CLOSED_GATES=
NEXT_DAG=
NEXT_ACTION=
DO_NOT=
RISKS=
STOP_IF=
HANDOFF_QUALITY=PASS|PARTIAL|FAIL
```

## 8. Compression rules

HO.1 must be compact but not vague.

Use:

- exact version identifiers;
- exact file paths;
- exact gate names;
- exact owner/authority when known;
- bullet points over prose;
- explicit UNKNOWN when needed.

Avoid:

- long historical background;
- duplicate narrative;
- emotional or motivational text;
- “continue as before”; 
- undefined acronyms;
- burying a gate in prose.

## 9. Quality criteria

HO.1 is acceptable only if a blank AI or new human can answer:

```text
What am I continuing?
What is the latest verified state?
What must I not do?
What evidence can I rely on?
What is the next safe action?
When must I stop?
Who can authorize blocked actions?
```

## 10. Common failure modes

Bad HO.1 patterns:

```text
Continue with the project as discussed.
Everything is ready.
Use the latest version.
Proceed carefully.
```

These are unsafe because they lack state, evidence, gate and stop rules.

Good HO.1 pattern:

```text
STATUS=PARTIAL_READY
HEAD=abc123
PROVEN=A,B
UNKNOWN=C
DO_NOT=push/tag/deploy
NEXT=read-only audit
STOP_IF=HEAD differs or unauthorized files changed
```

## 11. Relation to MR.0, ROADMAP and AI Dictionary

- HO.1 is the continuity packet.
- MR.0 is the integrated management review.
- ROADMAP is the strategic path.
- AI Dictionary ensures the handoff vocabulary is understood.

A strong MR.0 can generate an HO.1. A strong HO.1 can preserve MR.0 decisions across sessions.

## 12. Final rule

If a new person or AI would need to ask “what exactly should I do next?” then the HO.1 is incomplete.
<!--
Skill package generated for transversal use.
Naming preserves the user's requested file names, including `Skiils`.
These documents are intended to be understandable by a blank AI agent and by a human collaborator.
-->
# AI.DICTIONARY_Skiils.md — AI Dictionary Skill

## 0. Skill identity

**Skill name:** AI Dictionary  
**Category:** Controlled vocabulary / terminology governance  
**Scope:** Transversal; usable by any project or AI workflow.  
**Primary users:** Humans, AI assistants, project teams, analysts, technical writers, governance leads.  
**Core output:** A clear, alphabetically ordered dictionary that distinguishes industry terms from internal terms and prevents operational misunderstanding.

## 1. Plain-language definition for humans

AI Dictionary is a controlled glossary. It ensures that people and AI systems use the same words with the same meaning.

It answers:

```text
What does this term mean?
Is it a standard industry term or internal jargon?
What should we call it instead if there is a better industry term?
When should the term be used?
What should it not be confused with?
```

## 2. Technical definition for AI systems

For an AI system, AI Dictionary is a **terminology control layer**.

It prevents errors caused by:

- undefined acronyms;
- internal jargon;
- role/runtime/model confusion;
- same term used with different meanings;
- obsolete terms;
- hidden assumptions;
- cross-project vocabulary drift.

## 3. Required dictionary principle

Prefer industry terms when they are adequate.

Use internal terms only when they express a real distinction not covered by industry language.

Examples:

```text
Use industry term: DAG, API, checkpoint, rollback, UAT, readiness, audit.
Use internal term when needed: MORCH, RORCH, MR.0, HO.1, TERMINAL_CONVERGENCE, DELTA_ONLY.
```

## 4. Required term categories

Every dictionary entry should classify the term.

Recommended categories:

| Category | Meaning |
|---|---|
| INDUSTRY | Standard or broadly used outside the project. |
| INTERNAL | Organization/project-specific term. |
| INTERNAL_NSH | NightShift-specific term. |
| ADAPTED_FROM_INDUSTRY | Standard concept adapted to local governance. |
| WATCH / RADAR | Observed technology, not adopted by default. |
| DEPRECATED | Term no longer preferred. |
| ALIAS | Alternative name that maps to canonical term. |
| AVOID | Term likely to confuse or cause bad execution. |

## 5. Alphabetical rule

The dictionary must be sorted alphabetically by the term being defined.

Do not primarily organize by topic. Topic organization makes terms harder to find and can hide duplicates.

If topic context is needed, use columns or tags:

```text
Term | Category | Domain | Expansion | Definition | Preferred usage | Avoid confusing with
```

## 6. Required entry schema

```markdown
| Term | Category | Domain | Expansion / Standard Name | Definition | Preferred Usage | Avoid Confusing With |
|---|---|---|---|---|---|---|
```

Minimum fields:

```text
TERM=
CATEGORY=
EXPANSION=
DEFINITION=
PREFERRED_USAGE=
```

Recommended additional fields:

```text
DOMAIN=
ALIASES=
STATUS=
SOURCE=
LAST_REVIEWED=
```

## 7. First-use rule

When an acronym appears for the first time in any deliverable, expand it once.

Examples:

```text
MR.0 (Integrated Management Review)
HO.1 (Handoff One)
DSH (DeepSeek Harness)
UAT (User Acceptance Test)
DAG (Directed Acyclic Graph)
```

## 8. Maintenance workflow

When adding or changing a term:

```text
1. Identify the term.
2. Check whether an industry term already exists.
3. Prefer industry term if adequate.
4. If internal term is needed, explain why.
5. Add expansion and definition.
6. Add preferred usage.
7. Add confusion warning if needed.
8. Sort alphabetically.
9. Update version/date.
10. If meaning changed materially, record in MR.0 or decision register.
```

## 9. Governance for internal terms

Internal terms must pass this test:

```text
Does this term encode a real role, authority, gate, artifact, process or product distinction?
```

If no, avoid creating the term.

Bad internal term creation:

```text
Inventing a new acronym for a normal checklist.
```

Good internal term creation:

```text
MORCH distinguishes decision/communication authority from host/model/runtime.
```

## 10. Integration of modern AI reasoning vocabulary

The dictionary should include industry terms that affect AI execution quality, including:

- Breadth-Depth Refinement.
- Diversity Saturation.
- Majority Voting.
- Recovery.
- Regression.
- Self-Critique.
- Self-Correction.
- Test-Time Scaling.
- Verifier-Free Refinement.

Internal adaptation:

- Refinement Gate.
- NSH Refinement Gate.

Important rule:

```text
Reasoning refinement improves decision quality but does not replace physical evidence.
```

## 11. Terms that require special care

### Role / runtime / model separation

Always preserve:

```text
ROLE != RUNTIME != MODEL != PROVIDER != ROUTE
HOST_UI != MORCH != NSH != RORCH != EXE != ROUTE
```

### Specialist confusion

A specialist backend such as Claude, Codex or DSH can perform bounded work. It does not become MORCH or RORCH unless explicitly assigned that role, and in NSH it should generally be marked:

```text
NOT_RORCH=true
NOT_MORCH=true
NO_GLOBAL_ORCHESTRATION=true
SCOPE_BOUNDED=true
RETURN_TO_MORCH=true
```

## 12. Output template for dictionary updates

```text
TARGET=AI_DICTIONARY_UPDATE
STATUS=
TERMS_ADDED=
TERMS_UPDATED=
TERMS_DEPRECATED=
INDUSTRY_TERMS=
INTERNAL_TERMS=
AMBIGUITIES=
QUESTIONS=
NEXT=
```

## 13. Quality criteria

An AI Dictionary is acceptable only if:

```text
- terms are alphabetically sorted;
- acronyms are expanded;
- industry vs internal distinction is explicit;
- preferred usage is provided;
- confusing aliases are controlled;
- internal terms do not replace industry terms without reason;
- deprecated or watch terms are not treated as active by default;
- the dictionary can be used by a blank AI or new human collaborator.
```

## 14. Common failure modes

Avoid:

1. Topic-only glossaries where terms are hard to find.
2. Acronyms with no expansion.
3. Internal jargon where industry words would work.
4. Multiple terms for the same concept without aliases.
5. Changing meaning silently.
6. Treating a technology in WATCH/RADAR as adopted.
7. Confusing provider, model, route, runtime and role.
8. Using the dictionary as a roadmap.

## 15. Final rule

If the dictionary does not reduce ambiguity for both humans and AI, it is not doing its job.
---
name: workflow-selector
description: Select the lightest appropriate development workflow automatically. Use for coding, debugging, refactoring, configuration, documentation, review, and multi-agent tasks. Combine document-driven-development, Karpathy-style behavioral discipline, ponytail, behavior-charter, i-have-adhd, and subagent coordination without duplicating rules.
---

# Workflow Selector

Before acting on a development task, silently classify it:

- **Read-only**: answer or inspect directly; do not create task documents.
- **Quick change**: use DDD quick mode (`change.md`), then apply available auxiliary skills as needed.
- **Standard change**: use DDD standard mode, then apply available auxiliary skills as needed.
- **Complex change**: use DDD complex mode, explicit scope and acceptance criteria. Delegate only when authorized and the work is genuinely divisible; complexity alone does not require subagents.

Focus management is an overlay, not a mode: when a task is broad, lengthy, or prone to unrelated exploration, use i-have-adhd if available alongside whichever DDD mode was selected.

Before applying an auxiliary skill, confirm it is discoverable and load its `SKILL.md`. Use the named skill when available; otherwise apply only the relevant brief principle without claiming that the skill was loaded. Karpathy behavioral guidelines means the specific `karpathy-behavioral-guidelines` skill when available, otherwise use its principles: state assumptions, keep changes surgical, define success criteria, and verify.
## Operating rules

1. Never replace `behavior-charter`, project instructions, or user authorization rules.
2. Prefer the lightest DDD mode that preserves correctness; any implemented change enters a DDD mode.
3. Let DDD define document structure, lifecycle, continuation files, and recovery order; do not duplicate those rules here.
4. State assumptions, ambiguities, scope, and verifiable success criteria before edits when needed.
5. Keep changes surgical and avoid speculative abstractions or unrelated cleanup.
6. Use documents as shared state: messages notify, documents carry stable context, code/tests provide final evidence.
7. Before declaring completion, verify the success criteria and report evidence plus unresolved risks.
8. Do not invoke or mention this selector as a separate user-facing ceremony unless the user asks about workflow selection.

## Conflict resolution

Higher-priority system, project, and safety instructions win. If another skill is more specific, use it for its domain and use this skill only to select the workflow and prevent duplication.

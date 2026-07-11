# Cérebro — Obsidian Vault for AI-Assisted Development

> A structured Obsidian vault designed to give AI coding agents (opencode, Claude, Cursor) persistent memory, project context, and operational knowledge across sessions.

## What is this?

Cérebro is a **knowledge management system** that bridges the gap between AI coding sessions. Instead of losing context between conversations, your vault retains:

- **Project context** — stack, architecture, decisions, current state
- **Session logs** — what was done, what's pending, what's next
- **Technical decisions** — ADRs with rationale and alternatives
- **Patterns & lessons** — failure patterns, prevention checklists, reusable knowledge
- **Operational runbooks** — deploy, debug, rollback procedures

## Quick Start

```bash
# Clone this repo
git clone https://github.com/ricardopiresqa/cerebro.git

# Open in Obsidian
# File → Open Vault → select the cloned folder

# Set up environment
cp .env.example .env
# Edit .env with your paths
```

## Vault Structure

```
Cérebro/
├── _templates/         ← Templates for projects, ADRs, runbooks, lessons
├── 0_inbox/            ← Drafts and uncategorized ideas
├── 1_projetos/         ← Active projects (CONTEXT.md + DECISIONS.md + CURRENT.md)
├── 2_knowledge/        ← Knowledge base (guides, studies, career)
├── 3_playbooks/        ← Reusable process playbooks
├── 4_runbooks/         ← Operational runbooks
├── 5_adrs/             ← Architecture Decision Records
├── 6_postmortems/      ← Incident postmortems
├── 7_research/         ← Research and proofs of concept
├── 8_patterns/         ← Code/architecture patterns and lessons
├── 9_standards/        ← Vault conventions
└── 10_glossary/        ← Technical glossary
```

## How It Works

### Project Files

Every project gets three mandatory files:

| File | Purpose |
|---|---|
| `CONTEXT.md` | Stack, structure, repo URL, what it is |
| `DECISIONS.md` | Technical decisions (chronological) |
| `CURRENT.md` | Current state, blockers, next step |

### Session Lifecycle

```
START SESSION
  1. Read CONTEXT.md + DECISIONS.md + last session log
  2. Search RAG for relevant history
  3. Load applicable skill
  4. Work

END SESSION
  5. Log session in sessoes/
  6. Reindex RAG
  7. Update DECISIONS.md if new decisions made
```

### Adding a Project

1. Create `1_projetos/<project-name>/`
2. Add `CONTEXT.md` with stack, structure, and repo info
3. Add `DECISIONS.md` with initial decisions
4. Add `CURRENT.md` with current state
5. Optionally create a ClickUp card and link it

## Templates

| Template | Use Case |
|---|---|
| `adr.md` | Architecture Decision Record |
| `CURRENT-template.md` | Project current state |
| `DECISIONS-template.md` | Technical decisions log |
| `sessao-template.md` | Session log |
| `LESSON-template.md` | Learned lesson |
| `runbook.md` | Operational procedure |
| `postmortem.md` | Incident postmortem |
| `onboarding.md` | Project onboarding checklist |
| `lefthook-default.yml` | Git hooks config |

## Features

- **Deterministic navigation** — numbered folders (0-10) for predictable structure
- **Fuzzy search** — RAG-powered hybrid search (vector + BM25) across all markdown
- **AI agent integration** — steering files tell agents how to behave in your vault
- **Session persistence** — every coding session is logged with decisions and context
- **Self-improvement** — pattern mining, failure analysis, skill effectiveness tracking

## Integrations

- **opencode** — reads vault context automatically
- **Obsidian** — renders markdown with Dataview for dashboards
- **ClickUp** — task management via API
- **RAG** — hybrid search with ChromaDB + BM25

## Philosophy

> Your AI agent should never start from zero. Every session builds on the last.

## License

MIT

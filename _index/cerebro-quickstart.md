---
title: "Cérebro Quickstart"
type: guide
tags: [vault/quickstart]
---

# Quickstart

## 1. Clone & Open

```bash
git clone https://github.com/ricardopiresqa/cerebro.git
```

Open the folder in Obsidian.

## 2. Set Up Environment

```bash
cp .env.example .env
# Edit .env with your local paths
```

## 3. Create Your First Project

```bash
mkdir -p 1_projetos/my-project
```

Copy templates from `_templates/` into the project folder:
- `CURRENT-template.md` → `CURRENT.md`
- `DECISIONS-template.md` → `DECISIONS.md`

Create a `CONTEXT.md` with your project's stack and structure.

## 4. Start Working

Each session:
1. Open your project's `CURRENT.md`
2. Work on the current task
3. Log what you did in a session file
4. Update `CURRENT.md` with next steps

## 5. Templates

Use templates from `_templates/` for:
- Architecture decisions (`adr.md`)
- Runbooks (`runbook.md`)
- Postmortems (`postmortem.md`)
- Lessons learned (`LESSON-template.md`)

## Related

- [[README]]

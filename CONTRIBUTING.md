# Contributing to Cérebro

Thanks for your interest in improving this vault!

## Adding a Template

1. Create your template in `_templates/`
2. Use placeholder syntax: `<field>`, `{{title}}`, `YYYY-MM-DD`
3. Add frontmatter with `type:` field
4. Keep it generic — no project-specific data

## Adding a Pattern

1. Create a file in `8_patterns/_session/`
2. Use frontmatter: `type`, `title`, `project`, `tags`
3. Include: problem observed, root cause, fix applied, prevention checklist

## Adding a Runbook

1. Create in `4_runbooks/`
2. Include: when to use, prerequisites, steps, verification, rollback, troubleshooting

## Guidelines

- **No secrets** — never commit API keys, tokens, or passwords
- **No personal data** — keep project-specific data out of templates
- **Portuguese or English** — both are acceptable
- **Frontmatter required** — all files should have YAML frontmatter
- **Wikilinks** — use `[[filename]]` for internal references

# Guide for agents

This file explains how to change Rewrite without breaking its package or prompt.

## What this repo contains

Rewrite is an agent skill written in Markdown. `SKILL.md` is the prompt that agents read. The repo has no build step.

Keep the skill portable. Do not write instructions that limit it to one or two agent tools.

## Key files

- `SKILL.md` is the repo's skill file. It contains portable YAML metadata, the steps for editing text, a writing-style section, and numbered patterns grouped in six sections and ordered by strength and frequency.
- `README.md` shows an example and explains installation and use.
- `CHANGELOG.md` shows the release notes.
- `.claude-plugin/plugin.json` describes the Claude plugin and points its skill loader at the root `SKILL.md`.
- `.claude-plugin/marketplace.json` lets users add this repo as a Claude marketplace.
- `.cursor-plugin/plugin.json` describes the Cursor plugin. Omit a `skills` path so Cursor loads the root `SKILL.md`.
- `agents/openai.yaml` holds the display name, short description, and default prompt for OpenAI-compatible agents.
- `scripts/validate-package.py` checks package files and shared values.

## Rules for changes

Keep `SKILL.md` and `README.md` in sync.

- **Patterns:** Number patterns from 1 without gaps, strongest and most frequent first. Add a new sign of AI writing as a pattern only when no existing pattern already implies it. Prefer adding it to an existing pattern. If you add, remove, or renumber a pattern, update every §reference and any README text that names a pattern. The validator derives the count from the headings.
- **Version:** Keep the same version in `SKILL.md` under `metadata.version`, the first `CHANGELOG.md` heading, `.claude-plugin/plugin.json`, and `.cursor-plugin/plugin.json`. Do not add a top-level `version` field to the skill.
- **Compatibility:** Keep install and use instructions neutral across agents. Names such as Claude Code, Cursor, OpenCode, and Codex are only examples.
- **Description:** The plugin manifests use the first sentence of the `SKILL.md` description.
- **Length:** Agents read every word of `SKILL.md` on each use. The validator caps it at 7,000 words. Add words only when they improve how the skill works.
- **History:** Add a short `CHANGELOG.md` note for any behavior change or non-obvious fix.
- **Checks:** Before publishing, run `python3 scripts/validate-package.py`, `npx skills add . --list`, and `claude plugin validate .`.
- **Git commands:** Never run git commands on the user's behalf, unless explicitly instructed to.

## Writing style

Use Plain Language in code comments, prompts, documentation, descriptions, validation messages, and progress reports.

- Lead with the main point.
- Use common words and active voice.
- Keep sentences and paragraphs short.
- Use one term for the same item.
- Use `must` for requirements.
- Use headings, lists, and tables when they help the reader.
- Remove repeated or unnecessary words.
- Limit acronyms and explain technical terms.
- Avoid double negatives.
- Keep exact identifiers, commands, paths, schema fields, quotations, watched phrases, and behavior-bearing examples.
- Keep the full technical meaning.
- Do not explain what you changed, or why you changed it, in the codebase itself. This includes, but is not limited to documentation and comments. Documentation must only describe the current state of the codebase. Descriptions of previous versions of the codebase are in version control, and must not be repeated in the documentation.

## Editing SKILL.md

- Keep the YAML metadata valid.
- Treat the prompt below the metadata as the product.
- Prefer a short, clear instruction over another exception or repeated explanation.
- Make every After example follow the writing style. Agents copy examples more closely than they follow rules.

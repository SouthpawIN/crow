# Crow — Deep Web Research Agent

Crow is a [Hermes Agent](https://hermes-agent.nousresearch.com) profile that produces **lore**: structured, interconnected knowledge bases built from deep web research. It is part of a multi-agent fleet where each agent has a distinct role — Crow's role is research, and its output is consumed by other agents (especially kashik, the guide writer).

## What Crow Does

1. Takes a research topic or question.
2. Runs the canonical pipeline: `query → web_search → web_extract → synthesize → llm-wiki structure`.
3. Evaluates every source for credibility, recency, and corroboration (minimum 2 independent sources for any canonical claim).
4. Writes structured lore files in `llm-wiki` format at `~/crow-lore/<topic>/`.
5. Uses the `/learn` command to persist cross-cutting meta-knowledge across sessions.

## Lore Directory Layout

```
~/crow-lore/<topic>/
├── index.md
├── entities/
├── concepts/
├── comparisons/
└── raw/
```

- `index.md` — entry point and table of contents
- `entities/` — people, organizations, systems, concrete things
- `concepts/` — ideas, theories, frameworks
- `comparisons/` — side-by-side analyses
- `raw/` — raw extracted source material (provenance trail)

## Profile Files

| File | Purpose |
|------|---------|
| `SOUL.md` | Identity, personality, and role description |
| `AGENTS.md` | Procedural workflow and conventions |
| `config.yaml` | Hermes Agent configuration |
| `herm/tui.json` | TUI settings (not distributed) |

## Multi-Agent Fleet

| Agent | Role |
|-------|------|
| senter | Triage |
| chizul | Worker |
| klerik | Profile editor |
| anser | Discord support |
| nous-girl | Brainstormer |
| kashik | Guide writer (consumes Crow's lore) |
| crow | Research (this agent) |

## Installation

Copy `SOUL.md`, `AGENTS.md`, and `config.yaml` into a Hermes profile directory (e.g., `~/.hermes/profiles/crow/`). See the Hermes Agent docs for profile management.

## License

MIT

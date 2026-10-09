# Bevy Harness Research

A comparison of AI coding-agent harnesses for porting a game to the **Bevy engine (Rust)** — researched October 2026.

- `index.html` — the full interactive comparison: per-harness pros/cons, Claude Code fit ranking, local-model delegation guide, and recommendations, all with sources.

## Headline findings

1. **No installable Bevy game-dev harness exists.** Genex (the only true game-dev harness product) is Three.js-only with no Windows build.
2. **Best fit for Claude Code is Claude Code itself** — subagents, hooks (`cargo check`/`clippy` gates), skills, plus Bevy Remote Protocol MCP servers for live game inspection.
3. **Local AI delegation works** via a LiteLLM proxy with per-tier routing: cheap `haiku`-tier scout subagents run on a local Ollama model, porting work stays on frontier models.

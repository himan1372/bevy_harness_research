# Bevy Harness Research

Research notes for porting a game to the **Bevy engine (Rust)** with Claude Code — October 2026.

## Pages

- [Harness comparison](https://himan1372.github.io/bevy_harness_research/) (`index.html`) — per-harness pros/cons, Claude Code fit ranking, local-model delegation guide, and recommendations, all with sources.
- [Recommended skills](https://himan1372.github.io/bevy_harness_research/skills.html) (`skills.html`) — the skill stack for Rust + Bevy development: what to install, what to write, what to skip, plus a task-coordination system so agents don't duplicate work.

## Headline findings

1. **No installable Bevy game-dev harness exists.** Genex (the only true game-dev harness product) is Three.js-only with no Windows build.
2. **Best fit for Claude Code is Claude Code itself** — subagents, hooks (`cargo check`/`clippy` gates), skills, plus Bevy Remote Protocol MCP servers for live game inspection.
3. **Local AI delegation works** via a LiteLLM proxy with per-tier routing: cheap `haiku`-tier scout subagents run on a local Ollama model, porting work stays on frontier models.

# OpenCode Go Swarm

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platform: OpenCode Go](https://img.shields.io/badge/Platform-OpenCode%20Go-blue.svg)](https://opencode.ai)

Minimalist config for **OpenCode Go** subscribers ($10/mo). Orchestrator routes tasks to specialized models automatically.

## The Team

| Agent | Model | Weekly Quota | Temperature | Purpose |
|-------|-------|--------------|-------------|---------|
| Orchestrator | M2.5 | ~50k | 0.1 | Routes tasks |
| Build | M2.7 | ~35k | 0.2 | Daily coding (80% of tasks) |
| Plan | GLM-5 | ~2.8k | 0.3 | Complex logic, escalations |
| Math | Kimi K2.5 | ~4.6k | auto (1.0) | Algorithms, math |
| Docs | M2.5 | ~50k | 0.2 | Boilerplate, tests |

**Quota Strategy:** M2.5 and M2.7 handle ~85k requests/week combined. GLM-5 and Kimi are reserved for their specialties.

## Setup

1. **Copy Files**: Move `opencode.json` and `agents/` to your config directory.
   * **Windows**: `%USERPROFILE%\.config\opencode\`
   * **Linux/Mac**: `~/.config/opencode/`
2. **Add Keys**: Paste your `GITHUB_TOKEN` and `CONTEXT7_API_KEY` into `opencode.json`.
3. **Launch**: Run `opencode`. The Orchestrator loads by default.

## ⚠️ Security

**Never commit `opencode.json` with real keys.** The `.gitignore` excludes it by default.

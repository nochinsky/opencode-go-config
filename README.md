# OpenCode Go Swarm

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platform: OpenCode Go](https://img.shields.io/badge/Platform-OpenCode%20Go-blue.svg)](https://opencode.ai)

Minimalist config for **OpenCode Go** subscribers ($10/mo). This setup uses an Orchestrator to automatically pick the best model for your task so you don't have to manual-swap.

## The Team
* **Orchestrator (M2.5)**: The manager. Handles routing and research.
* **Build (M2.7)**: Your daily workhorse for 80% of coding tasks.
* **Plan (GLM-5)**: The architect. High reasoning for "hard mode" logic and deep debugging.
* **Math (Kimi K2.5)**: The specialist for algorithms and complex CSS/math logic.
* **Docs (M2.5)**: Fast boilerplate, unit tests, and documentation.

## Setup
1. **Copy Files**: Move `opencode.json` and the `agents/` folder to your config directory.
   * **Windows**: `%USERPROFILE%\.config\opencode\`
   * **Linux/Mac**: `~/.config/opencode/`
2. **Add Keys**: Open `opencode.json` and paste your `GITHUB_TOKEN` and `CONTEXT7_API_KEY` into the environment blocks.
3. **Launch**: Just run `opencode`. The Orchestrator loads by default.

## Why this works
* **Saves Money**: Configured to use the $USD billing rate.
* **Zero Interruption**: Permissions are set to `allow` for reads, git, and npm to stop popup fatigue in Zed.
* **Quota Efficiency**: Uses cheap M2.5 for "thinking" and routing, saving your heavy-hitter credits for actual code.

## ⚠️ Security
**Never commit your `opencode.json` once your keys are inside.** Check the `.gitignore` before you push.

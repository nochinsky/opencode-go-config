# OpenCode Go Native Agent Config

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platform: OpenCode Go](https://img.shields.io/badge/Platform-OpenCode%20Go-blue.svg)](https://opencode.ai)

Minimalist config for **OpenCode Go** subscribers ($10/mo). Uses native agent routing to assign the right model for each task.

## Architecture

OpenCode Go's built-in agent system automatically routes tasks to specialized agents. Each agent type has a dedicated model optimized for its workload.

| Agent | Model | Temperature | Purpose |
|-------|-------|-------------|---------|
| `build` | M2.7 | 0.3 | Daily coding tasks |
| `general` | M2.7 | 0.3 | General tasks |
| `debug` | GLM-5 | 0.0 | Complex debugging with high reasoning |
| `plan` | Kimi K2.5 | 0.1 | Task planning |
| `explore` | M2.5 | 0.0 | Codebase exploration |
| `summary` | M2.5 | 0.0 | Summarization |
| `compaction` | M2.5 | 0.0 | Context compaction |
| `title` | M2.5 | 1.0 | Title generation |

## Features

- **Native Agent Routing**: OpenCode Go's built-in task distribution
- **Auto Compaction**: Context is automatically pruned when approaching limits (15000 token reserve)
- **MCP Integration**: GitHub and Context7 tools enabled
- **Auto Updates**: Config syncs automatically via `autoupdate: true`

## Setup

1. **Copy Config**: Move `opencode.json` to your config directory.
   - **Windows**: `%USERPROFILE%\.config\opencode\`
   - **Linux/Mac**: `~/.config/opencode/`

2. **Add Keys**: Replace the placeholder tokens in `opencode.json`:
   - `GITHUB_PERSONAL_ACCESS_TOKEN`: Your GitHub PAT
   - `CONTEXT7_API_KEY`: Your Context7 API key

3. **Launch**: Run `opencode`. Agents are automatically routed based on task type.

## Provider Options

```json
"provider": {
  "opencode-go": {
    "timeout": 300000,
    "chunkTimeout": 3000,
    "setCacheKey": true
  }
}
```

- **Timeout**: 5 minute response timeout
- **Chunk Timeout**: 3 second per-chunk timeout
- **Cache Key**: Enabled for improved performance

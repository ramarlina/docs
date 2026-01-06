---
title: Configuration
excerpt: Configure the Repr CLI for your workflow
---

# Configuration

Settings are stored in `~/.repr/config.json`.

```json
{
  "version": 1,
  "auth": {
    "access_token": "...",
    "user_id": "...",
    "email": "user@example.com",
    "authenticated_at": "2025-01-01T00:00:00",
    "litellm_url": "...",
    "litellm_api_key": "..."
  },
  "settings": {
    "default_paths": ["~/code"],
    "skip_patterns": ["node_modules", "venv", ".venv", "vendor", "__pycache__", ".git"]
  },
  "sync": {
    "last_pushed": "2025-01-01T00:00:00",
    "last_profile": "myrepo_2025-01-01"
  },
  "llm": {
    "extraction_model": "gpt-4o-mini",
    "synthesis_model": "gpt-4o",
    "local_api_url": "http://localhost:11434/v1",
    "local_api_key": "ollama"
  }
}
```

### LLM Configuration

Use `repr config-set` to configure models:

```bash
# View current config
repr config

# Set extraction and synthesis models
repr config-set --extraction-model gpt-4o-mini --synthesis-model gpt-4o

# Configure for local Ollama
repr config-set --local-api-url http://localhost:11434/v1 --local-api-key ollama
```

### Environment Variables

- `REPR_DEV=1`: Enable dev mode (use localhost backend).
- `REPR_API_BASE=URL`: Override the API base URL.

### File Locations

- **Config file**: `~/.repr/config.json`
- **Profiles directory**: `~/.repr/profiles/`
- **Cache directory**: `~/.repr/cache/`


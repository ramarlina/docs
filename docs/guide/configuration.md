---
title: Configuration
excerpt: Configure Repr settings and preferences
---

# Configuration

Settings are stored in `~/.repr/config.json`.

```json
{
  "settings": {
    "default_paths": ["~/code"],
    "skip_patterns": ["node_modules", "venv", ".git"]
  },
  "llm": {
    "extraction_model": "gpt-4o-mini",
    "local_api_url": "http://localhost:11434/v1"
  }
}
```

### Environment Variables

- `REPR_LOCAL`: Set to `true` to default to local analysis.
- `REPR_MODEL`: Specify the default local model.
- `OLLAMA_HOST`: Override the default Ollama API endpoint.

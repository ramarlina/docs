---
title: Privacy Options
excerpt: Understand Repr's privacy-first approach to data handling
---

# Privacy Options

Repr is designed with privacy as a first-class citizen.

| Mode | Description | Data Flow |
|------|-------------|-----------|
| **Cloud (ZDR)** | Zero Data Retention | Code sent → analyzed → immediately discarded |
| **Local** | Ollama Integration | Code never leaves your machine |
| **Offline** | Basic Stats Only | No network required, no AI analysis |

### Local LLM Mode (Recommended)

For complete local control, use [Ollama](https://ollama.com/):

```bash
# Pull a model first
ollama pull llama3.2

# Run analysis locally
repr analyze ~/code --local
```

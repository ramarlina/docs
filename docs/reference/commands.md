---
title: Command Reference
excerpt: Complete reference for all Repr CLI commands
---

# Command Reference

### `repr analyze`
Analyze repositories and generate per-repo profiles (auto-pushed unless `--offline`).

```bash
repr analyze <paths...> [OPTIONS]
```

**Options:**
- `--local, -l`: Use local LLM (OpenAI-compatible local endpoint).
- `--model, -m NAME`: Local model name (default: `llama3.2`).
- `--api-base URL`: Custom local LLM API endpoint.
- `--offline`: Metrics-only, no AI, no network, no push.
- `--since TEXT`: Only analyze commits after this point.
- `--json`: Machine-readable output.

### `repr view`
View your generated profile in the terminal.

```bash
repr view [--raw] [--profile NAME] [--json]
```

### `repr push`
Upload your profile to repr.dev.

```bash
repr push [--profile NAME]
```

### Other commands

For the full CLI surface (including `sync`, `repos`, `hook`, `stories`, `status`, `whoami`, `config`, `config-set`), see:

- `/cli/commands`

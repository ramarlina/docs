---
title: Installation
excerpt: Get started with the Repr CLI tool
---

# CLI Installation & Quick Start

The Repr CLI (`repr`) is a developer-focused tool that analyzes your local repositories to build a comprehensive technical profile.

## Installation

Recommended (isolated) via `pipx`:

```bash
pipx install repr-cli
```

Alternative via `pip`:

```bash
pip install repr-cli
```

## Quick Start

### 0. Authenticate (required for cloud + sync/push)

```bash
repr login
```

### 1. Cloud Analysis (Default)
Generate a profile using our cloud engine with Zero Data Retention:

```bash
# Analyze repos in your code directory
repr analyze ~/code
```

### 2. Local Analysis (Privacy-First)
For complete control, use a local LLM via [Ollama](https://ollama.com/):

```bash
# Pull a model first
ollama pull llama3.2

# Run analysis locally
repr analyze ~/code --local
```

### 3. Offline Mode (No AI / No Network)

```bash
repr analyze ~/code --offline
```

## Next Steps

- [Configuration](/cli/configuration)
- [Command Reference](/cli/commands)

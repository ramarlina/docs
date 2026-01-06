---
title: Privacy & Security
excerpt: How Repr protects your data and gives you control
---

# Privacy & Security

Repr is designed with privacy as a first-class citizen. Whether you use the Web Platform or the CLI, you have control over how your data is processed.

## Data Processing Modes

| Mode | Description | Data Flow |
|------|-------------|-----------|
| **Cloud (ZDR)** | Zero Data Retention | Code sent → analyzed → immediately discarded |
| **Local** | Ollama Integration | Code never leaves your machine |
| **Offline** | Basic Stats Only | No network required, no AI analysis |

### Zero Data Retention (Cloud)

When using our cloud services:
1.  **Encryption**: Data is encrypted in transit (TLS 1.3).
2.  **Ephemeral Processing**: Analysis happens in stateless, ephemeral containers.
3.  **Immediate Discard**: Once the profile is generated, the raw code is wiped from memory and disk. We only store the *output* (the structured dossier).

### Local Execution (CLI)

For complete peace of mind, the Repr CLI supports [Ollama](https://ollama.com/), allowing you to run powerful LLMs on your own hardware. In this mode, your code never touches our servers.

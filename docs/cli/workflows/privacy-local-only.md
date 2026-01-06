---
title: Privacy (Local Only)
excerpt: Use repr entirely offline with maximum privacy
---

# Privacy-Focused Workflow (Local Only)

**Goal:** Use repr entirely offline with maximum privacy.

## The Journey

### Step 1: Check Current Privacy Mode

```bash
repr mode
```

### Step 2: Lock to Local-Only Mode

Reversible lock:

```bash
repr privacy lock-local
```

Or permanently disable cloud features:

```bash
repr privacy lock-local --permanent
```

### Step 3: Configure Local LLM

```bash
repr llm configure
```

Detects Ollama automatically, or lets you enter a custom endpoint:

```
Available models:
  1. llama3.2
  2. codellama
Select: 1
```

### Step 4: Test Local LLM Connection

```bash
repr llm test
```

**Output:**
```
Local LLM:
  ✓ Connection successful
  Provider: Ollama
  Model: llama3.2
  Response time: 234ms
```

### Step 5: Generate Stories Locally

```bash
repr generate --local
```

This is the default when not signed in.

### Step 6: Review Privacy Guarantees

```bash
repr privacy explain
```

**Output:**
```
ARCHITECTURE:
  ✓ No background daemons or silent uploads
  ✓ All network calls are foreground, user-initiated
  ✓ No telemetry by default (opt-in only)

LOCAL MODE NETWORK POLICY:
  Allowed: 127.0.0.1, localhost, ::1 (loopback only)
  Blocked: All external network
```

## Using Your Own API Keys (BYOK)

### Add Provider Keys

Your keys are stored securely in your OS keychain, never in config files:

```bash
# OpenAI
repr llm add openai
# API Key: ****

# Or other providers
repr llm add anthropic
repr llm add groq
repr llm add together
```

### Set as Default

```bash
repr llm use byok:openai
```

### Generate with Your Key

```bash
repr generate
```

This calls your provider directly — repr never sits in the middle.

## Privacy Modes Summary

| Mode | Network Access | Data Storage |
|------|----------------|--------------|
| **Local LLM** | Localhost only | Your machine only |
| **BYOK** | Direct to provider | Provider's logs (per their policy) |
| **Cloud** | repr.dev backend | Zero data retention (ZDR) |

## Next Steps

- Configure [Daily Workflow](daily-workflow.md) for automatic local capture
- Learn about [Backup & Migration](backup-migration.md) to keep your data safe


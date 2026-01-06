---
title: Multi-Device Sync
excerpt: Keep stories synchronized across multiple computers
---

# Multi-Device Sync

**Goal:** Keep stories synchronized across multiple computers.

## Setting Up a New Device

### Step 1: Install repr

```bash
pipx install repr-cli
```

### Step 2: Initialize

```bash
repr init ~/code
```

### Step 3: Login with Same Account

```bash
repr login
```

Uses device flow — no password entry in the terminal.

### Step 4: Pull Stories from Cloud

```bash
repr sync
```

**Output:**
```
Syncing with repr.dev...
↓ 23 remote stories to pull
↑ 0 local stories to push
All stories synced
```

## Ongoing Sync Workflow

### Before Starting Work

Pull the latest:

```bash
repr pull
```

### After Working

Do your work, generate stories locally:

```bash
repr generate --local
```

At end of session, push new stories:

```bash
repr push
```

### Or Do Both at Once

```bash
repr sync
```

## Handling Conflicts

### Check Sync Status

```bash
repr status
```

**Output:**
```
Auth: ✓ Signed in as user@example.com
Tracked repos: 5
Stories: 45 (3 unpushed)
```

### Preview What Would Be Pushed

```bash
repr push --dry-run
```

### Push Specific Story

```bash
repr push --story 01ARYZ6S41TSV4RRFFQ69G5FAV
```

## Next Steps

- Set up [Daily Workflow](daily-workflow.md) on your new device
- Review [Privacy settings](privacy-local-only.md) for local-only options


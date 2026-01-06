# Backup & Migration

**Goal:** Back up all data or migrate to a new machine.

## Creating a Backup

### Step 1: Check What You Have

```bash
repr data
```

**Output:**
```
Local Data
Stories: 45 files (2.1 MB)
Profiles: 3 files (340 KB)
Cache: 120 KB
Config: 8 KB
Total: 2.6 MB
Location: /Users/me/.repr/stories
```

### Step 2: Create Full Backup

```bash
repr data backup --output ~/backups/repr-backup-2026-01-05.json
```

**Output:**
```
Backup saved to /Users/me/backups/repr-backup-2026-01-05.json
  Stories: 45
  Profiles: 3
```

## Restoring on a New Machine

### Step 1: Install repr

```bash
pipx install repr-cli
```

### Step 2: Copy Backup File

Transfer the backup file to your new machine via USB, cloud storage, etc.

### Step 3: Restore from Backup

Merge with any existing data:

```bash
repr data restore ~/backups/repr-backup-2026-01-05.json --merge
```

Or replace everything:

```bash
repr data restore ~/backups/repr-backup-2026-01-05.json --replace
```

## Housekeeping

### Clear Cache

Keeps stories and config:

```bash
repr data clear-cache
```

### Check Storage Usage

```bash
repr data
```

## What Gets Backed Up?

- ✅ All stories and their metadata
- ✅ Profile data
- ✅ Configuration settings
- ✅ Repository tracking info
- ❌ Cache (regenerated as needed)
- ❌ API keys (stored in OS keychain)

## Next Steps

- Set up [Multi-Device Sync](multi-device-sync.md) for automatic backups
- Review [Privacy settings](privacy-local-only.md) for data control


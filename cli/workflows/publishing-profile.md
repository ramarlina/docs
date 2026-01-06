# Publishing Your Profile

**Goal:** Create a public developer profile at repr.dev.

## The Journey

### Step 1: Sign In

Cloud features require authentication:

```bash
repr login
```

### Step 2: Set Up Your Profile

```bash
repr profile set-bio "Full-stack engineer specializing in distributed systems"
repr profile set-location "San Francisco, CA"
repr profile set-available true
```

### Step 3: Review What You'll Publish

```bash
repr stories
repr story hide 01ARYZ...  # Hide sensitive stories
repr story feature 01BEST...  # Feature best work
```

### Step 4: Preview Before Publishing

```bash
repr push --dry-run
```

**Output:**
```
Publishing 12 story(ies) to repr.dev...
  • Built OAuth2 integration with Google/GitHub
  • Implemented Redis caching layer
  • Fixed race condition in auth flow
Run without --dry-run to publish
```

### Step 5: Publish Your Stories

```bash
repr push --all
```

### Step 6: Get Your Profile Link

```bash
repr profile link
```

**Output:**
```
Your profile: https://repr.dev/@yourusername
```

## Managing What's Public

### Hide Sensitive Stories

```bash
repr story hide 01SENSITIVE_STORY_ID
```

### Feature Top Stories

Pin a story to the top of your profile:

```bash
repr story feature 01BEST_STORY_ID
```

### Check Privacy Settings

```bash
repr privacy explain
```

### Audit What Was Sent

```bash
repr privacy audit
```

## Next Steps

- Set up [Multi-Device Sync](multi-device-sync.md) to keep stories current
- Review [Privacy settings](privacy-local-only.md) if you prefer local-only mode


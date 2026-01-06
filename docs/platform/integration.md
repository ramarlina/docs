---
title: CLI Integration
excerpt: Bridge your local development environment with the cloud platform
---

# CLI Integration

The power of Repr comes from combining deep local analysis with cloud-based tailoring. The **CLI Integration** bridges these two worlds.

## The Data Flow

1.  **Local Analysis**: You run `repr analyze` on your machine. This extracts metrics, architecture patterns, and complexity scores from your actual code.
2.  **Auto-Push**: Analysis results are automatically pushed to your private profile on repr.dev (for non-offline mode).
3.  **Web Consumption**: In the Workflow Canvas, the **CLI Node** shows your pushed repository profiles, which feed into your generated profile.

## Usage Guide

### 1. Authenticate
First, link your CLI to your web account:

```bash
repr login
# This opens your browser to authenticate and saves a token locally.
```

### 2. Analyze Repositories
Run the analysis on your code directories:

```bash
# Analyze repos (automatically pushes to repr.dev)
repr analyze ~/code

# Use local LLM instead of cloud
repr analyze ~/code --local --model llama3.2

# Offline mode (stats only, no AI, no push)
repr analyze ~/code --offline
```

Each repository is analyzed separately and saved as `{repo_name}_{date}.md`.

### 3. View & Manage Profiles
```bash
# List all profiles
repr profiles

# View latest profile
repr view

# View specific profile
repr view --profile myrepo_2025-12-26
```

### 4. Push Unsynced Profiles
If you ran analysis offline or need to re-push:

```bash
# Push all unsynced profiles
repr push

# Push specific profile
repr push --profile myrepo_2025-12-26
```

### 5. Use in Workflow
1.  Go to the **Workflow Canvas** in the web app.
2.  The **CLI Node** shows your pushed repository profiles.
3.  Click "Generate Profile" to synthesize all your data sources into a comprehensive profile.
4.  Use "Apply to Job" to generate tailored materials for specific positions.

The generator uses your analyzed code as "proof" of your skills (e.g., *"Built a Python API with 95% test coverage"*) to back up your resume claims.

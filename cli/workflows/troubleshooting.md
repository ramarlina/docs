# Troubleshooting

**Goal:** Diagnose and fix issues with repr.

## Health Check

### Run Full Diagnostics

```bash
repr doctor
```

**Output:**
```
Checking repr health...

✓ Config: valid (v3)
✓ Stories: 45 files, no corruption
✓ Local LLM: Ollama (llama3.2)
✓ Git: 2.40.0
⚠ Tracked repos: 1 missing (/old/path/repo)

Recommendations:
  1. Remove missing repo: repr repos remove /old/path/repo
```

## Common Issues

### "Local LLM not found"

**Solution:** Install Ollama and pull a model

```bash
ollama pull llama3.2
repr llm test
```

### "Not authenticated"

**Solution:** Log in or check token

```bash
repr login
# Or check if token is valid
repr whoami
```

### "Repository not tracked"

**Solution:** Add the repository

```bash
repr repos list
repr repos add ~/code/my-repo
```

### "Hook not working"

**Solution:** Check and reinstall hooks

```bash
repr hooks status
repr hooks install --repo ~/code/my-repo
```

### Corrupted config

**Solution:** Edit config manually

```bash
repr config edit  # Opens in $EDITOR
```

### Check what mode you're in

```bash
repr mode
```

### See full configuration

```bash
repr config show
repr config show llm.default
```

## Debugging Commands

### Check Version

```bash
repr --version
```

### Check Auth Status

```bash
repr whoami --json
```

### Check Repo Tracking

```bash
repr repos --json
```

### Check Hook Queue

```bash
repr hooks status --json
```

### View Raw Config

```bash
repr config show --json
```

### Privacy Audit

```bash
repr privacy audit --days 7 --json
```

## Getting Help

- **GitHub Issues:** [github.com/repr-app/cli/issues](https://github.com/repr-app/cli/issues)
- **Community:** Join discussions in the repo
- **Docs:** Check other workflow guides for specific features

## Next Steps

- Review [Configuration guide](../configuration.md) for advanced settings
- Check [Privacy settings](privacy-local-only.md) if experiencing auth issues


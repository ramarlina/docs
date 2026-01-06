# Interview Prep

**Goal:** Create interview-ready stories from your actual work using the STAR format.

## The Journey

### Step 1: Generate Interview-Style Stories

```bash
repr generate --template interview --local
```

### Step 2: Review STAR-Format Stories

```bash
repr stories
```

### Step 3: View Specific Stories

```bash
repr story view 01ARYZ6S41TSV4RRFFQ69G5FAV
```

**Output format:**
```
**Situation:** The authentication system was experiencing...
**Task:** I needed to implement a more robust...
**Action:** I designed and implemented...
**Result:** Reduced authentication failures by 60%...
```

### Step 4: Feature Your Best Stories

```bash
repr story feature 01ARYZ6S41TSV4RRFFQ69G5FAV
```

### Step 5: Export for the Interview

```bash
repr profile export --format md > interview-prep.md
```

### Step 6: Generate from Specific Projects

```bash
repr generate --repo ~/code/important-project --template interview
```

## Advanced Tips

### Custom Focus Areas

Generate stories with extra context:

```bash
repr generate --template interview --prompt "Focus on leadership and technical decision-making"
```

### Filter by Technology

```bash
repr stories --json | jq '.[] | select(.technologies | contains(["Python"]))'
```

### Export Only Featured Stories

```bash
repr stories --json | jq '[.[] | select(.is_featured == true)]'
```

## What is STAR Format?

**S**ituation - Context and background
**T**ask - What needed to be done
**A**ction - What you specifically did
**R**esult - Measurable impact and outcomes

This format is widely used in behavioral interviews at top tech companies.

## Next Steps

- [Publish your profile](publishing-profile.md) for recruiter discovery
- Use [Weekly Reflection](weekly-reflection.md) to keep stories updated


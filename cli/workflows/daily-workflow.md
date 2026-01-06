# Daily Workflow

**Goal:** Automatically capture your daily work with minimal friction.

## Approach A: Automatic Hook-Based Capture

### One-Time Setup

Install git hooks in your repositories:

```bash
repr hooks install --all
```

Now, every git commit is automatically queued (the hook runs silently, no network calls).

### Daily Routine

At end of day or week, generate stories from queued commits:

```bash
repr generate --local
```

Review what was generated:

```bash
repr stories --needs-review
```

### Interactive Review

```bash
repr review
```

**Options:**
- `[a]` Approve
- `[e]` Edit
- `[r]` Regenerate
- `[d]` Delete
- `[s]` Skip
- `[q]` Quit

## Approach B: Manual Daily Standup

Quick standup summary (last 3 days):

```bash
repr standup
```

**Output:**
```
📊 Work since last 3 days
myproject (8 commits):
  • Add user authentication flow
  • Fix session timeout bug
  • Implement rate limiting
Total: 8 commits

This summary wasn't saved. Run with --save to create a story.
```

## Approach C: End-of-Day Capture

Check what you did today:

```bash
repr since "this morning"
```

Save it as a story:

```bash
repr since "this morning" --save
```

Or generate from specific commits:

```bash
repr commits --limit 5
# Shows recent commits with SHAs

repr generate --commits abc1234,def5678,ghi9012
```

## Key Commands

| Command | Purpose |
|---------|---------|
| `repr hooks install --all` | Set up auto-capture |
| `repr generate` | Create stories from queued commits |
| `repr standup` | Quick 3-day summary |
| `repr since <date>` | Work since specific time |
| `repr review` | Interactive story review |

## Next Steps

- Set up [Weekly Reflection](weekly-reflection.md) to polish your best work
- Use different [templates](weekly-reflection.md#template-options) for various contexts


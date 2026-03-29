# Weekly Reflection — Finn

Run every Sunday or after testing 3+ POCs.

## 0. Review daily logs

Check `memory/` for files named `YYYY-MM-DD.md`. If none exist, write "no daily logs yet" and skip to step 1. If they exist, read the last 7 days. Look for **config/process gaps** — situations where your current rules or prompts didn't cover what came up.

## 1. Review recent QA cycles

- Did your QA cycles catch real issues before Max got the POC?
- Were there false positives (flagging things that weren't actually broken)?
- Were there false negatives (issues that slipped through to Max or users)?
- How many cycles did ventures need on average? Are Louise's builds improving?
- Did you test from the sprint contract, or did you freestyle?

## 2. Audit your files

| File | What to check |
|------|---------------|
| `agents/finn.md` | Testing scope — anything you consistently do differently than what's written? |
| `agents/finn-ref.md` | Report format — what do Louise and Max actually read? |
| `SOUL.md` | Operating principles — any that slow you down without improving test quality? |
| `HEARTBEAT.md` | Missing checks for new patterns? |

## 3. Update rules

| File | Who approves |
|------|-------------|
| `agents/finn.md` — role/scope | Flag to Steve before committing |
| `agents/finn-ref.md` — report templates | Autonomous |
| `SOUL.md` | Autonomous |
| `HEARTBEAT.md` | Autonomous |

Only update a file if you have concrete evidence from actual work. Do not speculate.

## 4. Update `ventures/knowledge/`

Skip this step if no QA work happened this week.

- `patterns/` — hypothesis types that are inherently hard to QA via browser testing?
- Common failure patterns worth documenting for Louise?

Delete any stubs (files with only "None yet" fields).

## 5. Commit and report

```bash
git add [changed files only]
git commit -m "reflection: [date] — [one-line summary]"
git push
```

Post a one-line summary to Steve's channel (channel:1483825159415664700).

Nothing changed? Say so — note what you verified and why it still holds.

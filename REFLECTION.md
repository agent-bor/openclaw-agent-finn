# Weekly Reflection — Finn

Run every Sunday or after testing 3+ POCs.

## 1. Review recent QA cycles
- Did your QA cycles catch real issues before Max got the POC?
- Were there false positives (flagging things that weren't actually broken)?
- Were there false negatives (issues that slipped through to Max or users)?
- How many cycles did ventures need on average? Are Louise's builds improving?
- Did you test from the sprint contract, or did you freestyle?

## 2. Audit your files

| File | What to check |
|------|---------------|
| `agents/qa.md` | Testing scope — anything you consistently do differently than what's written? |
| `agents/qa-ref.md` | Report format — what works in practice? What do Louise and Max actually read? |
| `SOUL.md` | Operating principles — any that slow you down without improving test quality? |
| `HEARTBEAT.md` | What should you track between sessions? New test patterns, blockers? |

## 3. Update rules

| File | Who approves |
|------|-------------|
| `agents/qa.md` — role/scope | Flag to Steve before committing |
| `agents/qa-ref.md` — report templates | Autonomous |
| `SOUL.md` | Autonomous |
| `HEARTBEAT.md` | Autonomous |

## 4. Update `ventures/knowledge/`

**Only do this step if you tested POCs this week** (check memory/ — daily logs must exist with QA activity). If no active work, skip entirely.

- `hypothesis-patterns.md` — any hypothesis types that are inherently hard to QA via browser testing?
- Common failure patterns worth documenting for Louise?

## 5. Commit your changes

```bash
cd ${OPENCLAW_ROOT:-.}/workspace-qa
git add -p
git commit -m "reflection: [date] — [one-line summary]"
git push
```

## 6. Ping Steve
Note what changed in your QA approach and what evidence drove it.

---
*Nothing changed? That's fine — note what you verified and why it still holds.*

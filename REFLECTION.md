# Weekly Reflection — Finn

Run every Sunday or after testing 3+ POCs.

## 0. Post-mortem: find what broke or slowed down

**0A — Scan git log for rework signals:**
```bash
git log --oneline --since="7 days ago"
```
Flag commits with: "fix", "retry", "redo", "correct", "revert", or re-runs of the same QA cycle.

**0B — Read the session compact** (created by compact-sessions.sh). Look for:
- QA cycles you had to run more than once on the same POC
- False positives — things you flagged as broken that were actually fine
- False negatives — bugs that slipped through to Max or users
- Tests you ran that weren't based on the sprint contract (freestyling)

**0C — Check QA accuracy:**
- How many issues did you catch before Max got the POC vs. after?
- Which issue categories keep recurring (same Louise build pattern, same test gap)?
- Were your QA reports clear enough that Louise could fix without back-and-forth?
- Did you test from the sprint contract, or did scope drift into your test plan?
- How many cycles did ventures need on average? Are Louise's builds improving?

**0D — Write diagnosis to `memory/YYYY-MM-DD-postmortem.md`:**
- What false positive or false negative happened? What caused it?
- Root cause: test coverage gap, wrong test scope, Louise's build pattern you hadn't seen before, missing checklist item?
- What would catch this earlier next time?

If nothing to diagnose: write "clean week — no rework detected" and continue.

**0E — Self-patch protocol:**
- Observation only → write to `memory/` (additive, safe)
- High-confidence fix (same QA failure 2+ times) → propose change to `AGENTS.md`, flag to Steve before committing
- Test checklist/report format fix → update `agents/finn-ref.md` autonomously

## 1. Audit your files

| File | What to check |
|------|---------------|
| `AGENTS.md` | Testing scope — anything you consistently do differently than what's written? Steps that slow you down? |
| `agents/finn-ref.md` | Report format and test checklist — what do Louise and Max actually read vs. skim? |
| `SOUL.md` | Operating principles — any that slow you down without improving test quality? |
| `HEARTBEAT.md` | Missing checks for new build patterns or stack choices Louise introduced? |

## 2. Update rules

| File | Who approves |
|------|-------------|
| `AGENTS.md` — role/scope | Flag to Steve before committing |
| `agents/finn-ref.md` — report templates | Autonomous |
| `SOUL.md` | Autonomous |
| `HEARTBEAT.md` | Autonomous |

Only update a file if you have concrete evidence from actual work. Do not speculate.

## 3. Update `ventures/knowledge/`

Skip if no QA work happened this week.

- `ventures/knowledge/patterns/` — hypothesis types that are inherently hard to QA via browser testing? Common failure modes worth documenting for Louise?

Delete stubs (files with only "None yet" fields).

## 4. Commit and report

```bash
git add [changed files only]
git commit -m "reflection: [date] — [one-line summary]"
git push
```

`exec` → `openclaw agent --agent main --message "reflection [date]: [one-line summary of what changed or was verified]"`

Nothing changed? Say so — note what you verified and why it still holds.

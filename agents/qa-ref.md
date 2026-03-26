# Finn — Reference (load when writing QA reports)

## QA report format (passing)

Save to `ventures/[venture-id]/build/qa-report.md`.

```
## QA Report: [Project Name]
**Date:** [date] | **QA cycle:** [N] | **Verdict:** PASSED
**Live URL:** [url] | **Build report:** ventures/[id]/build/build-report.md

### P0 Results
| # | Criterion | Result | Notes |
|---|-----------|--------|-------|
| 1 | [criterion] | ✅ PASS | [observation] |
| 2 | [criterion] | ✅ PASS | [observation] |

### P1 Results (non-blocking)
| # | Criterion | Result | Notes |
|---|-----------|--------|-------|
| 1 | [criterion] | ✅ PASS / ⚠️ FAIL | [observation] |

### P1 issues for Max
- [issue and suggested fix or workaround]

### Screenshots / evidence
- [description of what was observed at each key step]
```

---

## QA feedback format (failing)

Save to `ventures/[venture-id]/build/qa-feedback.md`. Louise reads this file before starting her fix pass.

```
## QA Feedback: [Project Name] — Cycle [N]
**Date:** [date] | **QA analyst:** Finn | **Verdict:** FAILED

### Summary
[1-2 sentences: what broke, what couldn't be validated]

### P0 Failures — fix these before resubmitting

#### [Criterion name]
- **What I did:** [exact steps taken in the browser]
- **Expected:** [what should have happened]
- **Actual:** [what actually happened — be specific]
- **Fix required:** [specific change needed]

#### [Next P0 failure]
...

### P1 Issues (fix if quick, document if not)
- [issue]: [observation]

### What to leave alone
- [things that passed — don't break them in the fix pass]

### Next QA cycle focus
[What Louise should prioritize; what I'll test first in cycle N+1]
```

---

## Sprint contract format

Louise writes this BEFORE building. Save to `ventures/[venture-id]/build/sprint-contract.md`.

```
## Sprint Contract: [Project Name]
**Date:** [date] | **Engineer:** Louise | **QA cycle:** [N]
**Design spec:** ventures/[id]/design/design-spec.md
**Live URL:** (filled after deploy)

### What will be built
[2-3 sentences: scope for this build/fix pass, specifically what user flows will be implemented]

### P0 Acceptance criteria — must pass before handoff to Max
| # | Feature | How to verify in browser |
|---|---------|--------------------------|
| 1 | [feature name] | [step: navigate to X, do Y, expect Z] |
| 2 | ... | ... |

### P1 Acceptance criteria — document if missing, don't block
| # | Feature | How to verify in browser |
|---|---------|--------------------------|
| 1 | [feature name] | [step] |

### Explicitly out of scope for this build
- [item]
```

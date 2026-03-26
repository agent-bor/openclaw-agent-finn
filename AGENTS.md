# Other Agents — Reference

Who does what. Use this to know who to escalate to, who hands off to you, and who you hand off to.

## Steve 🎯 — Operations Lead
- **Channel:** `1483825159415664700`
- **Does:** Orchestrates the pipeline, resolves blockers, manages ops tickets
- **When to contact:** Tool failures, infra issues, blocked QA, anything that needs ops resolution
- **Escalate to Steve when:** browser/exec tools fail, live URL is down, unclear ticket state

## Hunter 🔍 — Market Researcher
- **Channel:** `1483825178336039012`
- **Does:** Finds and evaluates venture ideas, runs signal scans
- **Interaction:** Upstream — Hunter finds ideas that eventually become POCs you test

## Vladi 📊 — Business Analyst
- **Channel:** `1483825305763450983`
- **Does:** Scores hypotheses, validates market data, produces scorecards
- **Interaction:** Upstream — Vladi's scorecard informs what gets built

## Adam 🎨 — Product Designer
- **Channel:** `1483825238151139442`
- **Does:** Creates design specs, defines user flows and acceptance criteria
- **Interaction:** Adam's design spec defines expected UX — reference it when testing

## Louise 💻 — Product Engineer
- **Channel:** `1483825204659749016`
- **Does:** Builds POCs from design specs, deploys to Vercel, writes sprint contracts
- **Interaction:** Louise builds what you test. QA failures go back to Louise with specific feedback via qa-feedback.md. Louise reads your feedback file and fixes.

## Max 🚀 — Growth Lead
- **Channel:** `1483825252760027186`
- **Does:** Acquires users, designs channel experiments, measures traction
- **Interaction:** Downstream — when QA passes, you advance the ticket to `max-briefed` and notify Max with the live URL and QA report

---

## Pipeline flow (your position)

```
Hunter → Vladi → Adam → Louise → **Finn (you)** → Max
```

You are the quality gate between build and growth. Nothing reaches Max without passing through you.

# Heartbeat — Finn (QA Analyst)

- Scan `../../ventures/*/TICKET.md`. Is any in stage `qa-briefed` with no active task in `memory/tasks.md`? Read the build report and sprint contract and start testing now.
- Is any active QA test blocked by something that will delay delivery >4 hours? Escalate immediately to Steve and Lukas with specifics.
- If you hit a blocker (browser failure, live URL down, broken tool): **do NOT delete work.** Keep all files. If the blocker is venture-specific, update that TICKET.md `blocker:` field. If it's an ops/infra issue, create a ticket at `ventures/tickets/t-[slug].md` using the ops-ticket template. Message Steve with what's done and what's blocking.
- If no active QA tasks and no blockers — reply HEARTBEAT_OK.
- Weekly: if directly asked to reflect, run `skills/self-reflection/SKILL.md`. Do not auto-run reflection from heartbeats or generic trigger phrases.

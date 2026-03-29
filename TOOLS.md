# TOOLS.md - Local Notes

## GitHub

- **Account:** agent-bor
- **Auth:** PAT configured in `~/.git-credentials` — git operations work without extra setup
- **Token:** `GITHUB_TOKEN` env var — loaded automatically by OpenClaw from `~/.openclaw/.env`
- **API calls:** `curl -H "Authorization: Bearer $GITHUB_TOKEN"`
- **Workspace repo:** https://github.com/agent-bor/openclaw-agent-finn

## Browser

- Primary testing tool — all QA must happen via live app, not code inspection
- Screenshot key steps for evidence in QA reports
- React 🔄 every ~5 browser actions to show progress

## Shared ventures vault

- **Path:** `ventures/`
- **Always use absolute paths** when writing here
- Structure: `/../ventures/[project-name]/[research|validation|decisions|design|build|growth]/`

## Memory (QMD)

- **NEVER create `.sqlite`, `.db`, or `.sql` files — all persistence is `.md` in `memory/`**
- Indexes this workspace's `memory/` + the shared ventures vault automatically
- Scope: DM sessions only (not exposed in Discord channels)

## Git identity

- `user.name`: agent-bor
- `user.email`: agent@openclaw

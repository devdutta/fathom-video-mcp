# Fathom MCP Server — Setup Reference

## What This Is
Local MCP server connecting Fathom AI meeting data to Claude Code CLI.
Repo: https://github.com/trevorwelch/fathom-video-mcp

## Available MCP Tools
| Tool | Description |
|------|-------------|
| `list_meetings` | List meetings with filters (date, team, search, recorder) |
| `get_summary` | AI-generated summary for a specific recording |
| `get_transcript` | Full transcript with speaker attribution & timestamps |

## Configuration
- **MCP config location:** `~/.claude/settings.json`
- **API key:** Stored as env var `FATHOM_API_KEY`
- **API key management:** https://fathom.video/api_settings
- **Server location:** `D:\Claude_Code_Test\Tools\fathom-mcp\`

## Useful Filters for list_meetings
- `created_after` / `created_before` — ISO timestamps for date range
- `recorded_by` — Filter by recorder email
- `teams` — Filter by team name
- `invitee_domains` — Filter by attendee company domain (e.g., "acme.com")
- `search` — Smart search across titles, attendee names, email domains

## Troubleshooting
| Issue | Fix |
|-------|-----|
| MCP not loading | Run `/mcp` in Claude Code to check. Restart Claude Code. |
| Auth error | Verify API key: `echo $FATHOM_API_KEY` |
| No meetings | Fathom needs to record at least one meeting first |
| uv not found | Install: `irm https://astral.sh/uv/install.ps1 \| iex` |

## Fathom Resources
- Dashboard: https://fathom.video
- API Docs: https://developers.fathom.ai
- API Settings: https://fathom.video/api_settings

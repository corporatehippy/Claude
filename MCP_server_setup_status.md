# MCP Server Setup Status

*Tracks which MCP servers are configured, on which machines, and what's pending.*

*Last updated: April 15, 2026*

---

## How MCP Servers Work (Quick Reference)

MCP servers run **locally on each machine** via the Claude Desktop app — they are NOT tied to your Claude.ai account in the cloud. This means:

- Each machine needs its own setup
- The config file lives at a machine-specific path (see below)
- The same Personal Access Token can be reused across machines
- Claude Desktop must be fully quit and relaunched after any config change

**Config file locations:**
- Mac: `~/Library/Application Support/Claude/claude_desktop_config.json`
- Windows (standard): `%APPDATA%\Claude\claude_desktop_config.json`
- Windows (MSIX/Store-style install): `C:\Users\<username>\AppData\Local\Packages\Claude_pzs8sxrjxfjjc\LocalCache\Roaming\Claude\claude_desktop_config.json`

> ⚠️ **Windows gotcha:** Even if you installed Claude Desktop via the .msi from claude.ai (not the Windows Store), it may still install as an MSIX package and use filesystem virtualization. If the config isn't loading, check the logs at `C:\Users\<username>\AppData\Local\Claude\logs\` — look for the line `[MSIX] Filesystem virtualization active` to confirm which path applies. **Check the logs first.**

**Prerequisite for all machines:** Node.js must be installed (`node --version` in terminal to check)

---

## MCP Servers Configured

### GitHub MCP Server
**Package:** `@modelcontextprotocol/server-github`
**Purpose:** Read and write to GitHub repos directly from Claude Desktop — used to push/pull project state docs and prompt library

**Config block:**
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "your-token-here"
      }
    }
  }
}
```

**Token permissions needed:** `repo` (full repository access — check the `repo` box when generating a classic token)
*(Token is stored in your password manager — do not paste it into this doc)*

| Machine | OS | Status | Notes |
|---|---|---|---|
| Mac Mini | macOS | ✅ Configured and working | Primary machine, set up April 2026 |
| Windows PC | Windows 11 | ✅ Configured and working | Set up April 15, 2026. Config lives in MSIX virtualized path — see Windows gotcha above |
| MacBook / other Mac | macOS | ⏳ Pending | Same token, same config |

---

## MCP Servers Planned / Under Consideration

| Server | Purpose | Status |
|---|---|---|
| *(none identified yet)* | | |

*Add servers here as they're identified. Good candidates to consider: filesystem access, calendar, Notion, etc.*

---

## Setup Checklist (for each new machine)

- [ ] Claude Desktop app installed and signed in
- [ ] Node.js installed — verify with `node --version`
- [ ] Config file located at correct path for OS (check logs if unsure — look for MSIX virtualization line)
- [ ] JSON config block added with correct token
- [ ] Claude Desktop fully quit and relaunched (verify no processes running in Task Manager)
- [ ] Verified by asking Claude: "Can you see my GitHub repos?"
- [ ] Update status table in this doc

---

## Open Questions

- What other MCP servers might be useful? (Consider: DaVinci Resolve workflows, Stream Deck integration, file system access for project files)
- Should the MacBook config include any additional servers beyond GitHub from the start?

---

## Troubleshooting Notes

- **Always check the logs first.** Location: `C:\Users\<username>\AppData\Local\Claude\logs\` (Windows) or `~/Library/Logs/Claude/` (Mac)
- **Windows MSIX path:** If Claude Desktop isn't loading your config, the MSIX filesystem virtualization is the most likely culprit. The log line `[MSIX] Filesystem virtualization active` confirms it and shows the real path.
- **Token exposed accidentally?** Revoke immediately in GitHub → Settings → Developer Settings → Personal Access Tokens, then generate a new one.

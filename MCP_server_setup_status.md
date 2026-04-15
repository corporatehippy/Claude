# MCP Server Setup Status

*Tracks which MCP servers are configured, on which machines, and what's pending.*

*Last updated: April 2026*

---

## How MCP Servers Work (Quick Reference)

MCP servers run **locally on each machine** via the Claude Desktop app — they are NOT tied to your Claude.ai account in the cloud. This means:

- Each machine needs its own setup
- The config file lives at a machine-specific path (see below)
- The same Personal Access Token can be reused across machines
- Claude Desktop must be fully quit and relaunched after any config change

**Config file locations:**
- Mac: `~/Library/Application Support/Claude/claude_desktop_config.json`
- Windows: `%APPDATA%\Claude\claude_desktop_config.json`

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

**Token:** Fine-grained Personal Access Token with `Contents: Read and Write` on the `corporatehippy/Claude` repo
*(Token is stored in your password manager — do not paste it into this doc)*

| Machine | OS | Status | Notes |
|---|---|---|---|
| Mac Mini | macOS | ✅ Configured and working | Primary machine, set up April 2026 |
| Windows PC | Windows | ⏳ Pending | Same token, same config — just needs Node.js check and config file edit |
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
- [ ] Config file located at correct path for OS
- [ ] JSON config block added with correct token
- [ ] Claude Desktop fully quit and relaunched
- [ ] Verified by asking Claude: "Can you see my GitHub repos?"
- [ ] Update status table in this doc

---

## Open Questions

- What other MCP servers might be useful? (Consider: DaVinci Resolve workflows, Stream Deck integration, file system access for project files)
- Should the Windows PC config include any additional servers beyond GitHub from the start?

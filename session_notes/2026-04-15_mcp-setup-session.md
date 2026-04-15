# MCP Setup Session — April 15, 2026

## What We Did This Session

- Confirmed that Marty's GitHub connection is a **locally-run MCP server** (not a cloud connector), configured via the Claude Desktop app using `npx @modelcontextprotocol/server-github`
- Clarified that this means each machine needs its own setup — the config does NOT follow the account
- Created `MCP_server_setup_status.md` to track server status across all machines
- Added **Section 4A** to `prompt_library.md` for MCP setup/troubleshooting sessions
- Also created `adhd_athlete_kitchen_plan.md` and the initial `prompt_library.md` earlier in this session (first push of those files from the docx)

## Windows PC Setup — What To Do Next

1. **Check Node.js** — open Command Prompt and run `node --version`. If not installed, go to nodejs.org and grab the LTS version.
2. **Find the config file** — navigate to `%APPDATA%\Claude\claude_desktop_config.json` (paste that path directly into File Explorer's address bar)
3. **Add the config block** — paste this in, with your token from your password manager:

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

4. **Fully quit and relaunch** Claude Desktop
5. **Verify** by asking Claude: "Can you see my GitHub repos?" — you should see `corporatehippy/Claude`
6. Update the machine status table in `MCP_server_setup_status.md`

## Repo State at End of Session

| File | Status |
|---|---|
| `adhd_athlete_kitchen_plan.md` | ✅ Pushed |
| `prompt_library.md` | ✅ Updated (added section 4A, How to Use entry for MCP) |
| `MCP_server_setup_status.md` | ✅ Created |
| `dip-film_project_state.md` | Exists from prior sessions — not touched today |

## If You Get Stuck on Windows

Paste prompt **4A** from the prompt library and attach or reference `MCP_server_setup_status.md` — that session context will get Claude up to speed immediately.

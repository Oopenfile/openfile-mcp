# OpenFile MCP server

Connects your AI agent to [OpenFile](https://joinopenfile.com?ref=gh-openfile-mcp), which forms U.S. companies in all 50 states and files U.S. trademarks through a licensed attorney.

The agent can look up any state's filing fees and annual report rules, quote a formation or trademark with every government fee on its own line, screen a brand name, search live USPTO records, suggest trademark classes, and save a draft formation or application. Each draft comes back as a review link: the owner checks it, signs and pays on joinopenfile.com. Nothing is filed or charged from the agent.

No account or API key is needed.

## Add it

**Cursor:** install the plugin from the Cursor Marketplace, or add this to `.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "openfile": {
      "url": "https://mcp.joinopenfile.com"
    }
  }
}
```

**Claude Code:** `claude mcp add --transport http openfile https://mcp.joinopenfile.com`

**Any other client:** a remote MCP server at `https://mcp.joinopenfile.com` (streamable HTTP, no auth).

## Things to ask

- What does it cost to form an LLC in Texas, including the state fee?
- Search the USPTO for trademarks named Brightloop.
- Which trademark classes fit a coffee subscription business?
- Start a Wyoming LLC called Brightloop Coffee LLC and give me the link to sign.

## Tools

27 tools: 22 read-only (`get_state`, `list_states`, `quote_formation`, `quote_application`, `screen_mark`, `search_marks`, `suggest_classes`, `plan_task`, `search_docs` and more) and 5 that save or edit drafts (`create_formation`, `update_formation`, `create_application`, `update_application`, `add_specimen`). Full list: https://joinopenfile.com/docs/mcp?ref=gh-openfile-mcp

## Contents

- `.cursor-plugin/plugin.json`: Cursor plugin manifest.
- `mcp.json`: the remote server.
- `skills/openfile/SKILL.md`: how an agent should use the tools.
- `assets/logo.png`: logo.

U.S. companies and U.S. trademarks only. OpenFile isn't a law firm and this is not legal advice. Support: support@joinopenfile.com

## License

MIT

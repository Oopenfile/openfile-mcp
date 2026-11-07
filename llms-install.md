# Installing the OpenFile MCP server in Cline

OpenFile is a remote MCP server. There is nothing to download, build or run locally, and no account or API key is needed.

- Server URL: `https://mcp.joinopenfile.com`
- Transport: streamable HTTP (`"type": "streamableHttp"`)
- Auth: none

## Steps

1. Add this entry to `cline_mcp_settings.json` under `mcpServers`. Keep any servers already there.

```json
{
  "mcpServers": {
    "openfile": {
      "type": "streamableHttp",
      "url": "https://mcp.joinopenfile.com",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

2. Set `"type": "streamableHttp"` explicitly. Without it Cline uses the legacy SSE transport and the connection fails.
3. Check the connection: call `list_states` (read-only). A list of U.S. states means it works.

## Notes for using the tools

- Before preparing anything, call `plan_task` with the user's words and ask its questions the user hasn't answered. Don't fill in owners, addresses, states, company types or trademark classes yourself.
- Never say a company or trademark name is available. `screen_mark` and `search_marks` are not a legal opinion.
- Drafts come back as a `review_url`. Only the owner signs and pays, on joinopenfile.com. Never sign or confirm for them.
- OpenFile isn't a law firm and this is not legal advice.

Docs: https://joinopenfile.com/docs/mcp

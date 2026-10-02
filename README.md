# STREEQ and TRAINEDBY plugins

Official plugins that connect your AI to the hosted MCP servers for [STREEQ](https://streeq.app) and [TRAINEDBY](https://www.trainedby.fit). One repo, three formats:

- **Cursor and Grok Bot:** `.cursor-plugin/` (Grok Bot uses the same plugins as Cursor)
- **Grok Build:** `.grok-plugin/`
- Any MCP client: use the URLs below

These plugins run no local code. They point your AI at the official HTTPS MCP servers, and you sign in with your own STREEQ or TRAINEDBY account. No API keys or tokens are stored in this repo.

| Plugin | Who it is for | MCP URL | Docs |
| --- | --- | --- | --- |
| `streeq` | People keeping their own fitness record | `https://mcp.streeq.app/streeq/mcp` | https://streeq.app/connect-ai |
| `trainedby` | Coaches | `https://mcp.trainedby.fit/mcp` | https://www.trainedby.fit/connect-ai |

## Install

**Cursor and Grok Bot:** find **STREEQ** or **TRAINEDBY** in the plugin marketplace and choose Add. Before it is listed, add this repo as a team marketplace or add the MCP URL as a custom server.

**Grok Build:**

```bash
grok plugin marketplace add theaverageapp/grok-plugins
grok plugin install streeq --trust
grok plugin install trainedby --trust
```

**Grok (grok.com):** grok.com/connectors, New Connector, Custom, then paste the MCP URL.

## Sign-in

Both servers use OAuth 2.1 with PKCE. The sign-in service is `https://mcp.trainedby.fit` (advertised in each server's protected-resource metadata). Each server asks only for the permissions listed on its sign-in screen.

## License

MIT. STREEQ and TRAINEDBY are products of TRAINEDBY FIT LTD.

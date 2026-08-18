# Grok plugins for TRAINEDBY and STREEQ

Public Grok Build plugins that attach the hosted MCP servers for [TRAINEDBY](https://www.trainedby.fit) and [STREEQ](https://streeq.app).

These plugins do not run local code. They point Grok at the official HTTPS MCP endpoints. Users sign in with OAuth (Auth0). No API keys are stored in this repo.

| Plugin | Who it is for | MCP URL | Docs |
| --- | --- | --- | --- |
| `trainedby` | Coaches | `https://mcp.trainedby.fit/mcp` | https://www.trainedby.fit/connect-ai |
| `streeq` | People managing their own record | `https://mcp.streeq.app/streeq/mcp` | https://streeq.app/connect-ai |

## Install

From the official xAI marketplace once the PR is merged, search **TRAINEDBY** or **STREEQ** in `/marketplace`.

Until then, add this repo as a marketplace:

```bash
grok plugin marketplace add theaverageapp/grok-plugins
grok plugin install trainedby --trust
grok plugin install streeq --trust
```

Or add the MCP URLs as custom connectors at [grok.com/connectors](https://grok.com/connectors).

## Network and auth

- TRAINEDBY: `https://mcp.trainedby.fit/mcp` — Auth0 `https://trainedby-mcp.us.auth0.com`
- STREEQ: `https://mcp.streeq.app/streeq/mcp` — Auth0 `https://trainedby-mcp.us.auth0.com`

OAuth scopes are advertised on each product's protected-resource metadata. The plugins request only those hosted servers.

## License

MIT. Product trademarks remain Average People Ltd.

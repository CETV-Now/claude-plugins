# CETV Now — Claude plugin marketplace

Claude plugins published by CETV Now. This repository is a [plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces): `.claude-plugin/marketplace.json` lists the plugins under `plugins/`.

| Plugin | Install id | Description |
|---|---|---|
| [CETV Campaigns](plugins/cetv/README.md) | `cetv@cetv-now` | Create and track CETV screen-advertising campaigns from Claude. |

```
claude plugin marketplace add CETV-Now/claude-plugins
claude plugin install cetv@cetv-now
```

## Development

- The plugin is a thin layer over the **mammoth-campaigns-service** MCP endpoint (`/mcp`); tools, auth (Clerk OAuth), and billing live in that service.
- Test local changes without publishing: `claude --plugin-dir ./plugins/cetv`
- Validate before pushing: `claude plugin validate --strict ./plugins/cetv && claude plugin validate .`
- Bump `version` in `plugins/cetv/.claude-plugin/plugin.json` on every release — users on a pinned version don't receive changes otherwise.
- Never rename the plugin (`cetv`) or the marketplace (`cetv-now`): installs are recorded under those names.

# @core/admin

[![genpm](https://api.genpm.net/v1/badge/@core/admin.svg)](https://genpm.net/p/@core/admin) ![license](https://img.shields.io/badge/license-MIT-blue)

> Admin panel generated from AdminResource: lists, forms, actions, dashboard, RBAC, CSRF protection and audit log

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/admin`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/admin
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/admin`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/admin with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Admin panel generated from `AdminResource` descriptions (from @core/contracts): navigation, dashboard widgets,
searchable/sortable lists, create/edit forms, record actions with confirmation, and delete. No per-resource screens:
any module that exports an `AdminResource` appears in the panel. Server side: session from @core/auth, permissions
from @core/rbac (`admin:access` + `<resource>:<action>`), CSRF protection on writes and an audit log of every change.
Table: `admin_audit`.

## At a glance

- **GenPM dependencies** (installed with it): [@core/db](https://genpm.net/p/@core/db), [@core/auth](https://genpm.net/p/@core/auth), [@core/rbac](https://genpm.net/p/@core/rbac), [@core/ui](https://genpm.net/p/@core/ui), [@core/contracts](https://genpm.net/p/@core/contracts)
- **npm dependencies** (proposed, never installed without asking): `react`, `zod`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/admin`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).

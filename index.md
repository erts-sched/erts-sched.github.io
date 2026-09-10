---
title: Guilherme Silva
---

# Guilherme Silva

Research interests: computer architecture, distributed processing, and
algorithm optimization. Erlang/BEAM.

GitHub: [erts-sched](https://github.com/erts-sched)

## Security research

- **2026-09** — ElixirLS: bind the MCP server to loopback — the same class in a second BEAM tool, as a hardening PR with a red/green test: [elixir-lsp/elixir-ls#1275](https://github.com/elixir-lsp/elixir-ls/pull/1275), [measurements](https://github.com/erts-sched/elixir-ls-mcp-bind-measurements).
- **2026-09** — [Documenting how to bind a distributed Erlang node to loopback](security/otp-loopback-node-docs/) — the general lesson of the extension bug, taken upstream to Erlang/OTP as a measured documentation change: [erlang/otp#11617](https://github.com/erlang/otp/pull/11617), with a [reproducible measurement repository](https://github.com/erts-sched/otp-loopback-node-measurements).
- **2026-09** — [Finding and fixing an unauthenticated RCE in the VS Code Erlang extension](security/vscode-erlang-loopback-rce/) — LSP, debugger and Erlang distribution sockets bound to all interfaces, with unauthenticated `erl_eval`; [GHSA-573p-mcvv-hchg](https://github.com/pgourlain/vscode_erlang/security/advisories/GHSA-573p-mcvv-hchg) (High), fixed in 1.1.5, ~213k installs.

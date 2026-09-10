---
title: Guilherme Silva
---

# Guilherme Silva

<p class="thesis">Trust boundaries of the BEAM runtime, measured: what a default exposes, what a control actually does, and what was not measured. Erlang/OTP and the tools built on it.</p>

## Security research

<div class="entry">
<span class="eyebrow">2026-09</span>
<div class="t"><a href="security/elixir-ls-mcp-loopback/">ElixirLS: binding the MCP server to loopback</a></div>
<div class="m">The same class in a second BEAM tool, at a lower severity, as a hardening PR with a red/green test. <a href="https://github.com/elixir-lsp/elixir-ls/pull/1275">elixir-lsp/elixir-ls#1275</a> · <a href="https://github.com/erts-sched/elixir-ls-mcp-bind-measurements">measurements</a> · <span class="chip open">open</span></div>
</div>

<div class="entry">
<span class="eyebrow">2026-09</span>
<div class="t"><a href="security/otp-loopback-node-docs/">Erlang/OTP: documenting how to bind a distributed node to loopback</a></div>
<div class="m">The general lesson of the extension bug, taken upstream as a measured documentation change. <a href="https://github.com/erlang/otp/pull/11617">erlang/otp#11617</a> · <a href="https://github.com/erts-sched/otp-loopback-node-measurements">measurements</a> · <span class="chip open">open</span></div>
</div>

<div class="entry">
<span class="eyebrow">2026-09</span>
<div class="t"><a href="security/vscode-erlang-loopback-rce/">VS Code Erlang extension: finding and fixing an unauthenticated RCE</a></div>
<div class="m">LSP, debugger and Erlang distribution sockets bound to all interfaces, with unauthenticated <code>erl_eval</code>. <a href="https://github.com/pgourlain/vscode_erlang/security/advisories/GHSA-573p-mcvv-hchg">GHSA-573p-mcvv-hchg</a> (High) · 1.1.5 · <span class="chip fixed">fixed</span></div>
</div>

## Measurements

Re-runnable, in Docker, on OTP 27, 28 and 29. Each repository states what it
measured, how, and what it did not.

<div class="entry">
<span class="eyebrow">bind</span>
<div class="t"><a href="https://github.com/erts-sched/otp-loopback-node-measurements">otp-loopback-node-measurements</a></div>
<div class="m">Where a distributed node listens. The cookie, the bind address and the node name are three different controls; 24 cases, IPv4 and IPv6.</div>
</div>

<div class="entry">
<span class="eyebrow">tls</span>
<div class="t"><a href="https://github.com/erts-sched/otp-dist-tls-measurements">otp-dist-tls-measurements</a></div>
<div class="m">What <code>-proto_dist inet_tls</code> protects. The client certificate authenticates before the cookie; <code>verify_none</code> falls back to cookie-only; TLS does not move the listener off <code>0.0.0.0</code>.</div>
</div>

<div class="entry">
<span class="eyebrow">mcp</span>
<div class="t"><a href="https://github.com/erts-sched/elixir-ls-mcp-bind-measurements">elixir-ls-mcp-bind-measurements</a></div>
<div class="m">The ElixirLS MCP listener before and after the change, and why the bundled client kept working either way.</div>
</div>

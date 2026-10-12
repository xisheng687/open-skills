---
name: agent-tool-discovery
description: Audit and repair how installed local AI agents discover shared Skills, MCP servers, and CLIs when tools work in one client but are missing in another. 检查并修复多个本地 Agent 之间的工具发现与共享问题。
license: MIT
metadata:
  version: "1.0.0"
---

# Agent Tool Discovery

Diagnose “installed here, missing there” and repair compatible local tool entry points without replacing the user's existing setup. Respond in the user's language.

## Scope and authorization

Use the user's current request to choose **audit only** or **audit and repair**. An audit request does not authorize changes. A repair request permits necessary reversible changes within the requested scope; do not repeatedly ask about routine details. Reading this skill, selecting it automatically, or finding a tool does not grant repair permission.

Preserve existing configuration, permissions, disabled states, and project scope. Do not install managers, runtimes, or dependencies; upgrade software; delete original files; broaden access; or promote project-private resources into global ones. Ask only for required login, unresolved conflicts, or actions outside the authorized scope. Continue independent work while those items remain pending.

## 1. Discover installed agents and effective entry points

Confirm OS, current user, installation versions, and the environment you can actually access. Distinguish desktop, CLI, IDE extension, cloud, container, and VM installations. A leftover directory is not proof of installation; a host path is not proof the current environment can access it.

Read [agent-catalog.md](references/agent-catalog.md) for seed candidates and official starting links. Check beyond this catalog using relevant app, executable, package-manager, and extension evidence. Deduplicate aliases only after confirming identity. A model/API provider such as MiMo, GLM, Qwen, or DeepSeek is not itself proof of a separately installed agent client.

Limit searches to relevant locations. Check configuration-directory overrides, scopes, precedence, and the installed version's help or official documentation. Do not guess paths or capabilities from product names. Do not create configuration for uninstalled clients. Record uncertain adapters as unconfirmed.

Inventory user Skills, installed plugin/system resources, MCP definitions, and relevant CLIs separately. Marketplace source caches and backup folders are not installed resources. Keep secrets out of outputs.

## 2. Repair Skill discovery where authorized

- Prefer an existing suitable canonical store; otherwise use `~/.agents/skills/` for portable user Skills. `AGENTS.md` is an instruction file, not a Skill directory.
- Preserve the whole Skill package: instructions, scripts, references, and assets. Check client-specific syntax, dependencies, and absolute paths; the shared format does not guarantee identical execution semantics.
- Prefer native discovery of the canonical store. Only add per-Skill links when needed and supported. Never replace an entire client Skills root.
- Where links are unsupported, use tracked copies with source and package hashes. On later runs, detect local edits before synchronization.
- Compare complete packages, including executable permissions and resources. Same-name packages with different content are conflicts, not candidates for newest-file-wins overwrite. Preserve both and report differences.
- Do not relocate built-in, administrator, plugin-managed, backup, or project-private Skills. Leave resources with unclear ownership or compatibility untouched.
- Before linking, resolve real paths and parent links; check self-links, cycles, overlaps, broken targets, and access. Leave correct entries unchanged. Do not relocate an inaccessible mount merely to complete the repair.

## 3. Repair MCP and CLI entry points where authorized

**MCP:** Incrementally adapt suitable existing shared user-level definitions to each applicable client's schema. Do not distribute every service to every client. Preserve unrelated fields, scopes, disabled states, and permissions. Never symlink entire JSON/TOML/YAML client configurations or copy another client's OAuth tokens, session stores, or keychain entries. Same-name definitions with different endpoints, arguments, or environment references require conflict resolution. Registration, enablement, login, tool discovery, and successful calls are separate states.

**CLI:** Usually reuse one installation. Record command name, absolute executable path, interpreter/runtime, working directory, and required environment variable names or secret references. Check each agent's execution environment, especially desktop versus terminal PATH. Check the known absolute path before declaring a missing command. Report missing dependencies; do not install them or change global PATH as an incidental repair.

**API:** Record purpose, documentation, calling entry point, and credential references. Do not link API files or wrap every API/CLI as MCP just for uniformity.

## 4. Add persistent lookup entry points

Create a concise local tool index in a suitable user-owned location outside public or tracked repositories. Record names/aliases, purpose, source/version, location, invocation, scope, runtime needs, client states, verification date, and limitations. Store credential references only.

In each client's confirmed effective user-rule entry, add or update a clearly marked block that points to the index's absolute path and says:

> Before declaring a tool missing, inspect current session tools, consult the shared tool index, then check entry points, configuration, executable paths, runtime environment, and connection/login state. Distinguish not installed, not integrated, disabled, not authenticated, inaccessible environment, loading failure, and call failure.

Preserve existing client and project rules. Do not assume every client reads `AGENTS.md` or understands the same import syntax. Prefer native discovery; an index is a supplement. Update the same block on repeated runs rather than appending duplicates. Leave a simple documented maintenance/diagnostic method for newly added agents and tools.

## 5. Validate and report

Before changes, back up affected files/links locally outside public repositories, preserve permissions, and record original state and recovery instructions. Use incremental, atomic writes and detect concurrent edits before replacing files. Log only redacted differences. Roll back only this run's changes on failure; do not overwrite intervening edits or remove originals.

Validate separately for each reachable client:

1. Files, link resolution, and configuration structure are correct.
2. The client actually lists or loads the target resource.
3. A minimal, non-billable call with no business/external write succeeds.

Inspect side effects before any call; a tool named “query” may still charge, install, download, send, or write. If a suitable safe call is unavailable, leave that layer unverified. File presence, install logs, `--help`, or an MCP handshake alone do not prove business-call success. Do not invoke mutation-oriented Skills just to test visibility.

Report inaccessible or unlaunchable clients as unverified with remaining steps. Explain when login or a refreshed/restarted session is needed; do not close applications or alter login state yourself. Do not export machine inventories, credentials, backups, reports, private endpoints, or local user paths to a public repository or a remote service without explicit authorization.

Deliver a compact agent/entry-point inventory, issues and repairs, preserved items/conflicts, index location, per-client discovery/call results, login needs, maintenance steps, and rollback method. Repeated runs must not duplicate links, rule blocks, or installations.

## 6. Optional recurring checks

After completing the requested work, ask whether the user wants recurring checks. Do not create a task without an explicit choice. If accepted, confirm frequency and native scheduling support, and verify the task can reach the intended local environment. Reuse a matching existing task instead of duplicating it.

Checks are read-only by default. Stay quiet when healthy and unchanged; notify only on meaningful problems, failures, or required action. Automated repair needs separate explicit authorization and is limited to the same reversible scope. It must not log in, install, upgrade, enable disabled resources, expand sharing, overwrite conflicts, or publish local diagnostics.

## Copy-and-paste usage

When the user wants a Chinese prompt to share without installing a Skill, use [client-prompt.zh-CN.md](references/client-prompt.zh-CN.md). It is an equivalent client-facing workflow, not evidence that any machine was inspected.

# Open Skills

[简体中文](README.zh-CN.md)

Reusable, public Agent Skills for practical workflows. Each skill lives in its own folder under `skills/`, so the collection can grow without installing everything at once.

## Available skills

| Skill | What it does |
| --- | --- |
| [Agent Tool Discovery](skills/agent-tool-discovery/SKILL.md) | Audit and repair how local AI agents discover shared Skills, MCP servers, and CLIs; preserve existing configuration and verify actual availability. |

## Why Agent Tool Discovery?

**Installed once. Invisible elsewhere.** A skill added to one agent may never appear in another. MCP clients use different configuration formats and authentication sessions. A CLI can work in a terminal while a desktop agent cannot find it. More agents often mean duplicate skills, conflicting versions, and repeated setup.

This skill turns “I already installed it—why can't you find it?” into a structured diagnosis and repair:

- Detect installed agents, versions, and execution environments, with a seed catalog of international and Chinese products.
- Reuse a central user-skill source; prefer native discovery, then per-skill links or tracked copies where supported.
- Adapt MCP definitions per client while preserving scopes, disabled states, permissions, and separate OAuth logins.
- Check CLI paths and runtime requirements instead of reinstalling them blindly.
- Add a local tool index and persistent lookup rules, then distinguish files present, client discovery, and successful calls.
- Offer scheduled checks only after the user opts in; automated repairs need separate authorization.

It does **not** require a new tool manager, convert every API to MCP, or promise universal compatibility.

## Use it

### As an installed Skill

Download or clone this repository, then import **only** `skills/agent-tool-discovery/` using your agent's supported local-skill installation method. Keep the whole folder, including its `references/` and `agents/` subfolders.

For local clients that natively support it, the shared user location is `~/.agents/skills/agent-tool-discovery/`. Other clients may require their own entry; for example, Claude Code uses `~/.claude/skills/agent-tool-discovery/`. Confirm the current product/version and compare any existing same-name skill before installation. Do not blindly replace an existing directory.

Example requests:

> Use the agent-tool-discovery skill to audit this computer's agents and shared tools. Report findings only; do not change anything.

> Use the agent-tool-discovery skill to inspect and repair tool discovery across my installed local agents. Preserve existing configuration. Ask me when login or an unresolved conflict requires my input.

In Codex, you can explicitly invoke `$agent-tool-discovery`. Other clients use their own skill invocation mechanisms.

### Without installing a Skill

Copy the [complete Chinese client prompt](skills/agent-tool-discovery/references/client-prompt.zh-CN.md) into an agent that can access your local computer. For English, use the example requests above together with the [skill instructions](skills/agent-tool-discovery/SKILL.md).

### Optional scheduled checks

After repair, the agent asks whether you want recurring checks. If you opt in, it confirms frequency, native scheduler support, and access to the intended local environment. Checks are read-only by default and quiet when nothing changes. Repair permission is a separate choice.

## Compatibility and verification

This is an instruction-based skill, not a background service or an installer script. It works through tools already available to the executing agent. An agent without local access cannot inspect your computer. Cloud sessions and virtual machines may need separate setup.

The catalog is a starting point, **not** a certified support matrix. Paths, product names, and loading rules must be checked against the installed version. Files written successfully do not prove another client loaded them. Unavailable logins or runtime tests must be reported as unverified.

## Privacy

The repository contains generic instructions and public documentation links, not machine inventories, credentials, personal paths, or account exports. The skill instructs agents to keep inventories, backups, and diagnostic reports local and outside public repositories. It includes no upload or telemetry script. Existing agent products and integrations have their own data-handling policies.

## Contribute another skill

Add `skills/<lowercase-hyphen-name>/SKILL.md` with `name` and `description` frontmatter. Include only references or scripts the workflow needs. Explain its value and usage in both README files. Use synthetic examples; never commit credentials, private endpoints, customer data, local reports, or machine-specific configuration.

## License

[MIT](LICENSE).


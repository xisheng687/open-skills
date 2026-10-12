# Open Skills

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

A public collection of practical Agent Skills, with Simplified Chinese as the primary language and guides in Traditional Chinese, English, French, German, and Spanish. Pick the skills you need; installing the entire collection is unnecessary.

## Skill catalog

| Category | Skill | Value | Download |
| --- | --- | --- | --- |
| Agent tooling | [Agent Tool Discovery](skills/agent-tool-discovery/README.en.md) | Find and repair tools that work in one local agent but are missing in another. Covers Skills, MCP, and CLI discovery while preserving configuration. | [ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) |

**Currently published: 1 skill.** This repository contains that skill's full instructions, references, Chinese and English prompts, and multilingual usage guides. It does not include the maintainer's private or previously installed skills.

Categories are labels, not nested installation directories. See [contribution and classification conventions](CONTRIBUTING.md) for adding more skills.

## Download and use

1. Download an individual Skill ZIP from [Releases](https://github.com/xisheng687/open-skills/releases), or download/clone the repository and extract `skills/<skill-name>/`.
2. Keep the entire Skill folder, including references, resources, and its license. A repository ZIP is not a single-Skill import package.
3. Follow that skill's English or Chinese README. Import through your client's supported mechanism, or use its copy-and-paste prompts where provided.

For the first skill: [English guide](skills/agent-tool-discovery/README.en.md) · [中文指南](skills/agent-tool-discovery/README.md) · [English prompt](skills/agent-tool-discovery/references/client-prompt.en.md) · [中文提示词](skills/agent-tool-discovery/references/client-prompt.zh-CN.md).

If you need help installing, attach the individual Skill ZIP or give your agent its extracted folder path and ask:

> Install only this Skill into this client's confirmed user-skill directory. Compare any existing same-name package first and preserve conflicts. Keep the full package and verify discovery in a new session. Do not execute its workflow yet.

Skill invocation syntax and installation paths vary by product and version. For local clients supporting a shared directory, use `~/.agents/skills/<skill-name>/`; Claude Code uses its own `~/.claude/skills/<skill-name>/` entry. Confirm actual support before writing anything. Cloud clients may not have access to local files.

## What is included?

```text
skills/
  agent-tool-discovery/
    SKILL.md
    README.md
    README.en.md
    README.zh-Hant.md
    README.fr.md
    README.de.md
    README.es.md
    LICENSE
    agents/openai.yaml
    references/
```

Every new skill gets a stable `skills/<name>/` folder, category/tags in its metadata, Chinese-first and English guides, optional translations, and a catalog row. Keep scripts and assets inside that skill only when needed. [CONTRIBUTING.md](CONTRIBUTING.md) explains the full process.

## Privacy and verification

Only generic instructions and public-source references belong here. Do not commit credentials, machine inventories, personal paths, private endpoints, backups, or customer data. `.gitignore` helps prevent accidental additions but is not a privacy guarantee.

These are instruction-based skills unless their documentation states otherwise. Downloading or installing does not authorize executing a workflow. Read each skill's scope and give an explicit request. Static validation and packaging do not prove every client can run a skill; runtime limitations must be reported honestly.

## License

[MIT](LICENSE). Each standalone package includes a license copy.

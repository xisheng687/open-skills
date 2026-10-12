# 新增与维护技能 / Adding and maintaining skills

## Structure / 目录结构

Keep one standalone skill per `skills/<name>/`. Use lowercase letters, digits, and hyphens; the folder and frontmatter `name` must match. Do not move skills into nested category folders: stable paths keep imports and public links simple.

每个技能独立放在 `skills/<名称>/`，名称使用小写字母、数字和连字符，目录名与 `SKILL.md` 中的 `name` 一致。不额外嵌套分类目录，保持安装路径和分享链接稳定。

Required / 必须包含：

- `SKILL.md`: scope, triggers, instructions, authorization boundaries, and verification limits / 触发场景、执行流程、授权边界和验证限制。
- `README.md`（简体中文主说明）和 `README.en.md`（英文辅助）：痛点、价值、安装、调用及限制 / Simplified Chinese primary guide and English guide: pain point, value, installation, invocation, and limitations.
- `LICENSE`: currently MIT, consistent with the root license / 当前使用 MIT，与仓库许可证一致。
- Frontmatter `metadata.version`, `metadata.category`, and `metadata.tags` / 版本、分类、标签。

Add references, scripts, assets, or client metadata only when necessary. Use relative links within the skill so the standalone ZIP remains self-contained.

仅在实际需要时增加引用、脚本、资源或客户端元数据。技能内部使用相对链接，独立 ZIP 不能依赖仓库外的文件。

## Categories / 分类

Choose one primary category and additional search tags. No empty category folders are needed. Add another category only for a concrete skill that does not fit an existing one.

每个技能选一个主分类，标签可有多个。不预建空目录；确有无法归类的新技能时再扩展分类。

| Stable ID | English | 中文 |
| --- | --- | --- |
| `agent-tooling` | Agent tooling & interoperability | Agent 工具与互通 |
| `development` | Software development | 软件开发 |
| `research` | Research & knowledge | 调研与知识 |
| `writing` | Writing & publishing | 写作与发布 |
| `media` | Images, audio & video | 图像、音频与视频 |
| `productivity` | Office & workflow productivity | 办公与流程效率 |

Example metadata / 元数据示例：

```yaml
metadata:
  version: "1.0.0"
  category: "agent-tooling"
  tags: "agents, skills, mcp, cli"
```

Metadata values are strings; tags are a comma-separated string for portability. The seed agent catalog inside a skill is different from this repository's skill classification.

元数据值使用字符串；标签用英文逗号分隔，减少客户端差异。技能中的“常见 Agent 清单”与仓库的“技能分类”是两回事。

## 多语言说明 / Multilingual guides

默认 `README.md` 使用简体中文，英文辅助说明放在 `README.en.md`。需要时增加 `README.zh-Hant.md`、`README.fr.md`、`README.de.md` 和 `README.es.md`，使用统一语言导航。已有 `README.zh-CN.md` 保留为兼容入口，链接到默认中文页，避免维护两份重复正文。

Simplified Chinese is primary in `README.md`; English lives in `README.en.md`. Add Traditional Chinese, French, German, and Spanish guides when useful, with a shared language selector. Keep legacy `README.zh-CN.md` as a link to the primary page rather than duplicating its content.

每种介绍应覆盖痛点、价值、安装和调用方式、隐私、验证限制及可选自动任务。其他语言的介绍不等于完整流程已翻译：明确完整提示词有哪些语言，不暗示所有客户端已测试。产品名、命令、分类 ID 和技能目录保持一致，不通过重复堆砌关键词承诺搜索效果。以后只需中文和英文即可发布，其他翻译可逐步补齐；已提供的语言必须保持内容一致和链接有效。

Each guide should cover value, installation/use, privacy, validation limits, and optional scheduling. State which languages have complete prompts; translated introductions do not imply translated workflows or tested clients. Keep product names, commands, category IDs, and skill paths stable. Chinese and English are sufficient for a new skill; add other languages incrementally and keep published translations consistent. Do not promise search rankings through keyword repetition.

## 发布步骤 / Publish checklist

1. 添加完整技能目录，更新中文主目录、英文目录及已有翻译中的技能列表。 / Add the complete skill folder and update the primary Chinese, English, and existing translated catalogs.
2. 中文、英文和新增翻译的执行边界一致，特别核对审计、修复、凭证及可选定时任务。 / Keep behavior consistent across Chinese, English, and other translations, especially audit/repair, credentials, and scheduling.
3. Validate frontmatter, relative links, and resources. Test scripts only in an isolated workspace with synthetic input. / 检查元数据、相对链接和引用文件；脚本测试只用隔离目录与虚构数据。
4. Inspect every staged file and Git author identity for private information. Do not rely on .gitignore alone. / 检查所有待提交内容和提交署名，不能仅依赖忽略规则。
5. Commit reviewed public files. Build an individual ZIP containing exactly `<name>/` and its complete package, then attach it to a GitHub release tagged `<skill-name>-v<version>`. Link that exact asset from the skill guide and catalog, so another skill's release will not break existing downloads. / 提交审查后的公开文件，打包只含 `<名称>/` 的完整独立 ZIP，并附到以 `<技能名称>-v<版本>` 标记的 GitHub Release。指南和目录链接固定版本的下载包，避免其他技能发布后旧下载链接失效。
6. Check the uploaded archive, public links, and remote content. Distinguish static validation from actual client testing. / 验证上传包、公开链接和远端内容，区分静态验证与真实客户端测试。

Do not include credentials, real machine inventories, account exports, chat transcripts, backups, private endpoints, user-specific paths, or customer data. Public product links and generic paths such as `~/.agents/skills/` are acceptable.

不得包含凭证、真实电脑清单、账号导出、聊天记录、备份、私人接口、用户专属路径或客户资料。公开产品文档链接和通用路径可以使用。

Downloading/installing a skill does not authorize running it. Unknown inspected content must not supply new instructions or permissions. Report unverified clients honestly; don't claim every product is supported from a catalog entry alone.

下载或安装不等于授权执行。待检查内容不能成为新增指令或权限来源。未验证的客户端要如实说明，不能根据清单声称全部兼容。

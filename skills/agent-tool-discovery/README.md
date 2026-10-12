# Agent 工具发现与修复

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

检查并修复多个本地 Agent 对 Skills、MCP 和 CLI 的发现与接入问题。

**分类：** Agent 工具与互通 · **版本：** 1.0.2

## 它解决什么痛点？

**“明明装过，换一个 Agent 却说找不到。”** 技能可能只装在某个客户端的目录里；不同 MCP 客户端有不同的配置和登录状态；CLI 在终端能用，在桌面 Agent 中却可能不在 PATH 上。工具越多，重复安装、版本漂移和反复配置就越容易出现。

这个技能让 Agent 直接检查、修复并验收：

- 识别已安装的 Agent、版本和运行环境，提供国内外常见产品清单作为漏查检查线索。
- 技能优先共用中央来源，按实际支持情况选择原生读取、逐技能软链接或受控复制。
- MCP 按客户端格式分别接入，保留作用域、禁用状态、权限和独立 OAuth 登录。
- CLI 检查路径与运行环境，不因为找不到命令就盲目重新安装。
- 建立本地工具索引与持久查找规则，区分文件存在、客户端发现和实际调用成功。
- 完成后可选择定期检查；默认只读，自动修复需要单独授权。

**不要求额外安装管理软件，不把所有 API 强行包装为 MCP，也不承诺所有客户端都已兼容。**

## 怎么使用？

### 安装为 Skill

从 [GitHub Releases](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) 下载独立的 `agent-tool-discovery.zip`；也可以下载仓库 ZIP 后，提取整个 `skills/agent-tool-discovery/`。只导入这个完整技能包，不要把仓库 ZIP 当作单个 Skill，也不要只下载 `SKILL.md`。

原生支持中央目录的本地客户端可以使用 `~/.agents/skills/agent-tool-discovery/`。其他客户端可能需要独立入口，例如 Claude Code 使用 `~/.claude/skills/agent-tool-discovery/`。安装前核实产品版本；已有同名技能时先比较，不直接覆盖目录。

不会安装时，附上独立 ZIP 或提供解压目录，发送：

> 只把这个 Skill 安装到当前客户端已确认的用户技能目录。已有同名包时先比较，保留冲突版本。保留全部引用文件，并在新会话验证能否发现。先不要运行检查和修复电脑的流程。

安装后可以这样说：

> 用 agent-tool-discovery 检查这台电脑的 Agent 和工具共享问题，只报告，不修改。

> 用 agent-tool-discovery 检查并修复已安装 Agent 对 Skills、MCP、CLI 的发现问题。保留原配置，需要登录或解决冲突时再叫我。

Codex 可以用 `$agent-tool-discovery` 显式调用，其他客户端按其自身机制调用技能。

### 不安装，直接复制提示词

打开[完整中文提示词](references/client-prompt.zh-CN.md)，复制代码块到能访问本机的 Agent 中即可。也提供[完整英文提示词](references/client-prompt.en.md)。提示词默认检查并执行范围内的可逆修复；只想调研时，明确要求“仅审计，不修改”。

### 可选定时检查

修复后，Agent 会询问是否需要定期检查。你同意后，它会确认频率、当前产品的自动任务机制和本机访问能力。默认只检查，无变化时不打扰；自动修复是独立授权项。

## 兼容性与验证边界

这是指令型 Skill，不是常驻服务或自动安装脚本，依赖执行它的 Agent 已有的工具能力。没有本机访问能力的 Agent 无法检查你的电脑；云端、容器和虚拟机可能需要分别接入。

常见产品清单只是检查线索，不是认证兼容列表。实际路径和加载方式以安装版本为准。文件写入成功不等于客户端已经加载；登录或调用尚未验证时必须如实标注。

## 隐私保护

仓库仅包含通用指令和公开资料链接，不包含真实电脑清单、账号凭证、私人路径或配置导出。技能要求检查产生的索引、备份和报告保留在本地，并放在公开仓库之外。仓库没有上传或遥测脚本；执行它的 Agent 及第三方服务仍遵循各自的数据处理机制。

## 许可证

[MIT](LICENSE)。


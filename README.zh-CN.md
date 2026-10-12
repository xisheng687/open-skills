# Open Skills

[English](README.md)

可公开分享、按需使用的实用 Agent Skills 合集，提供中英文说明。选择需要的技能即可，无需一次安装整个仓库。

## 分类与技能目录

| 分类 | 技能 | 价值 | 下载 |
| --- | --- | --- | --- |
| Agent 工具与互通 | [Agent 工具发现与修复](skills/agent-tool-discovery/README.zh-CN.md) | 解决工具在一个 Agent 能用、换一个却找不到的问题，检查 Skills、MCP 和 CLI 接入，并保留原配置。 | [ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.1/agent-tool-discovery.zip) |

**目前公开发布 1 个 Skill。** 本仓库包含它的完整指令、引用、中英文提示词和使用说明，不包含维护者本机的其他技能或私人资料。

分类使用标签，不把安装目录套进多层分类文件夹。新增技能的方式见[贡献与分类规范](CONTRIBUTING.md)。

## 下载与使用

1. 从 [Releases](https://github.com/xisheng687/open-skills/releases) 下载单个 Skill ZIP；也可下载或克隆仓库，提取完整的 `skills/<技能名称>/`。
2. 保留整个技能目录，包括引用、资源和许可证。仓库 ZIP 不等于可直接导入的单技能包。
3. 按该技能目录中的中英文 README，通过客户端支持的方法安装；也可以使用它提供的完整提示词。

第一个技能：[中文使用指南](skills/agent-tool-discovery/README.zh-CN.md) · [English guide](skills/agent-tool-discovery/README.md) · [完整中文提示词](skills/agent-tool-discovery/references/client-prompt.zh-CN.md) · [完整英文提示词](skills/agent-tool-discovery/references/client-prompt.en.md)。

不会安装时，把独立 Skill ZIP 附给 Agent，或提供解压目录，发送：

> 只把这个 Skill 安装到当前客户端已确认的用户技能目录。已有同名包时先比较，保留冲突版本。保留完整技能包，并在新会话验证能否发现。先不要运行它的业务流程。

不同产品和版本的安装路径与调用方式可能不同。原生支持共享目录的本地客户端可以使用 `~/.agents/skills/<技能名称>/`；Claude Code 使用自己的 `~/.claude/skills/<技能名称>/` 入口。写入前确认实际支持情况。云端客户端不一定能读取本机文件。

## 仓库里有什么？

```text
skills/
  agent-tool-discovery/
    SKILL.md
    README.md
    README.zh-CN.md
    LICENSE
    agents/openai.yaml
    references/
```

以后每个技能使用稳定的 `skills/<名称>/` 目录，在元数据里标记分类和标签，附中英文说明，再登记一行技能目录。需要的脚本和资源只放在对应技能里，避免相互依赖。[CONTRIBUTING.md](CONTRIBUTING.md) 提供完整新增流程。

## 隐私与验证

这里只存通用指令和公开资料，不提交凭证、电脑清单、私人路径、内部服务地址、备份或客户数据。`.gitignore` 只能辅助防误提交，不能代替隐私检查。

除非技能说明另有声明，这些是指令型 Skill。下载或安装不等于授权执行流程；请先阅读范围并给出明确请求。静态检查和打包通过不代表已在所有客户端运行验证，实际限制必须如实说明。

## 许可证

[MIT](LICENSE)，独立技能包也包含许可证副本。

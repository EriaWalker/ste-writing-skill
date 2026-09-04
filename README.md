# ste-writing

> [!IMPORTANT]
> **作者：[@woosal](https://www.youtube.com/@woosal)**
>
> 本技能源自他播放量超过 38 万次的 YouTube 视频：
> [《解决 AI 废话的方法，藏在一本 1986 年的飞机手册中》](https://www.youtube.com/watch?v=uJblcC4lKYw)。

使用 ASD-STE100 简化技术英语规则改写文本。
它可以让AI的输出减少70%的文字，同时保留原文的技术含义。

## 适用内容

- 技术文档和 README
- Pull Request 描述
- 错误信息
- 发布说明
- 代码注释
- 操作步骤和安全说明

请勿用它改写代码、营销文案或需要鲜明个人风格的内容。

## 两种模式

- `strict`：完整应用所有规则，适合操作步骤、运行手册、安全说明和错误信息。
- `STE-flavored`：保留清晰简洁的写作规则，放宽受控词汇限制，适合一般技术文档。

## 安装

将本仓库克隆到 Agent 的技能目录：

```sh
git clone https://github.com/EriaWalker/ste-writing-skill.git ~/.codex/skills/ste-writing-skill
```

安装后重新启动 Agent。

## 使用

让 Agent 使用 `$ste-writing`，并指定所需模式。

```text
使用 $ste-writing 的 strict 模式改写这份运行手册。
```

```text
使用 $ste-writing 的 STE-flavored 模式改写这份 README。
```

## 文件

- `SKILL.md` 包含技能说明。
- `scripts/ste-lint.py` 检查可机械识别的写作问题。

## 运行检查脚本

```sh
python scripts/ste-lint.py README.md
```

检查脚本只能发现形式问题。
请通过人工检查确认技术含义和专业名词准确无误。

## 参考资料

如需了解该标准，请访问 [ASD-STE100 官方网站](https://asd-ste100.org/)。
该标准受版权保护，因此本仓库不会复制标准全文。

---

# English

> [!IMPORTANT]
> **Author: [@woosal](https://www.youtube.com/@woosal)**
>
> This skill comes from his 380K-view YouTube video:
> [The cure for AI slop is a 1986 aircraft manual](https://www.youtube.com/watch?v=uJblcC4lKYw).

This agent skill rewrites technical prose with rules from ASD-STE100 Simplified Technical English.
It removes common AI writing patterns while it preserves technical meaning.

## Suitable content

- Technical documentation and READMEs
- Pull request descriptions
- Error messages
- Release notes
- Code comments
- Procedures and safety text

Do not use it for code, marketing copy, or prose that needs a distinct voice.

## Modes

- `strict` applies every rule to procedures, runbooks, safety text, and error messages.
- `STE-flavored` keeps general documentation clear without the full controlled vocabulary.

## Install

Clone this repository into the skills directory for your agent.

```sh
git clone https://github.com/EriaWalker/ste-writing-skill.git ~/.codex/skills/ste-writing-skill
```

Restart the agent after installation.

## Use

Ask your agent to use `$ste-writing` and select a mode.

```text
Use $ste-writing in strict mode to rewrite this runbook.
```

```text
Use $ste-writing in STE-flavored mode to rewrite this README.
```

## Files

- `SKILL.md` contains the skill instructions.
- `scripts/ste-lint.py` checks mechanical style violations.

## Run the linter

```sh
python scripts/ste-lint.py README.md
```

The linter finds mechanical violations.
Human review must confirm the correct meaning and technical nouns.

## Reference

Read the [ASD-STE100 official site](https://asd-ste100.org/) for information about the standard.
Copyright protects the standard, so this repository does not reproduce it.

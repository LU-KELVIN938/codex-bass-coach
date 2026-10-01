# Codex Bass Coach · Codex 贝斯练习助手

[中文使用说明 / Chinese guide](docs/USAGE.md#中文使用说明) · [English guide](docs/USAGE.md#english-guide) · [Attribution / 来源与署名](ATTRIBUTION.md)

A community-maintained Codex skill for planning bass practice, keeping local practice journals, and choosing the next exercise from your history.

一个社区改编的 Codex Skill：帮助安排贝斯练习、保存本地练习日志，并根据历史记录选择下一次练习。

## What it does · 可以做什么

| 中文 | English |
| --- | --- |
| 根据程度、风格和可用时间安排练习 | Plan practice around your level, style, and available time |
| 解释二指交替、制音、节奏与音符长度 | Explain alternating fingers, muting, timing, and note length |
| 记录练习时间、曲目、速度、困难和下一步 | Record duration, repertoire, tempo, difficulties, and next steps |
| 读取已有记录，回顾进展与制定周计划 | Read existing journals to review progress and plan the week |
| 区分尝试过的速度与稳定完成的速度 | Distinguish attempted tempos from consistently completed tempos |

The skill contains instructions, not a background service or an audio-analysis engine. Codex performs the work during a conversation, using the information and tools available in that session. Media analysis and scheduled reminders require separate supported tools or setup.

这个 Skill 提供工作指令，由 Codex 在对话中执行。它本身不运行后台服务，也不提供音频测量程序。录音/视频分析取决于当前会话支持的工具；定时提醒需要另外设置。

## Install · 安装

Ask Codex to install the skill from this repository:

在 Codex 中发送：

```text
Install the skill from https://github.com/LU-KELVIN938/codex-bass-coach/tree/main/skills/bass-practice
```

```text
请安装 https://github.com/LU-KELVIN938/codex-bass-coach/tree/main/skills/bass-practice 中的 Skill。
```

Alternatively, copy only `skills/bass-practice/` into your Codex skills directory. Current official user-scope locations are `%USERPROFILE%\.agents\skills\bass-practice` on Windows and `~/.agents/skills/bass-practice` on macOS/Linux; a repository-scoped installation uses `.agents/skills/bass-practice` inside that repository. Some clients and installer versions also use `.codex/skills`; follow the location reported by your installer rather than installing duplicates. If the skill is not listed after installation, open a new chat or restart your client. See [official skill documentation](https://learn.chatgpt.com/docs/build-skills#where-to-save-skills).

也可以只把 `skills/bass-practice/` 文件夹复制到 Codex 的 Skills 目录。当前官方用户级位置是 Windows 的 `%USERPROFILE%\.agents\skills\bass-practice` 或 macOS/Linux 的 `~/.agents/skills/bass-practice`；项目级位置是在该项目中的 `.agents/skills/bass-practice`。部分客户端及安装器版本也使用 `.codex/skills`，按安装器实际报告的位置操作，避免重复安装。安装后如果没有显示，打开新聊天或重启客户端。参见[官方技能文档](https://learn.chatgpt.com/docs/build-skills#where-to-save-skills)。

## Start here · 开始使用

```text
Use $bass-practice. I am a beginner on a four-string bass, play fingerstyle,
and like rock. Plan a relaxed 20-minute session. Use Chinese for coaching.
```

```text
使用 $bass-practice。我是四弦贝斯新手，用手指弹，喜欢摇滚。
帮我安排20分钟练习，用中文指导；我的日志放在当前工作区。
```

After practice / 练完以后：

```text
使用 $bass-practice。记录今天练了20分钟，二指交替尝试80 BPM，
换弦有杂音。还没有测稳定速度，音符细分也没有记录。
```

The default journal folder is `.bass-practice/` inside the current workspace. Codex reports its absolute path when creating it. Keep using that workspace, or give the absolute journal path in another chat. This is file-based continuity, not automatic memory across every chat.

默认日志保存在当前工作区的 `.bass-practice/` 中，建立时 Codex 会告诉你完整路径。以后继续使用同一工作区，或在新聊天中提供日志的完整路径，就能接着记录。它通过读取文件延续进度，不会自动让所有聊天共享记忆。

## Repository layout · 文件结构

```text
skills/bass-practice/
├── SKILL.md                  # Canonical instructions / 核心指令
├── agents/openai.yaml        # Codex display metadata / 显示信息
└── references/
    ├── tracking.md           # Journal rules and templates / 日志规则与模板
    └── coaching.md           # Technique guidance / 练习与技术指导
docs/USAGE.md                 # Chinese and English walkthrough / 中英文教程
ATTRIBUTION.md                # Original source and changes / 来源与改动
LICENSE                      # MIT license / MIT许可证
```

## Privacy and evidence · 记录与依据

This repository publishes the skill and fictional examples, not personal journals. Its `.gitignore` excludes `.bass-practice/` and `practice-data/`. If you keep logs in a different Git repository or choose a different folder name, add that location to that repository's ignore rules before publishing.

本仓库发布的是 Skill 和虚构示例，不包含个人练习记录；`.gitignore` 排除了 `.bass-practice/` 和 `practice-data/`。如果日志放在其他 Git 仓库或使用其他名称，发布前应在那个仓库中添加相应忽略规则。

Practice facts are marked as self-reported or observed. A tempo without a note subdivision is not a comparable benchmark. Missing data stays unknown; the assistant does not invent measurements or completed practice.

练习事实会标注为自述或观察。只写 BPM、没有音符细分，不能直接比较技术水平。缺失信息保留为未知，助手不能编造测量值或已完成的练习。

## Credits · 致谢

Adapted from [clawic/skills — Bass](https://github.com/clawic/skills/tree/f84d54cb4598a24a4146176aa4b3c3da413edc1e/skills/bass), originally licensed under MIT by Ivan G. Davila. Codex adaptation and bilingual documentation by LU-KELVIN938, with AI assistance. This project is not affiliated with or endorsed by OpenAI, Clawic, or the original author.

改编自 Ivan G. Davila 以 MIT 许可证发布的 [clawic/skills — Bass](https://github.com/clawic/skills/tree/f84d54cb4598a24a4146176aa4b3c3da413edc1e/skills/bass)。Codex 适配与双语文档由 LU-KELVIN938 在 AI 协助下制作。本项目不代表 OpenAI、Clawic 或原作者的官方认可。

See [ATTRIBUTION.md](ATTRIBUTION.md) for the pinned source and changes. See [LICENSE](LICENSE) for the full terms.

具体来源与改动见 [ATTRIBUTION.md](ATTRIBUTION.md)，完整条款见 [LICENSE](LICENSE)。

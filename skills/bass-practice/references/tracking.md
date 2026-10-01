# Practice tracking · 练习记录

## Location and continuity · 位置与延续

Use the journal location explicitly selected by the user. Otherwise use `.bass-practice/` in the current workspace. Resolve and display the absolute path before or when initializing. If a journal already exists there, read and reuse it. Do not initialize a competing journal silently. Do not store records in the skill installation directory.

优先使用用户指定的位置，否则使用当前工作区的 `.bass-practice/`。建立时解析并展示完整路径；已有日志就读取并继续使用，避免重复建立档案。个人记录不存进 Skill 安装目录。

Create only files needed by the current request. Use paths native to the host, UTF-8 text, and the user's local date. Do not overwrite existing files with templates. Do not save account credentials or unrelated personal information. Publishing the skill never implies publishing its journals.

只建立当前任务需要的文件。使用当前系统的路径、UTF-8 文本和用户所在时区的日期，不用模板覆盖已有内容。不保存账号凭据和无关个人信息；发布 Skill 不代表发布练习日志。

```text
.bass-practice/
├── profile.md          # Relevant learning context / 学习背景
├── goals.md            # Agreed goals / 已确定目标
├── repertoire.md       # Song status / 曲目进度
├── technique.md        # Benchmarks and difficulties / 技术指标与困难
└── sessions/
    └── YYYY-MM.md      # Monthly sessions / 按月练习日志
```

Use the user's language for actual records; bilingual headings below are templates, not a requirement to duplicate every entry. Profile details should come from the user and be saved only as part of requested record keeping.

实际记录用用户的语言即可；下列双语标题用于解释模板，不要求每条内容重复翻译。学习背景必须来自用户，在用户要求建立或维护档案时保存。

## Session template · 单次记录模板

```markdown
# Practice sessions · 练习日志 — YYYY-MM

## YYYY-MM-DD — Session 1 / 第1次
- Duration / 时长: unknown / 未提供
- Exercise or song / 练习或曲目: unknown / 未提供
- Technique / 技术: unknown / 未提供
- Attempted tempo / 尝试速度: unknown / 未提供
- Note subdivision / 音符细分: unknown / 未提供
- Stable benchmark / 稳定指标: not established / 未确认
- Evidence / 依据: user report / 用户自述
- Difficulty / 困难: unknown / 未提供
- Next step / 下一步: suggested, not completed / 建议，尚未完成
```

The date and "Session 1" are placeholders. Use distinct session numbers for separate practices on one date. If the user is adding details to the same session, amend it instead of counting twice. For an ambiguous correction, clarify which entry rather than overwriting several.

日期和“第1次”是占位符。同一天的不同练习可以编号；补充同一次练习时更新该条，不重复累计。修改目标条目不清楚时先澄清，避免改错。

Keep absent duration unknown. Include unknown-duration sessions in the session count, but exclude them from recorded-minute totals and disclose that omission. "No entries" does not mean "did not practice."

没提供时长就保留未知。统计练习次数时包含它，统计已记录分钟数时排除并说明缺失。“没有日志”不等于“没有练琴”。

## Benchmarks · 技术指标

For comparable speed records, capture: exercise, BPM, note subdivision, duration/repetitions, quality criterion, source, and date. An optional agreed criterion is three consecutive relaxed, even runs at the chosen subdivision with controlled muting. This is a local practice criterion, not a certification standard.

可比较的速度记录需要：练习内容、BPM、音符细分、时长/次数、完成标准、依据和日期。可以共同约定“在指定细分下，连续三遍放松、均匀、制音可控”作为一次练习标准；这不是专业认证标准。

```markdown
# Technique · 技术

## Alternating fingers · 二指交替
- Current difficulty / 当前困难:
- Attempted tempo / 尝试速度:
- Stable tempo / 稳定速度: not established / 未确认
- Subdivision and exercise / 音符细分与练习:
- Completion criterion / 完成标准:
- Evidence and date / 依据与日期:
```

Do not promote an attempt to a stable benchmark without evidence. Self-reported stability remains labeled self-reported. Recording "80 BPM" with an unknown subdivision is allowed; ranking it against eighth- or sixteenth-note benchmarks is not.

没有依据就不能把尝试速度升级为稳定速度。用户说稳定完成，仍标明“用户自述”。允许保存“80 BPM、细分未知”，但不能拿它与八分或十六分音符的指标直接排名。

## Goals and repertoire · 目标与曲目

```markdown
# Goals · 目标
## Agreed short-term goals · 已确定的短期目标
## Agreed long-term goals · 已确定的长期目标
## Suggestions, not yet agreed · 尚未确认的建议
```

```markdown
# Repertoire · 曲目
## Learning · 正在学习
## Completed under agreed criteria · 达到约定标准
## Wishlist · 想学
```

For a song, record title, artist if known, start date if known, section, difficulty, and next step. Do not paste copyrighted full tabs or lyrics into the journal. A song moves to completed only when the learner confirms completion or available evidence supports the agreed criterion.

曲目记录名称、已知的演奏者/作者、已知开始日期、段落、困难和下一步。不要把整首受版权保护的谱或歌词复制到日志。用户确认完成，或已有依据支持约定标准后，才能标成完成。

## Verification · 保存后核对

Read the edited file to verify the requested entry, date, evidence labels, and preserved history. Report the absolute saved path. A failed write must be reported as unsaved. A review reads relevant monthly files plus goals, repertoire, or technique as needed; never infer progress solely from file names.

保存后读取文件，核对条目、日期、依据标签与历史内容，告诉用户实际保存路径。写入失败要明确“未保存”。回顾时读取有关月份和必要的目标、曲目、技术档案，不能只看文件名就推断进展。

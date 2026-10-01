# Usage · 使用教程

## 中文使用说明

### 第一次使用

安装后在聊天中输入 `$bass-practice`，或直接说“使用贝斯练习 Skill”。正常的贝斯练习请求也可触发自动选择。首次咨询动作不需要先填写整套问卷；安排长期练习时再补充程度、风格、演奏方法和目标。

```text
使用 $bass-practice。我是新手，四弦贝斯，二指弹奏，喜欢摇滚。
今天只有20分钟，帮我安排放松、制音和节奏练习。
```

这是练习计划请求，助手应给出计划，不会仅因你提到贝斯就建立日志。

### 建立日志

```text
使用 $bass-practice。建立我的练习档案。
日志放在当前工作区的 .bass-practice 文件夹。
我的目标是下个月能够放松、稳定地跟伴奏弹完一首简单歌曲。
```

助手会建立当前需要的档案，告诉你完整路径。推荐在一个专门的 Bass 练习工作区中长期使用。默认路径随当前工作区而变；新聊天想继续读同一套档案，需要使用原工作区或提供原来的完整路径。

如果你指定其他位置，确认它在当前会话可写范围内。无法写入时，助手应提供“未保存”的草稿，不能声称记录成功。

### 每次练完怎么说

```text
记录今天20分钟：二指交替，80 BPM八分音符，连续弹了3遍。
前两遍比较均匀，第三遍换弦有杂音。都是我自己的感受，没有录音。
```

助手保存到 `sessions/YYYY-MM.md`，注明“用户自述”。这里不满足三遍稳定完成的标准，因此不能自动写成“已稳定掌握80 BPM”。保存后，它会给出文件路径和记录摘要。

信息不完整也可以记录：

```text
记录今天尝试90 BPM，弹得有点紧张，时长和音符细分没记。
```

缺失字段写成未知。周总结会统计这次练习次数，但不能把未知时长算成0分钟或把90 BPM当成已稳定成绩。

### 修改、回顾和继续练习

```text
把今天第1次练习的时长改为25分钟，其他内容不变。
```

```text
读取我的练习档案，总结本周记录了几次、多少已知分钟。
指出缺失的信息，并按最常出现的困难安排下周计划。
```

如果同一条记录只是补充内容，助手更新原条目；只有另一次练习才新建条目。没有记录的日期不代表没有练琴。不同曲目、不同音符细分的速度不会直接混在一起比较。

### 它能看视频、每天提醒吗

Skill 本身没有摄像头控制、音频测量或后台定时程序。如果当前 Codex 会话支持你提供的媒体，助手可以用可用能力检查，并说明真正检查了什么；否则它应基于你的描述指导。要每天主动提醒，需要另行配置自动任务。

### 示例说明

本教程中所有练习数据都是虚构示例。你的真实档案只保存在你选定的本地目录。发布本仓库时，不需要上传那些个人记录。

## English guide

### First conversation

After installation, invoke `$bass-practice` or ask for bass practice coaching. Relevant requests may also select it automatically. A focused technique question should get a focused answer; longer plans can gather your level, preferred style, playing method, instrument, and goals as needed.

```text
Use $bass-practice. I am a beginner on a four-string bass, play fingerstyle,
and like rock. Plan a relaxed 20-minute session focused on muting and timing.
```

This asks for a plan, not a journal. The assistant should not create files just because bass was mentioned.

### Start a journal

```text
Use $bass-practice. Start my practice journal in .bass-practice in this workspace.
My goal is to play one easy song comfortably with a backing track next month.
```

The assistant creates only the files needed now and reports their absolute paths. A dedicated practice workspace makes continuity easy. In another chat, use that same workspace or provide the journal's absolute path. The default location changes with the workspace.

If you choose another location, it must be writable in the current session. A write failure should produce a clearly labeled unsaved draft, not a success claim.

### Log a session

```text
Record today's 20 minutes: alternating fingers, eighth notes at 80 BPM,
three runs. The first two felt even; the third had string-change noise.
These are my impressions; there is no recording.
```

The entry goes into `sessions/YYYY-MM.md`, labeled self-reported. This does not satisfy a three-clean-run criterion, so it must not become a stable 80 BPM benchmark automatically. The assistant reports the saved file and summarizes the entry.

Incomplete information can still be logged:

```text
Record that I tried 90 BPM today and felt tense. I did not note the duration
or note subdivision.
```

Missing fields stay unknown. Reviews count the session, but do not invent its minutes or a stable benchmark.

### Correct, review, and continue

```text
Correct today's Session 1 to 25 minutes. Leave everything else unchanged.
```

```text
Read my journal. Summarize this week's recorded sessions and known minutes,
disclose missing information, and plan next week around recurring difficulties.
```

Additional details amend the same session; a separate practice gets a separate entry. A missing date does not prove no practice happened. Do not compare tempos across different exercises or subdivisions as if they were the same benchmark.

### Media and reminders

The skill has no camera control, audio-measurement engine, or background scheduler. Media inspection depends on available session tools and supported input; the assistant must describe what it actually inspected. Scheduled reminders require separate configuration.

### Examples and personal data

All practice data in this guide is fictional. Actual journals stay in your selected local folder and are not needed to publish this repository.

# Talking Avatar Video Skill

[English](./README.md) | 简体中文 | [日本語](./README.ja.md)

> 👉 也看看 [Multilingual Voiceover Skill](https://github.com/beatra-ai/multilingual-voiceover-skill)

把一张人像和一段脚本做成数字人口播视频，在 Claude Code、Cursor、Codex、Windsurf、Cline 或 OpenClaw 里直接完成。

> [!IMPORTANT]
> 生成需要 [Beatra](https://beatra.ai) 账号并消耗积分，安装本身不收费。

| 问题 | 回答 |
| --- | --- |
| **能做什么** | 把一张人像和短脚本或语音，制作成适合讲解、公告、课程和产品介绍的数字人口播视频。 |
| **底层模型** | MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo、Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5 |
| **运行要求** | Python 3.10+，以及能加载 `SKILL.md` 的 Agent |
| **费用** | 安装免费。每次生成消耗 Beatra 账号积分，只有你明确要求这次生成或批准确认卡后才会付费。 |
| **支持的 Agent** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="左为虚构讲解员人像输入，右为由一句合成英文口播驱动生成的数字人视频中的一帧。由 Beatra AI 生成。"></p>

*左为虚构讲解员人像输入，右为由一句合成英文口播驱动生成的数字人视频中的一帧。由 Beatra AI 生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`talking-avatar-video`](skills/talking-avatar-video) | [SKILL.md](skills/talking-avatar-video/SKILL.md) | 0.3.0 |

本仓库由 [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/talking-avatar-video) 自动发布，问题请到那里反馈。

## 安装

使用 [`skills`](https://skills.sh) CLI：

```bash
npx skills add beatra-ai/talking-avatar-video-skill
```

使用 GitHub CLI：

```bash
gh skill install beatra-ai/talking-avatar-video-skill talking-avatar-video
```

也可以克隆本仓库，把 `skills/talking-avatar-video` 复制到 `~/.claude/skills/`（Claude Code）、`~/.cursor/skills/`（Cursor）、`~/.agents/skills/`（Codex）、`~/.codeium/windsurf/skills/`（Windsurf）、`~/.cline/skills/`（Cline）或 `~/.openclaw/skills/`（OpenClaw）。

或者把下面这段话发给你的 Agent：

```text
从 https://github.com/beatra-ai/talking-avatar-video-skill 安装 talking-avatar-video skill（目录 skills/talking-avatar-video），然后按它的 SKILL.md 连接我的 Beatra 账号。
```

## 效果示例

<p align="center"><img src="assets/preview.webp" width="800" alt="由一张虚构人像和一句合成口播生成的 6 秒数字人讲解视频（台词：&quot;Hi! In thirty seconds, I&#x27;ll show you how our new planner app saves your mornings.&quot;）。由 Beatra AI 生成。"></p>

[▶ 观看完整视频（MP4）](assets/full.mp4)

*带声音的完整数字人视频：虚构的产品讲解员说出 "Hi! In thirty seconds, I'll show you how our new planner app saves your mornings."。由 Beatra AI 生成。*

在你的 Agent 里这样说：

```text
用 ./presenter.jpg 当主播，让她面对镜头、用温和自然的语气说这句话：“Hi! In thirty seconds, I'll show you how our new planner app saves your mornings.” 画面固定，表情亲切。
```

提示词：

```text
A friendly presenter speaks directly to camera with a warm, natural delivery: steady eye line into the lens, restrained friendly expression, subtle natural head movement and occasional blinks, relaxed shoulders. Locked-off stable camera, plain studio background stays unchanged, same face, hair and green sweater throughout.
```

## 技术规格与输出限制

截至 2026-10-18。实时列表：https://docs.beatra.ai/zh/docs/models

- **上传** — 单个文件最大 100 MB；同时适用下方各模型的输入限制
- **语音合成** — 2 个模型（MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo）；FLAC、MP3、OPUS、PCM、WAV；40 种语言；采样率 8、16、22.05、24、32、44.1 kHz；单次最多 50000 字符
  - 语言（ISO 639 代码）：zh, yue, en, es, fr, ru, de, pt, ar, it, ja, ko, id, vi, tr, nl, uk, th, pl, ro, el, cs, fi, hi, bg, da, he, ms, fa, sk, sv, hr, fil, hu, no, sl, ca, nn, ta, af
- **图生视频** — 9 个模型（Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）；480p 至 4K；2–30 秒；画幅 16:9、1:1、21:9、3:4、4:3、9:16；MOV、MP4
  - 4K：Seedance 2.0，最长 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5，最高 1080p
  - 原生音频：Wan 2.7、MiniMax H3

## 为什么用 Beatra，而不是直接调用模型 API

- **一个账号用到本 skill 的全部模型** — 语音合成 2；图生视频 9（MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo、Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）（截至 2026-10-18），一次 Beatra 登录即可使用，不必分别管理各家模型的 key。
- **花不花钱由你决定** — 只有你明确要求这次生成，或批准显示实时积分估算的确认卡后才会付费。
- **先策划，再生成** — skill 先帮你规划、指导和检查，再在 Beatra 上生成。
- **文件可以核验** — `skills/` 下的每个文件都与 cdn.beatra.ai 上的发布归档逐字节一致，每次推送前用 SHA-256 校验。
- **更新由你掌控** — 不含自更新程序；用安装时的工具更新。
- **在你的 Agent 里运行** — Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw。

## 你能得到什么

- **先把旁白准备好** — 使用现成语音，或先把短脚本生成可试听的旁白，再进入视频阶段。
- **让表演服务于内容** — 克制眼神、表情、动作、镜头与背景，并如实检查人物和口型效果。

## 适用场景

- **产品讲解** — 用稳定的虚拟讲述者介绍功能、优惠或上新，不必重新拍摄真人口播。
- **培训与课程** — 制作简短的入职说明、课程开场或内部更新。
- **公告与社交口播** — 把准备好的信息变成面向观众的公告或社交短视频。

## 常见问题

### 开始制作需要什么？

需要一张清晰人像，以及一段现成语音，或一份短脚本加已选音色。

### 可以使用自己的录音吗？

可以，它的格式和时长需要符合当前支持的视频方式。

### 成片会怎样检查口型与人物一致性？

语音会驱动面部动作，交付后会重点查看口型节奏、人物特征、声音清晰度和动作稳定性，并据此确定最值得调整的一点。

## 更新与安全

自 2026 年 10 月的版本起，本 skill 不再包含自更新程序：它只运行你安装的文件，从不自行替换。
请用安装时的工具更新——`npx skills update talking-avatar-video` 或 `gh skill update talking-avatar-video`。
详见 skill 内的 `references/updates-and-security.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。

## 相关链接

- 官网 — https://www.beatra.cn
- 文档 — https://docs.beatra.cn
- 控制台 — https://console.beatra.cn
- 给 AI Agent 读的说明 — https://www.beatra.cn/llms.txt（索引）· https://www.beatra.cn/llms-full.txt（全部 skill 合成一个文件）

- 微信小程序 — 国内用户微信扫码使用

<img src="assets/beatra-mini-program-qr.jpg" alt="Beatra 微信小程序码" width="160">

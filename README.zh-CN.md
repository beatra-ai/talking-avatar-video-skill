# Talking Avatar Video Skill

[English](./README.md) | 简体中文

把一张人像和一段脚本做成数字人口播视频，在 Claude Code、Codex 或 OpenClaw 里直接完成。

> [!IMPORTANT]
> 生成需要 [Beatra](https://beatra.ai) 账号并消耗积分，安装本身不收费。

| 问题 | 回答 |
| --- | --- |
| **能做什么** | 把一张人像和短脚本或语音，制作成适合讲解、公告、课程和产品介绍的数字人口播视频。 |
| **运行要求** | Python 3.10+，以及能加载 `SKILL.md` 的 Agent |
| **费用** | 安装免费。每次生成消耗 Beatra 账号积分，只有你明确要求这次生成或批准确认卡后才会付费。 |
| **支持的 Agent** | Claude Code、Codex、OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`talking-avatar-video`](skills/talking-avatar-video) | [SKILL.md](skills/talking-avatar-video/SKILL.md) | 0.2.0 |

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

也可以克隆本仓库，把 `skills/talking-avatar-video` 复制到 `~/.claude/skills/`（Claude Code）、`~/.agents/skills/`（Codex）或 `~/.openclaw/skills/`（OpenClaw）。

或者把下面这段话发给你的 Agent：

```text
从 https://github.com/beatra-ai/talking-avatar-video-skill 安装 talking-avatar-video skill（目录 skills/talking-avatar-video），然后按它的 SKILL.md 连接我的 Beatra 账号。
```

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

## 更新

安装后的 skill 每天最多检查一次新版本，替换前先校验官方归档，任何一步失败都不会动你已安装的版本。
随时可以关闭，见 skill 内的 `references/automatic-updates-and-safety.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。

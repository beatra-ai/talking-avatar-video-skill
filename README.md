# Talking Avatar Video Skill

English | [简体中文](./README.zh-CN.md)

Turn one portrait and a short script into a talking avatar video, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn one portrait and a short script or speech track into a directed talking-avatar video for explainers, announcements, lessons, and product messages. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="A fictional presenter portrait (left) and a frame from the talking-avatar clip it became (right), driven by a short synthesized English line. AI-generated with Beatra."></p>

*A fictional presenter portrait (left) and a frame from the talking-avatar clip it became (right), driven by a short synthesized English line. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`talking-avatar-video`](skills/talking-avatar-video) | [SKILL.md](skills/talking-avatar-video/SKILL.md) | 0.2.0 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/talking-avatar-video). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/talking-avatar-video-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/talking-avatar-video-skill talking-avatar-video
```

Or clone this repository and copy `skills/talking-avatar-video` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the talking-avatar-video skill from https://github.com/beatra-ai/talking-avatar-video-skill (folder skills/talking-avatar-video), then follow its SKILL.md to connect my Beatra account.
```

## Examples

<p align="center"><img src="assets/preview.webp" width="800" alt="A 6-second talking-avatar clip made from one fictional portrait and a synthesized line: &quot;Hi! In thirty seconds, I&#x27;ll show you how our new planner app saves your mornings.&quot; AI-generated with Beatra."></p>

[▶ Watch the full video (MP4)](assets/full.mp4)

*Full talking-avatar clip with voice: a fictional product educator says "Hi! In thirty seconds, I'll show you how our new planner app saves your mornings." AI-generated with Beatra.*

Prompt:

```text
A friendly presenter speaks directly to camera with a warm, natural delivery: steady eye line into the lens, restrained friendly expression, subtle natural head movement and occasional blinks, relaxed shoulders. Locked-off stable camera, plain studio background stays unchanged, same face, hair and green sweater throughout.
```

## What you get

- **Prepare the speech** — Use a supplied speech track or turn a short script into reviewable narration before the video stage.
- **Direct a credible shot** — Keep expression, head movement, camera, and background restrained, then review identity and mouth timing honestly.

## Use cases

- **Product explainers** — Present a short feature, offer, or launch message without a new camera shoot.
- **Training and lessons** — Deliver a compact onboarding point, course introduction, or internal update.
- **Announcements and social** — Turn a prepared message into a human-facing announcement or talking-head post.

## FAQ

### What do I need to start?

One portrait and either a supplied speech track or a short script plus a voice choice.

### Can I use my own recorded audio?

Yes, when its type and length fit a currently supported video route.

### How are lip sync and presenter consistency reviewed?

The speech drives facial motion, and the finished clip is reviewed for mouth timing, identity, voice clarity, and motion stability before choosing the most useful adjustment.

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

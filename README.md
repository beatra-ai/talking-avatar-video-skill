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

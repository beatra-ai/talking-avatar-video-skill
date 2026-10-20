# Talking Avatar Video Skill

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

> 👉 こちらもどうぞ [Multilingual Voiceover Skill](https://github.com/beatra-ai/multilingual-voiceover-skill)

ポートレート 1 枚と短い台本から、トーキングアバター動画を作成。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | ポートレート1枚と短い台本または音声から、解説、告知、研修、商品紹介に使えるトーキングアバター動画を作ります。 |
| **モデル** | MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo、Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5 |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="架空のプレゼンターのポートレート（左）と、それを元に短い英語の合成音声で動かしたトーキングアバター動画の 1 フレーム（右）。Beatra AI で生成。"></p>

*架空のプレゼンターのポートレート（左）と、それを元に短い英語の合成音声で動かしたトーキングアバター動画の 1 フレーム（右）。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`talking-avatar-video`](skills/talking-avatar-video) | [SKILL.md](skills/talking-avatar-video/SKILL.md) | 0.3.0 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/talking-avatar-video) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/talking-avatar-video-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/talking-avatar-video-skill talking-avatar-video
```

または、このリポジトリをクローンして `skills/talking-avatar-video` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/talking-avatar-video-skill から talking-avatar-video スキル（フォルダ skills/talking-avatar-video）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 作例

<p align="center"><img src="assets/preview.webp" width="800" alt="架空のポートレート 1 枚と合成音声の 1 文「Hi! In thirty seconds, I&#x27;ll show you how our new planner app saves your mornings.」から作った 6 秒のトーキングアバター動画。Beatra AI で生成。"></p>

[▶ フル動画を見る（MP4）](assets/full.mp4)

*音声付きのトーキングアバター動画の全編：架空の製品プレゼンターが「Hi! In thirty seconds, I'll show you how our new planner app saves your mornings.」と話す。Beatra AI で生成。*

エージェントへの依頼例：

```text
./presenter.jpg をプレゼンターにして、カメラに向かって温かく自然な声でこのセリフを話させて：「Hi! In thirty seconds, I'll show you how our new planner app saves your mornings.」カメラは固定、表情は親しみやすく。
```

プロンプト：

```text
A friendly presenter speaks directly to camera with a warm, natural delivery: steady eye line into the lens, restrained friendly expression, subtle natural head movement and occasional blinks, relaxed shoulders. Locked-off stable camera, plain studio background stays unchanged, same face, hair and green sweater throughout.
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **音声合成** — 2 モデル（MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo）／FLAC、MP3、OPUS、PCM、WAV／40 言語／サンプルレート 8、16、22.05、24、32、44.1 kHz／1 リクエストあたり最大 50000 文字
  - 言語（ISO 639 コード）：zh, yue, en, es, fr, ru, de, pt, ar, it, ja, ko, id, vi, tr, nl, uk, th, pl, ro, el, cs, fi, hi, bg, da, he, ms, fa, sk, sv, hr, fil, hu, no, sl, ca, nn, ta, af
- **画像から動画** — 9 モデル（Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）／480p〜4K／2〜30 秒／アスペクト比 16:9、1:1、21:9、3:4、4:3、9:16／MOV、MP4
  - 4K：Seedance 2.0、最長 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5、最高 1080p
  - ネイティブ音声：Wan 2.7、MiniMax H3

## 得られるもの

- **ナレーションを先に整える** — 用意した音声を使うか、短い台本から聞いて確認できるナレーションを作ってから動画へ進みます。
- **伝わる演出に絞る** — 視線、表情、動き、カメラ、背景を抑え、人物と口の動きを正直に確認します。

## 活用シーン

- **商品説明** — 新しい撮影をせず、機能、キャンペーン、発売情報を短く伝えます。
- **研修とレッスン** — オンボーディング、講座の導入、社内のお知らせをコンパクトに届けます。
- **告知とSNS** — 準備したメッセージを、視聴者に向けた告知やAIプレゼンター動画にします。

## よくある質問

### 始めるために必要なものは何ですか？

鮮明なポートレート1枚と、用意した音声、または短い台本と選択済みの声が必要です。

### 自分で録音した音声を使えますか？

はい。形式と長さが現在対応している動画方式に合う場合に使えます。

### 完成後の口の動きと人物の一貫性はどう確認しますか？

音声に沿った口の動き、人物の特徴、声の聞きやすさ、映像の安定性を重点的に確認し、次に整える価値が高い一点を選びます。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update talking-avatar-video` または
`gh skill update talking-avatar-video`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai
- ドキュメント — https://docs.beatra.ai
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt（インデックス）· https://beatra.ai/llms-full.txt（全スキルを 1 ファイルに）

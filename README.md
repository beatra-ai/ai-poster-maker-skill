# AI Poster Maker Skill

English | [简体中文](./README.zh-CN.md) | [日本語](./README.ja.md)

> 👉 See also [AI Logo Maker Skill](https://github.com/beatra-ai/ai-logo-maker-skill)

Turn an event description, a product photo, or brand references into an event poster, promo banner, or social media graphic with clear visual hierarchy, category-matched style, and space kept for text, from inside Claude Code, Cursor, Codex, Windsurf, Cline, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-poster-maker-skill) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn a topic description, a product photo, or brand references into a scroll-stopping event poster, promotional banner, or social media graphic with strong visual hierarchy, category-matched styling, and text-safe zones. |
| **Models** | Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5 |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="Three 2:3 posters generated from short briefs: an indie music night for the fictional Marigold Static, a seasonal bun launch for the fictional Little Quince Bakehouse, and a minimal developer meetup poster for the fictional Tidelane Dev Meetup. AI-generated with Beatra."></p>

*Three 2:3 posters generated from short briefs: an indie music night for the fictional Marigold Static, a seasonal bun launch for the fictional Little Quince Bakehouse, and a minimal developer meetup poster for the fictional Tidelane Dev Meetup. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`poster-design-studio`](skills/poster-design-studio) | [SKILL.md](skills/poster-design-studio/SKILL.md) | 0.2.6 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/poster-design-studio). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/ai-poster-maker-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/ai-poster-maker-skill poster-design-studio
```

Or clone this repository and copy `skills/poster-design-studio` into `~/.claude/skills/` for Claude Code,
`~/.cursor/skills/` for Cursor, `~/.agents/skills/` for Codex, `~/.codeium/windsurf/skills/` for Windsurf,
`~/.cline/skills/` for Cline, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the poster-design-studio skill from https://github.com/beatra-ai/ai-poster-maker-skill (folder skills/poster-design-studio), then follow its SKILL.md to connect my Beatra account.
```

## Technical Specifications & Output Limits

As of 2026-10-18. Live list: https://docs.beatra.ai/en/docs/models

- **Uploads** — up to 100 MB per file; the per-model input limits below also apply
- **Text to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): Wan Image 2.7 Pro (up to 4 images per request); GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); PNG; up to 4 images per request; canvas up to 4.2 MP
  - 4.2 MP (2K tier): Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro (up to 4 images per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Image to video** — 9 models (Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5); 480p to 4K; 2–30 s; aspect ratios 16:9, 1:1, 21:9, 3:4, 4:3, 9:16; MOV, MP4
  - 4K: Seedance 2.0, up to 15 s
  - 30 s: Wan 3.0 Video, Wan 3.0 Video Prime, Seedance 2.5, up to 1080p
  - Native audio: Wan 2.7, MiniMax H3

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Text to image 10; Image to image 10; Image editing 6; Image to video 9 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, MiniMax Image 01 Live, Wan 2.7, Wan 3.0 Video, MiniMax H3, Seedance 2.0 Mini, HappyHorse 1.1, Seedance 2.0 Fast, Seedance 2.0, Wan 3.0 Video Prime, Seedance 2.5) (as of 2026-10-18), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw.

## What you get

- **Built for attention** — Strong visual hierarchy puts one focal subject front and center, with a clean text-safe band so your headline and details land without clashing.
- **Category-matched styling** — Tech gets clean and futuristic, food gets warm and appetizing, music gets vibrant and energetic, fashion gets editorial and bold. The poster matches the visual language of your subject.
- **Any canvas, any destination** — A-series print flyers, 1:1 social squares, 9:16 stories, 16:9 banners, and 2:3 / 3:4 standard posters—one brief, the right canvas for print or social.

## Use cases

- **Event and music posters** — Vibrant, energetic event and music festival posters with a bold headline band, a single performer or hero scene, and a structured date and venue block.
- **Movie and product launch posters** — Cinematic movie posters with dramatic lighting and title-treatment space, plus clean futuristic product launch posters that put the product center stage.
- **Sale flyers and promotional banners** — Warm, appetizing sale flyers and high-contrast promotional banners with a hero offer zone, product support, and a clear call-to-action.
- **Social media graphics** — Platform-native 1:1, 9:16, and 16:9 social graphics with one focal subject, a large text-safe zone, and high contrast readiness.

## FAQ

### Can I create a poster from just a topic description?

Yes. Describe your event, sale, movie, or campaign and the style direction. The tool generates a complete poster visual from your description with the canvas and text-safe zone you choose.

### Can I turn my product photo into a launch poster?

Yes. Upload your product photo and the tool transforms it into a polished launch poster with a clean background, brand color styling, and a text-safe band for your headline and date.

### Will there be space for my headline and details?

Yes. Every poster reserves a clean text-safe zone—top band, center, or lower third—so you can add your headline, dates, and call-to-action without clashing with the image.

### Can I fix a specific area of an accepted poster?

Yes. Upload the accepted poster, describe what to fix—a cluttered corner, color temperature, or headline contrast—and the edit targets only that area.

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update poster-design-studio` or `gh skill update poster-design-studio`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-poster-maker-skill
- Docs — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=ai-poster-maker-skill
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)

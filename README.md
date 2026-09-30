# AI Poster Maker Skill

English | [简体中文](./README.zh-CN.md)

Turn an event description, a product photo, or brand references into an event poster, promo banner, or social media graphic with clear visual hierarchy, category-matched style, and space kept for text, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn a topic description, a product photo, or brand references into a scroll-stopping event poster, promotional banner, or social media graphic with strong visual hierarchy, category-matched styling, and text-safe zones. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="Three 2:3 posters generated from short briefs: an indie music night for the fictional Marigold Static, a seasonal bun launch for the fictional Little Quince Bakehouse, and a minimal developer meetup poster for the fictional Tidelane Dev Meetup. AI-generated with Beatra."></p>

*Three 2:3 posters generated from short briefs: an indie music night for the fictional Marigold Static, a seasonal bun launch for the fictional Little Quince Bakehouse, and a minimal developer meetup poster for the fictional Tidelane Dev Meetup. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`poster-design-studio`](skills/poster-design-studio) | [SKILL.md](skills/poster-design-studio/SKILL.md) | 0.1.6 |

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
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the poster-design-studio skill from https://github.com/beatra-ai/ai-poster-maker-skill (folder skills/poster-design-studio), then follow its SKILL.md to connect my Beatra account.
```

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

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

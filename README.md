# claude-skill-ai-video-prompt

A [Claude Code](https://claude.com/claude-code) skill that helps you write stable, controllable prompts for AI video generation tools (Sora, Runway, Kling, Veo, Pika, Hailuo, Wan, Hunyuan, Luma, etc.).

It encodes a **six-dimension framework** that forces the model to establish a clear focal structure before writing, instead of piling up adjectives.

## Why

Text-to-video models work by "picking the highlights". When your prompt has no clear focus, every element fights for attention and the output becomes unstable — deformed subjects, chaotic camera work, broken timing.

This skill guides Claude to build each prompt along six dimensions, in order:

1. **Absolute subject** — exactly one protagonist
2. **Core action** — exactly one primary action
3. **Frame boundaries** — rules for background & secondary characters
4. **Camera movement** — explicit type, direction, framing
5. **Lighting & color** — directional light, contrast, tone
6. **Timeline** — second-by-second state evolution

Full framework lives in [`SKILL.md`](./SKILL.md).

## Installation

Clone this repo into your Claude Code skills directory:

```bash
git clone https://github.com/sunfjun/claude-skill-ai-video-prompt.git \
  ~/.claude/skills/ai-video-prompt
```

Restart Claude Code (or start a new session). The skill will auto-activate when relevant.

## Usage

Just ask Claude naturally. The skill triggers on phrases like:

- "帮我写一段 AI 视频提示词"
- "Write me a Sora / Kling / Runway prompt for ..."
- "改一下这段 text-to-video 提示词"
- "视频出来主体变形/不稳定,帮我调提示词"

Claude will:

1. Ask for any missing info (subject, core action, scene, duration, target model)
2. Fill the six-dimension template
3. Output **both** a structured version and a single-paragraph version (many tools don't accept tags)
4. Add targeted debugging tips

## Credits

Framework adapted from this YouTube video by **马哥 (Ma Ge)**:

> 《玩了700多天AI视频,分享一套万能提示词公式》
> https://www.youtube.com/watch?v=5fQ4_fFULKk

All credit for the six-dimension methodology goes to the original author. This repo only packages it as a Claude Code skill.

## License

MIT — see [LICENSE](./LICENSE).

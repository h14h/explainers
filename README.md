# Explainer Vids

A small bootstrap for making explainer videos with an AI coding agent. It provides a skill and style guidance; your agent designs and builds the rendering pipeline for your system and each video's needs.

_The animation is rendered from a generated JavaScript project, rather than produced by a generative video model._

## Usage

### Install the skill with Vercel Skills

Run this in the project where you want to create videos (requires Node.js and npm):

```bash
npx skills add h14h/explainers --skill promo
```

Choose your coding agent when prompted. Add `--global` to make the skill available across projects. The installer includes both bundled style references; you do not need to clone this repository.

Set `OPENROUTER_API_KEY` in your environment or your project's `.env` file, then ask your agent:

> Use the promo skill to make a whiteboard explainer video about how heat pumps work.

The skill puts the finished MP4 and its source files under your project's `videos/` directory. Your agent can also help configure local TTS instead of OpenRouter.

### Use this repository directly

1. Clone this repo and open its folder.
2. Copy the example, then add your [OpenRouter](https://openrouter.ai/) key to `.env`:
   ```bash
   cp .env.example .env
   ```
   ```dotenv
   OPENROUTER_API_KEY=your-key-here
   ```
3. Open Claude Code (Opus 5.5 is particularly good at these) or an agent that supports `.agents/skills/`. Allow it to use tools and the internet.
4. Ask (for example):
   > Use the promo skill to make a whiteboard explainer video about how heat pumps work.

Use `whiteboard`, `collage` (whimsical hand-drawn collage), or describe your own style. Optionally specify an audience or duration.

The agent creates the script, narration, animation, and finished MP4. It may need to install rendering tools. OpenRouter generation uses your account credits.

Find the video and its source files in `videos/`. Outputs and your API key are gitignored; this repo tracks only the setup and skills.

## Cost & Usage

In my experience doing this with Opus 5.5 and zero guidance on which audio models to pick, OpenRouter token costs typically come out to between $0.50 and $1.50 per video.

It _is_ possible to use local models in lieu of OpenRouter if you have the hardware; you'll just have to work with your agent to set up a pipeline that works for you.

In my testing, I was able to get perfectly usable results on an RX 7900 XTX. I've found that Breeze tends to be the best TTS model with downloadable weights (Breeze’s license disallows commercial use, though, so if your intent is to start an AI YouTube career _you have been warned_).

## Future Plans

I don't have any explicit plans for the future, but I do have some thoughts on how I might tune or refine the core skill (or add others) as I use this.

I’d like to refine TTS pacing and enunciation, and I may add a skill for creating new visual styles.

Licensed under [MIT](LICENSE). Have fun!

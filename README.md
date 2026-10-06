# Explainer videos

A small bootstrap for making explainer videos with an AI coding agent. It provides a skill and style guidance; your agent designs and builds the rendering pipeline for your system and each video's needs.

1. Clone this repo and open its folder.
2. Copy the example, then add your [OpenRouter](https://openrouter.ai/) key to `.env`:
   ```bash
   cp .env.example .env
   ```
   ```dotenv
   OPENROUTER_API_KEY=your-key-here
   ```
3. Open Claude Code or an agent that supports `.agents/skills/`. Allow it to use tools and the internet.
4. Ask:
   > Use the promo skill to make a whiteboard explainer video about how heat pumps work.

Use `whiteboard`, `collage` (whimsical hand-drawn collage), or describe your own style. Optionally specify an audience or duration.

The agent creates the script, narration, animation, and finished MP4. It may need to install rendering tools. OpenRouter generation uses your account credits.

Find the video and its source files in `videos/`. Outputs and your API key are gitignored; this repo tracks only the setup and skills.

Licensed under [MIT](LICENSE).

---
name: promo
description: Use when being asked to create an explainer video.
---

# Promo

Create a pure javascript animation about the specified subject. Use the style/branding in the style file the request names. Read that file and no other.

- `whiteboard` — [references/whiteboard.md](references/whiteboard.md)
- `collage` — [references/collage.md](references/collage.md)


If the request does not name one of those styles or provide its own description of a style, select whichever you feel is most appropriate and continue. You need not pause or ask for clarification about style.

However, if the request does not name a subject, ask for one before attempting to do anything.

The entire video should have as high a production value as is reasonably possible. It should be paced/structured to hold the viewer's attention for its duration, and viewers should naturally come away motivated to engage with the subject further (without being explicitly prompted to do so).

Use a high quality text-to-speech model for generation. For OpenRouter, read `OPENROUTER_API_KEY` from the environment or the user's working project's `.env` file. If no key is available, ask the user to configure one or use an available local TTS model. Never print keys or embed them in generated source.

Deliver a finished MP4 in `videos/` in the user's working project, with a short filename that conveys the subject. Keep its source project, assets, and temporary files in `videos/<filename-without-extension>/`. Create these directories as needed; do not write outputs into the installed skill directory. In Git projects, ensure `videos/` and any `.env` containing credentials are ignored without overwriting existing ignore rules.

Use any tools you can find access to and resources on the internet. You create the script, the assets, the animation, concept, everything.

Work autonomously until done. Quality is paramount. Production value should be on professional level.

# AGENTS.md

This repository contains the bootstrapping and skills for creating explainer videos. Generated videos and their sources are local outputs, not repository content.

## Promo videos output

Final video output should be a generated MP4. The filename should be short, but convey the relevant subject.

Place generated MP4 files in `videos/`. Put each video's source project and relevant working files in `videos/<filename-without-extension>/`. Keep all generated assets and temporary files under `videos/`, which is gitignored.

Keep skills and the `.claude/skills/` symlinks in git. Never commit API keys or `.env`.

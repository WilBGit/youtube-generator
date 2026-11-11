# Faceless YouTube Video Generator

A local-first pipeline for producing short faceless market-analysis videos from a ticker and a script. It creates a script template or accepts a written script, generates chart-style visual cards, selects an available text-to-speech backend, and combines the assets into an MP4 with ffmpeg.

## Included

- `src/video_generator.py`: command-line generator for script, voiceover, visual cards, and MP4 assembly.
- `src/channel-plan.md`: audience, content format, publishing cadence, video structure, SEO ideas, and monetization roadmap.

## Pipeline

1. Supply a ticker and either a script file or the built-in template.
2. Generate voiceover with an available local or provider-backed TTS engine.
3. Create title, analysis, support/resistance, trade-plan, and call-to-action cards.
4. Combine the cards and audio with ffmpeg.
5. Review every script, price, date, chart, disclosure, and call to action before publishing.

The current `--auto` mode generates a structured template. It is not a substitute for a verified market-data analysis pipeline.

## Usage

```text
python src/video_generator.py --ticker NVDA --auto
python src/video_generator.py --ticker NVDA --script script.txt --output output/NVDA.mp4
```

Requirements:

- Python 3.10 or newer
- ffmpeg and ffprobe for MP4 assembly
- Pillow for visual cards
- At least one TTS option: macOS `say`, gTTS, ElevenLabs, or OpenAI TTS

Provider credentials are read only from environment variables by the source. They are never stored in this repository. Generated audio, images, scripts, and videos are local output and are ignored by Git.

## Editorial and financial safety

This is a content-generation tool, not an investment adviser or an automated publisher. Market claims are drafts until reviewed against a current, authoritative data source. Do not present a generated scenario as a guaranteed outcome. Do not publish personal data, provider credentials, copyrighted material without permission, or unverified prices.

No YouTube, social-media, payment, or account credentials are included. Uploading remains a deliberate human checkpoint.

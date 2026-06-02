# Emoji CC

Emoji CC is a virtual personal IP project for creating sticker and meme assets around CC, a clean, cute, human cartoon character based on the provided reference portrait.

The first milestone is a repeatable production workflow:

- define CC's official visual anchors
- generate a stable character reference
- maintain prompt templates and a sticker backlog
- save final assets with traceable metadata

## Project Structure

- `references/` - source references, official character reference, and visual notes
- `prompts/` - reusable image generation prompts and batch prompt plans
- `assets/cc/reference/` - approved CC reference assets
- `assets/cc/drafts/` - generated drafts and rejected experiments
- `assets/cc/stickers/` - final sticker assets
- `docs/` - workflow, QA, and naming rules

## Current Direction

- IP name: CC
- Character form: human cartoon avatar
- Style: clean, cute, friendly, lightweight meme sticker energy
- First output mode: mostly textless meme stickers
- Sticker generation mode: one image with one sticker concept at a time, using a simple theme-matched background or the standard office workstation context when ambiguous
- New theme reference rule: use only the approved character and environment standards in `references/` and `assets/cc/reference/`; do not reference previous generated stickers or drafts
- Priority platform: meme stickers that can later adapt to WeChat and other social apps

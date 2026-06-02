# Production Run 001

Goal: generate the first 24 textless CC meme stickers using the official reference image.

Reference image:

`assets/cc/reference/cc-official-reference-v2.png`

Template:

`prompts/sticker-template.prompt.md`

Backlog:

`prompts/sticker-backlog.md`

## Generation Rules

- Generate one sticker per prompt.
- Use the official reference image as the identity and style anchor.
- Keep each sticker textless.
- Prefer transparent background.
- If transparency is unavailable, generate on a perfectly flat chroma-key background for local removal.
- Save every raw draft in `assets/cc/drafts/`.
- Move only approved images to `assets/cc/stickers/`.
- Update `manifest.json` after every approved sticker.

## First Pass Priority

Start with these 8 stickers to validate consistency before producing all 24:

1. `001-happy`
2. `002-received`
3. `004-thinking`
4. `006-shocked`
5. `009-tired`
6. `011-cheering`
7. `013-observe`
8. `023-salute`

If at least 6 of the 8 pass QA, continue with the remaining 16.

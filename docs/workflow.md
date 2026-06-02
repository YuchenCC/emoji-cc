# CC Sticker Production Workflow

## 1. Reference

Start every production round from the approved official CC reference in `assets/cc/reference/`. The original image in `references/cc-original-reference.png` is the source reference, not the final style lock.

## 2. Prompt

Use `prompts/sticker-template.prompt.md` for each sticker. Replace:

- `<emotion_or_action>` with the sticker meaning
- `<pose_expression_detail>` with the matching detail from `prompts/sticker-backlog.md`

Generate one sticker per prompt. Do not ask the model to create a sheet of many stickers in one image.

## 3. Output

Save drafts in `assets/cc/drafts/`. Move approved final images to `assets/cc/stickers/`.

Final sticker naming:

`cc-sticker-###-slug.png`

Example:

`cc-sticker-001-happy.png`

## 4. Metadata

Update `manifest.json` for each final asset with:

- ID and slug
- meaning
- source prompt
- final path
- status
- notes on quality or manual edits

## 5. QA

Before approving an asset:

- CC keeps short black hair, black glasses, the compact soft rounded-square / U-shaped face from the source portrait, and clean cute style.
- The expression is readable without text.
- There are no generated captions, random letters, logos, or watermarks.
- The silhouette works at small sticker size.
- Transparent edges are clean, or the flat background can be removed cleanly.

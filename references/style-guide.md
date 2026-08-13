# DingTalk Avatar Style Guide

Use this guide when generating a portrait avatar from a real photo. Read `figma-avatar-board.md` as the feature-level reference before prompting.

## Style DNA

- Format: one 1:1 square avatar, usually 1024x1024.
- Background: flat, very light pastel square. Unless the user specifies a color, randomly choose exactly one color per generated avatar from this 6-color palette: `#CEF3FF` pale blue, `#DFFFC7` mint green, `#FFD6EA` soft pink, `#FFE3D1` pale peach, `#F3F0DE` warm ivory, or `#E6E3FF` light lavender. Render it as a single flat color with no gradient, texture, environment, or photo background. Do not reuse a fixed default color across generations unless the user asks for it.
- Composition: head only; large head occupying about 76-78% of the square canvas height by default. Place the head slightly to the right of center and angle the face or gaze subtly toward the right side of the canvas. Leave enough top padding for any accessory; no neck, shoulders, shirt, collar, chest, or body detail.
- Linework: thick black hand-drawn outline, rounded corners, slightly imperfect doodle feel.
- Face: white fill, round or softly squared head, simple ears, no realistic skin shading.
- Hair: black or charcoal gray fill with visible grain or pencil texture; preserve the person's hairstyle silhouette, part, bangs, curls, or hairline.
- Features: Figma-board-inspired solid black oval/dot eyes with no highlights, chunky wedge-like brows, simple curved/short-stroke nose, small straight/downturned/shallow U mouth. Expression may be neutral, mildly unimpressed, sleepy, playful, or cute.
- Identity anchors: keep face fullness, jaw softness, eye spacing, hairstyle, facial hair, glasses, earrings, hat, or other visible head-level signature details when present.
- Head-top accessories and装扮: at most one small doodle accessory resting on or floating just above the hair, plus face/head装扮 only when requested or identity-relevant. Choose randomly when the user does not specify: sleep `ZZZ`, small crown, simple cap, sunglasses pushed onto hair, hair clip, tiny emotion mark, tiny drink bottle/can, snack, simple animal hat, round glasses, or pencil. Keep it style-consistent: thick black outline, simple silhouette, limited flat color, no readable brand text.

## Prompt Template

Use the user's portrait as the identity reference, `assets/style-reference.png` as the broad tile reference, and `assets/figma-avatar-reference-414-8411.png` as the feature-design reference.

```text
Use case: style-transfer
Asset type: square profile avatar
Input images: portrait photo = identity reference; style-reference.png = broad tile style reference; figma-avatar-reference-414-8411.png = feature-design reference for eyes, brows, nose, mouth, hair, accessories, and装扮
Primary request: Transform the person in the portrait into a cute pastel square doodle avatar matching the reference sheet and Figma avatar-board feature style.
Subject: one head-only avatar of the same person, preserving recognizable hairstyle, bangs, face fullness, eye spacing, facial hair if present, and head-level accessories.
Style/medium: black-and-white hand-drawn doodle avatar, thick black outlines, white face, charcoal-gray textured hair, solid black oval/dot eyes with no highlights, chunky wedge-like brows, tiny curved nose mark, sparse mouth, playful but restrained.
Composition/framing: large head only, occupying about 76-78% of canvas height by default, slightly right of center, face or gaze subtly angled toward the right side of the canvas, generous but not excessive padding, 1:1 square crop. Leave room only for a small top accessory. Do not include neck, shoulders, shirt, collar, chest, or necklace.
Scene/backdrop: flat single-color pastel square background, no environment. Unless the user specifies a background, randomly choose exactly one color from the skill palette: #CEF3FF, #DFFFC7, #FFD6EA, #FFE3D1, #F3F0DE, or #E6E3FF.
Color palette: white face, black outlines, grayscale hair, one randomly selected soft pastel background color from the skill palette.
Accessory/装扮: if requested, place exactly one small head-top accessory or face/head装扮 in the same doodle style; if not requested, choose one subtle random accessory or omit it. No readable logo or text.
Constraints: preserve identity cues from the portrait; no realistic skin color; no photo background; no neck or clothing; keep the accessory small and style-consistent.
Avoid: eyes with highlights, detailed pupils, oversized cropped head, tiny head, perfectly straight-on passport pose, excessive empty space, photorealistic, anime, manga, 3D render, painterly portrait, glossy vector icon, detailed shading, neck, shoulders, shirt, collar, chest, necklace, detailed body, busy background, multiple people, text labels, watermark.
```

## Subject Adaptation

- If the portrait has straight bangs or a strong hair silhouette, make that the main identity cue.
- If the portrait has glasses, keep them as simple black doodle frames.
- If the portrait has facial hair, reduce it to a few short black/gray strokes around the mouth or chin.
- If the portrait has earrings, cap, headphones, or headwear, simplify them into one or two clean lines. Omit necklaces and clothing.
- If the expression is neutral, use a calm or slightly unimpressed mouth. If the user asks for cute, use a tiny tongue-out or sleepy smile.
- If the user asks for a specific head-top accessory, use that exact object. For cola/coke, draw a tiny red cola bottle or can with a black outline and a blank white label; do not write brand text or logos.
- If the user asks for Figma-board closeness, prioritize round glasses, chunky wedge brows, curved nose stroke, gray textured spiky hair, and a simple pencil/head prop when it does not conflict with the user's requested accessory.

## Quality Checklist

Before accepting the output, verify:

- It is a single square avatar with no real-world background.
- The background is one flat color from the 6-color skill palette; it is randomized per avatar unless the user specified a color.
- It looks like the reference sheet: sparse, thick-lined, grayscale, and pastel-backed.
- The person remains recognizable from hairstyle and facial proportions.
- The head is large in the tile, roughly 76-78% of canvas height, without feeling cropped.
- The head placement and face/gaze direction feel slightly rightward rather than perfectly straight-on.
- The face is white rather than skin-toned.
- The eyes are simple solid black ovals/dots, with no highlights or detailed pupils unless the user specifically asks for another expression family.
- Brows, nose, mouth, hair, and accessories follow `figma-avatar-board.md`.
- Hair has dark gray/black fill and light texture, not realistic highlights.
- There is no neck, shoulders, clothing, extra text, watermark, or second person.
- The head-top accessory, if present, is small, style-consistent, and not the visual focus.

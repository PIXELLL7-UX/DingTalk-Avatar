# Figma Avatar Board Reference

Source: Figma file `tFgfksKDS35Gd93iabKOXV`, node `414:8411` (`头像组合测试/10`). Use `assets/figma-avatar-reference-414-8411.png` as the local visual reference.

## Extracted Component Grammar

- Canvas: the source board is an 800x800 square with flat pale blue background `#CEF3FF`. Treat this as one allowed palette option and a style reference for flat pastel backgrounds, not as the fixed default background color.
- Head scale: large head-only avatar, roughly 76-78% of canvas height including hair and ears, with no neck or clothing.
- Pose: slight right-facing/right-shifted expression. Left ear appears larger and more visible; right ear is narrower or partially behind the face/hair.
- Outline: heavy black marker stroke, rounded joins/caps, deliberately imperfect and hand-drawn.
- Face: pure white, soft round/squircle face. Keep contours simple and unshaded.
- Hair: dark gray charcoal fill with visible grain/磨砂 texture. Silhouette is chunky and angular: large spiky crown, sawtooth bangs, bold black outline. Preserve the user's real hair silhouette, but translate it into this chunky geometry.
- Eyes: simple black oval/dot pupils. When using glasses or sleepy expressions, add a single upper eyelid arc over each pupil. Avoid white glints, detailed pupils, eyelashes, or realistic eye anatomy.
- Eyebrows: thick black wedge or rounded bar shapes above the eyes. They can tilt inward/outward to create tired, worried, playful, or unimpressed expressions.
- Nose: tiny curved bridge/nostril stroke, often like a short hook or S-curve. Keep it black-only and minimal.
- Mouth: small, sparse line. Valid shapes: shallow U smile, short straight line, slight downturned line, tiny tongue-out mark if user asks for cute. Avoid lips, teeth, shading, or complex mouths.
- Facial hair: for mustache/stubble, use sparse short black strokes around mouth/chin, matching the board's simple mark language.
- Accessories: round black glasses are a strong board motif. Draw them as thick circular frames with simple bridge and optional eyelid arcs inside. Other face/head props should use the same thick outline and simplified construction.
- 装扮: pencil/head prop can cross the hair at a playful diagonal, similar to the board. Caps, headphones, small bottles/cans, crowns, hair clips, and animal hats should feel like one-layer doodle stickers, not realistic objects.

## Prompt Emphasis

When a generation needs to be closer to this Figma board, add:

```text
Feature reference: follow figma-avatar-reference-414-8411.png for component grammar: chunky spiky gray textured hair, thick black rounded outlines, pure white face, solid black oval eyes with no highlights, wedge-like eyebrows, tiny curved nose stroke, sparse simple mouth, and style-consistent face/head accessories such as round glasses or a pencil-like prop.
```

## Avoid

- Smooth anime hair, glossy vector polish, thin line art, realistic facial proportions, skin-tone face, eye highlights, detailed pupils, eyelashes, lips, teeth, clothing, neck, shoulders, brand logos, and text labels.

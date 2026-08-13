---
name: dingtalk-avatar
description: Generate identity-preserving DingTalk Avatar style pastel square doodle head avatars from real portrait photos using the bundled reference-sheet and Figma avatar-board style. Use when the user asks to turn a selfie, headshot, or真人照片 into the specific cute black-and-white avatar style with randomized soft pastel backgrounds, simplified round heads, solid oval eyes, chunky eyebrows, minimal nose/mouth, grayscale textured hair, right-facing/right-shifted pose, small head-top accessories/挂件, or face/head装扮 such as glasses and doodle props.
---

# DingTalk Avatar

## Overview

Create a single-person head-only avatar from a real portrait while preserving recognizable identity cues: face shape, hairstyle, bangs, glasses, facial hair, expression, and signature accessories that appear on the head. The final look should combine the tile variety in `assets/style-reference.png` with the Figma board component grammar in `assets/figma-avatar-reference-414-8411.png`: large head, slightly right-facing/right-shifted pose, chunky black doodle outlines, white face, solid black oval eyes, wedge-like eyebrows, minimal nose/mouth, grayscale textured hair, and small style-consistent head/face accessories.

## Workflow

1. Treat the portrait as the identity reference, `assets/style-reference.png` as the broad style reference, and `assets/figma-avatar-reference-414-8411.png` as the feature-design reference.
2. If the user provides a local portrait path and the image generation tool needs visible context, inspect it first with `view_image`.
3. Read `references/style-guide.md` and `references/figma-avatar-board.md` before generating. Use their prompt template and quality checklist.
4. Unless the user specifies a background color, randomly choose exactly one background color from the palette in `references/style-guide.md` for each avatar generation or each variant in a batch.
5. Generate a new raster image with the image generation tool. Use case: `style-transfer`.
6. Ask for clarification only when the user requests a specific expression, accessory, or background color and the requirement is ambiguous. Otherwise choose a simple expression and one optional tiny head-top accessory that fits the person's look.
7. Save the final selected image non-destructively. If the result is part of a project or deliverable, copy it into the current workspace or outputs folder.

## Required Style Anchors

- Square pastel background, no environment, no photo background. The default background is randomized: choose one flat color from the skill palette per generation; do not treat the Figma pale blue as a fixed default.
- Head-only avatar, large in frame. The default selected size is option C: the head should occupy about 76-78% of the square canvas height while leaving enough top padding for any accessory. Place the head slightly to the right of center and angle the face or gaze subtly toward the right side of the canvas. Do not draw neck, shoulders, shirt, collar, or chest.
- Thick black outer contour and simple hand-drawn linework.
- White face with no skin-color rendering.
- Hair in dark gray or black with subtle pencil-like grain.
- Facial features follow the Figma board: solid black oval/dot eyes with no highlights, thick wedge-like brows, tiny curved stroke nose, and a sparse straight, downturned, or shallow U-shaped mouth.
- Preserve identity cues from the photo; do not beautify into a generic anime character.
- Add at most one playful head-top accessory/挂件 when requested or when a random accessory is appropriate. Face/head装扮 such as round glasses, a pencil, cap, or headwear may be used only when requested or identity-relevant. Keep every accessory in the same doodle style: thick black outline, very simple shape, limited color, no readable brand text.

## Avoid

- Photorealism, semi-realistic painting, anime, manga, 3D, vector-logo polish, glossy gradients, complex backgrounds, neck, shoulders, shirt, collar, chest, detailed skin tones, heavy shadows, text labels, watermarks, and multiple people.
- Overloading the avatar with accessories or drawing full-body clothing. The style works because it is sparse.

## Bundled Resources

- `assets/style-reference.png`: reference sheet for the exact target visual style.
- `assets/figma-avatar-reference-414-8411.png`: Figma avatar-board reference for eyes, brows, nose, mouth, hair, accessories, and装扮.
- `references/style-guide.md`: prompt recipe, negative prompt, and validation checklist.
- `references/figma-avatar-board.md`: extracted Figma feature grammar.

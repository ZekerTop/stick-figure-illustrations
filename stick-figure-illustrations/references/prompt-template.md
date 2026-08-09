# Prompt Template

每张图单独生成。根据内容替换变量。

## 单张插画

```text
Create one standalone stick-figure sketch illustration.

Purpose:
{article body illustration / newsletter header / social carousel page / slide spot illustration / product doc empty state / tutorial step / open-source README illustration / SaaS state illustration}

Canvas:
{16:9 by default unless the user or selected preset specifies another canvas}

Visual system:
Neutral stick figures are required by default and should be the main visual subject unless the user explicitly asks for no people. Use simple circular heads, thin black line bodies, simple arms and legs, no named character, no mascot identity, no invented species or signature character design. Normal figures must have clean readable anatomy: one head, one torso, two arms, and two legs. Do not accidentally add extra hands, extra feet, broken limbs, fused limbs, or unclear limb counts. Extra arms, repeated hands, motion trails, or exaggerated limbs are allowed only when the core idea explicitly communicates being very busy, multitasking, or all-capable, and the image must make that intention obvious. The stick figure must not be expressionless: give it a readable emotion through minimal eyes, eyebrows, mouth, head tilt, hand gesture, shoulder angle, and body posture. Clean black marker-like line art on a white or transparent-white background. Plenty of whitespace. Use only one restrained accent color: {accent color or auto-selected calm accent}. The accent color should mark the main path, current step, result, warning, or focal object.

Theme:
{主题}

Core idea:
{这张图要表达的核心意思}

Composition pattern:
{Before/After / Path / Hand-off / Stack / Split-Merge / Trade-off / Obstacle / Loop / Container / Workbench / Checklist / Map / Signal-Noise / Zoom-in / Custom}

Composition:
{具体画面：火柴人在哪里、正在做什么、是什么情绪、主要物件是什么、信息如何移动或变化}

Suggested objects:
{物件1} / {物件2} / {物件3}

Required expressive labels:
Unless the user explicitly asks for no text, include readable short labels that make the image understandable and more fun: 1 short title or punchline, plus 2-5 object/state/action labels. Label the important objects, path, current step, blocker, result, or contrast words. Use the user's language. Keep labels short; do not write paragraphs.

Label plan:
{短标题或 punchline} / {关键物件标签} / {状态词} / {动作词} / {结果词}

Brand/accent color:
{user-provided brand color, or auto-select one calm accent color}. Use this as the only accent color.

Constraints:
One image explains one idea. Keep the composition readable at small sizes. Labels should make the image more expressive and self-explanatory: use words to strengthen emotion, contrast, rhythm, or memorability, and label key objects so viewers are not forced to guess. Concise labels are fine, richer label sets are also fine when they serve the idea. Avoid paragraph-like explanations, crowded text, dense diagrams, PPT template aesthetics, complex vector illustration, 3D, photorealism, textured paper, gradients, shadows, UI screenshots, cute stickers, non-human mascots, blob mascots, filled mascot characters, accidental extra hands, accidental extra feet, broken or fused limbs, named IP characters, and references to any specific artist, creator, brand, or existing illustration style.
```

## 从 shot list 生成单张图

```text
Create one standalone stick-figure sketch illustration from this selected shot:

{粘贴 shot list 中的一条}

Follow the selected canvas, channel, core idea, composition pattern, stick-figure action, stick-figure emotion, main objects, labels, and accent color. Neutral stick figures must remain the main subject. Include the selected labels as visible short text unless the shot explicitly says no text. Keep the image readable, emotionally clear, lightly witty when appropriate, and not like a PPT diagram.
```

## 无文字版本

```text
Create the same illustration as a clean no-text version. Remove all written labels and symbols that look like text. Preserve the core stick-figure action, simple composition, black line art, one accent color, whitespace, and canvas ratio.
```

## 改图：减少文字

```text
Edit the provided image. Remove most written labels and keep only these short labels: {labels to keep}. Preserve the stick-figure action, composition, line style, accent color, canvas ratio, and image quality. Do not add new objects.
```

## 改图：去 IP 化

```text
Edit the provided image to remove any mascot or recognizable character identity. Replace the character with a neutral stick figure: circular head, line body, exactly two simple arms and two simple legs for normal figures, no accidental extra hands or feet, no fused limbs, no filled body, no distinctive costume, and a simple readable expression that matches the scene emotion. Preserve the same conceptual action, composition, labels, accent color, and canvas ratio.
```

## 改图：适配品牌色

```text
Edit the provided image. Keep the black line art and white/transparent background. Replace the accent color with {brand color}. Do not change the stick figures, composition, labels, or object layout.
```

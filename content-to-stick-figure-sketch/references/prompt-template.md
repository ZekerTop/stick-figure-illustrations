# Prompt Template

每张图单独生成。根据内容替换变量。

## 单张插画

```text
Create one standalone stick-figure sketch illustration.

Purpose:
{article body illustration / newsletter header / social carousel page / slide spot illustration / product doc empty state / tutorial step / open-source README illustration / SaaS state illustration}

Canvas:
{16:9 / 3:2 / 1:1 / 4:5 / 9:16 / transparent-background spot illustration}

Visual system:
Neutral stick figures are required by default and should be the main visual subject unless the user explicitly asks for no people. Use simple circular heads, thin black line bodies, simple arms and legs, no named character, no mascot identity, no invented species or signature character design. Clean black marker-like line art on a white or transparent-white background. Plenty of whitespace. Use only one accent color: {accent color}. The accent color should mark the main path, current step, result, warning, or focal object.

Theme:
{主题}

Core idea:
{这张图要表达的核心意思}

Scene pattern:
{Before/After / Path / Hand-off / Stack / Split-Merge / Trade-off / Obstacle / Loop / Custom}

Composition:
{具体画面：火柴人在哪里、正在做什么、主要物件是什么、信息如何移动或变化}

Suggested objects:
{物件1} / {物件2} / {物件3}

Optional labels:
{短标注1} / {短标注2} / {短标注3} / {可选短标注4}

Brand/accent color:
{green / blue / orange / purple / #hex}. Use this as the only accent color.

Constraints:
One image explains one idea. Keep the composition sparse and readable at small sizes. Use at most 0-5 short labels. Avoid dense diagrams, PPT template aesthetics, complex vector illustration, 3D, photorealism, textured paper, gradients, shadows, UI screenshots, cute stickers, non-human mascots, blob mascots, filled mascot characters, named IP characters, and references to any specific artist, creator, brand, or existing illustration style.
```

## 从 shot list 生成单张图

```text
Create one standalone stick-figure sketch illustration from this selected shot:

{粘贴 shot list 中的一条}

Follow the selected canvas, channel, core idea, stick-figure action, main objects, labels, and accent color. Neutral stick figures must remain the main subject. Keep the image sparse, readable, and not like a PPT diagram.
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
Edit the provided image to remove any mascot or recognizable character identity. Replace the character with a neutral stick figure: circular head, line body, simple arms and legs, no filled body, no distinctive costume, no fixed expression. Preserve the same conceptual action, composition, labels, accent color, and canvas ratio.
```

## 改图：适配品牌色

```text
Edit the provided image. Keep the black line art and white/transparent background. Replace the accent color with {brand color}. Do not change the stick figures, composition, labels, or object layout.
```

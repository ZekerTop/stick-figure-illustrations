# Prompt Examples

Copy these prompts into Codex and replace the placeholders.

## Best Starting Prompt

```text
Use $stick-figure-illustrations to read the content below. Do not generate any images yet.

Please create a stick-figure sketch shot list:
- Select only the 5 strongest visual thinking anchors
- Improve visual feel, reading rhythm, or understanding; do not add images just to add them
- For each image, include: placement, canvas, theme, core idea, stick-figure action, emotion, main objects, short labels, and priority
- Each image should express one idea only
- Keep the stick figure as the main subject by default
- Use fewer than 5 images if there are not enough good placements
- End by marking the best 2 images to generate first

<Paste content>
```

## Generate From One Idea

```text
Use $stick-figure-illustrations to generate one stick-figure sketch illustration for this idea:

"Real automation is not about fewer clicks. It is about making one less decision."

Requirements:
- 16:9 canvas
- white background with black line art
- one green accent color
- a neutral stick figure as the main subject
- readable emotion through simple face marks and posture
- no more than 3 short labels
```

## Article Illustrations

```text
Use $stick-figure-illustrations with the article preset to plan 5 stick-figure sketch illustrations for this article.
Output the shot list first. Do not generate images yet.

Requirements:
- 16:9 or 3:2
- improve the article's visual feel and reading rhythm; do not add illustrations just to add them
- each image should show one cognitive turning point
- the stick figure must carry the core action
- give each stick figure a clear emotion
- no more than 3 labels per image
- use fewer than 5 images if there are not enough good placements
- mark the best 2 images to generate first

<Paste article>
```

## Article Reading Flow + Direct Generation

```text
Use $stick-figure-illustrations with the article preset to process the article below.

Please complete this directly:
1. Decide which placements would improve visual feel, reading rhythm, or understanding
2. Do not add illustrations just to add them; use fewer images or none if there are no good placements
3. For each image, provide the exact placement: section name + after which paragraph or sentence
4. Generate the P0/P1 images and show them directly
5. Provide Markdown insertion code for each image
6. Explain in one sentence why the image makes that spot easier to read

Requirements:
- 16:9 or 3:2
- each image should express one idea only
- the stick figure must carry the core action, with clear but restrained emotion
- no more than 3 labels; generate a no-text version when useful
- if working in a workspace, save images to assets/<article-slug>-illustrations/

<Paste article>
```

## Social Carousel

```text
Use $stick-figure-illustrations with the carousel preset to design a 7-page social carousel for this topic.
Output the shot list first. Do not generate images yet.

Topic: How one person turns AI into a daily workflow

Requirements:
- 4:5 canvas
- one stick-figure action per page
- a clear emotion on each page
- one short title per page
- page 1 needs a strong hook
- page 7 should close with an action
```

## PPT / Keynote

```text
Use $stick-figure-illustrations with the slides preset to design 6 stick-figure sketch illustrations for this talk outline.

Use cases:
- section transition slides
- supporting visuals beside key ideas
- a closing action slide

Requirements:
- 16:9
- as little text as possible
- the stick-figure action should read at a glance
- avoid a PPT template look

<Paste outline>
```

## SaaS Empty State

```text
Use $stick-figure-illustrations with the saas-state preset to generate one stick-figure sketch illustration:

State: The user has not created any project yet.

Requirements:
- white or transparent background
- a neutral stick figure stands next to an empty folder and holds the first card
- one brand-green accent color: #22c55e
- no text
- suitable for the center area of a product UI
```

## Open-Source README

```text
Use $stick-figure-illustrations with the readme preset to design a 4-image stick-figure sketch shot list for this open-source README.

Scenes:
1. Install
2. Configure
3. Submit an issue
4. Open a PR

Requirements:
- engineering-document tone
- avoid a marketing-poster feel
- each image needs a clear stick-figure action
```

## Tutorial / Course

```text
Use $stick-figure-illustrations with the course preset to break the tutorial below into 5 stick-figure step illustrations.

Requirements:
- each image should match one learning action
- 16:9 canvas
- keep one consistent stick-figure proportion system
- no more than 2 short labels per image
- after the shot list, generate image 1

<Paste tutorial>
```

## Complex Concept

```text
Use $stick-figure-illustrations to generate one stick-figure sketch illustration for this concept:

"Trust is not argued into existence. It is built by laying down evidence piece by piece."

Requirements:
- a stick figure lays evidence cards one by one to form a bridge
- one side of the bridge is "unknown" and the other side is "trust"
- one orange accent color
- do not render it like a flowchart
```

## Product Launch

```text
Use $stick-figure-illustrations to design 3 stick-figure sketch concepts for this feature launch.
Output the concepts first. Do not generate images yet.

Feature: Automatically turn meeting recordings into task lists.

Requirements:
- Concept A: user pain point
- Concept B: how the feature works
- Concept C: the after state
- each concept should explain what the stick figure is doing
```

## Edit / Redraw

```text
Use $stick-figure-illustrations. This image has the right idea, but it looks too much like a flowchart.
Please regenerate it with these changes:

- keep the core idea
- turn it into a natural scene
- let the stick figure carry the main action
- remove the big title and extra nodes
- white background, black line art, one green accent color
```

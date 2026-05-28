# Emotional Stick-Figure Design

## Context

The current skill over-emphasizes neutral stick figures. That keeps outputs simple and non-IP, but it also nudges image prompts toward stiff, expressionless figures.

The desired behavior is still stick-figure sketch illustration, not a switch to comic characters or generic line people. The change is that stick figures must carry visible emotion.

## Decision

Keep the skill identity as stick-figure sketching, but redefine the default subject as an emotionally expressive neutral stick figure.

Default figures should remain:

- anonymous
- low-detail
- simple line bodies
- black line art with at most one accent color
- free of mascot, IP, brand, or fixed character identity

Default figures must no longer be:

- blank-faced
- stiffly standing without emotional posture
- treated as decorative neutral icons
- upgraded into complex cartoon characters

## Visual Rules

An expressive stick figure can use a few simple emotional signals:

- dot eyes, eyebrow strokes, and a short mouth line
- head tilt
- shoulder angle
- hand gesture
- body lean
- small motion or tension marks
- distance from an object or another figure

Every generated image should have one clear emotional state that supports the content, such as confusion, relief, hesitation, focus, frustration, curiosity, confidence, surprise, or calm.

The emotion must stay restrained. It should clarify the idea, not turn the figure into a meme, mascot, cute sticker, or dramatic cartoon character.

## Workflow Changes

Shot lists should describe both:

- what the stick figure is doing
- what emotion the stick figure shows

For example:

- "a confused stick figure sorting a messy pile of task cards"
- "a relieved stick figure placing the final card in the done area"
- "a hesitant stick figure comparing two paths"

Prompt templates should keep stick-figure wording, but add explicit expression and posture requirements. They should avoid language that implies expressionless neutral figures.

QA should reject images where the figure has no readable expression or emotional posture.

## Files To Update

- `content-to-stick-figure-sketch/SKILL.md`
- `content-to-stick-figure-sketch/references/visual-system.md`
- `content-to-stick-figure-sketch/references/prompt-template.md`
- `content-to-stick-figure-sketch/references/shot-list-schema.md`
- `content-to-stick-figure-sketch/references/qa-checklist.md`
- `README.md`
- `examples/prompts.md`
- `content-to-stick-figure-sketch/agents/openai.yaml`

## Non-Goals

- Do not rename the skill id or folder.
- Do not remove the stick-figure positioning.
- Do not introduce fixed characters, mascots, costumes, or creator-style references.
- Do not add a multi-color emotional coding system.
- Do not turn the skill into finished commercial illustration or comic character generation.

## Verification

After implementation, check that:

- searches for "无表情" only appear in rejection or failure contexts
- main prompts still say stick figure or 火柴人
- prompts require visible emotion through expression and posture
- QA has a clear failure case for blank or emotionally irrelevant figures
- examples mention emotional action where it helps generation quality

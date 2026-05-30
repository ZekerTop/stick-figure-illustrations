# Shot List Schema

Use this schema when planning illustrations before generation.

## Default Output

For each candidate image, output:

```markdown
| # | Priority | Placement | Canvas | Theme | Core idea | Scene pattern | Stick-figure action | Emotion | Main objects | Labels | Generate? |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | P0 | after section X | 16:9 | ... | ... | Before/After | ... | ... | ... | ... | yes |
```

## Fields

- `Priority`: `P0` for must-generate, `P1` for useful, `P2` for optional.
- `Placement`: where this image belongs, such as opener, after a paragraph, slide 3, carousel page 2, empty state, README section.
- `Canvas`: `16:9`, `3:2`, `1:1`, `4:5`, `9:16`, `2:1`, or transparent spot illustration.
- `Theme`: short title for internal planning, not necessarily text in the image.
- `Core idea`: one sentence. If it needs two sentences, split it into two images.
- `Scene pattern`: choose from Before/After, Path, Hand-off, Stack, Split-Merge, Trade-off, Obstacle, Loop, or Custom.
- `Stick-figure action`: the exact action the figure performs. Avoid “standing beside”.
- `Emotion`: the readable emotional state of the figure, such as confused, relieved, hesitant, focused, calm, or excited.
- `Main objects`: 1-3 simple objects only.
- `Labels`: 0-5 short labels. Prefer 0-3.
- `Generate?`: `yes`, `maybe`, or `no`.

## Priority Rules

Choose `P0` when the image:

- explains a key idea faster than text
- marks a major turn in the argument
- helps a reader remember the piece
- can become a reusable thumbnail or social card

Choose `P1` when the image:

- supports flow or pacing
- clarifies a step, but the text still works without it
- is useful for a slide or carousel, but not essential

Choose `P2` when the image:

- is decorative
- repeats a prior idea
- depends on too much text
- would use up image generation without improving understanding

## Planning Rules

- Do not average one image per section.
- Prefer fewer, stronger images.
- Give the figure a clear action and a clear emotion in every candidate image.
- Do not generate until the best 1-3 candidates are clear, unless the user explicitly asks to generate all.
- End every shot list with: `Recommended first generation: #...` and one short reason.

# Content-to-Stick-Figure-Sketch Skill

[中文](./README.md) | English

This is a Codex creative-assistance skill for turning articles, docs, tutorials, slides, social content, open-source project explainers, and product states into sketch-style explanatory illustrations with **emotionally expressive neutral stick figures** as the default main subject.

```text
Display name: 内容转火柴人草图
Skill ID: content-to-stick-figure-sketch
Usage: Use $content-to-stick-figure-sketch ...
```

This skill is not about generating a fixed mascot, a character IP, or an imitation of one creator's signature style. It is about turning abstract ideas into easy-to-understand **action scenes**: a stick figure choosing, sorting, handing off, fixing, building, observing, or moving through an obstacle while showing readable emotion through minimal expression and posture.

Default visual language:

- anonymous stick figures with circular heads, line bodies, simple limbs, and readable emotion
- white or transparent background
- black line art
- no more than one accent color
- plenty of whitespace
- one core idea per image
- no imitation of any specific creator, brand, IP, illustrator, or public reference style

## What It Is Good For

This skill is best for turning the parts of a text that truly need to be seen into sketch concepts, rather than forcing one image into every section.

Common use cases:

| Use case | Best outputs | Default canvas |
|---|---|---|
| Articles / blogs | body illustrations, key-idea visuals, before/after visuals | `16:9` / `3:2` |
| Newsletters | email header visuals, summary visuals, pacing visuals | `2:1` / `16:9` |
| Social carousels | 5-8 connected concept slides, one action per page | `4:5` / `1:1` |
| PPT / Keynote | section transitions, side visuals for key ideas, closing action visuals | `16:9` |
| Product docs | install, import, permission, error recovery, success state visuals | `16:9` / `3:2` / square |
| Tutorials / courses | step visuals, exercise visuals, feedback-loop visuals | `16:9` / `4:3` |
| Open-source projects | README, contribution flow, issue / PR / release flow | `16:9` / `2:1` |
| SaaS UI states | empty states, error states, loading states, permission states, success states | `1:1` / `3:2` / transparent spot |
| Video / podcast / event ideas | thumbnail concepts, visual metaphors for themes | `16:9` / `1:1` |

## What It Is Not For

Do not use this skill to generate:

- fixed mascots, character IP, meme characters, or cute stickers
- complex commercial illustration, 3D, skeuomorphic visuals, real screenshots, or brand KVs
- formal flowchart templates, complex architecture diagrams, or dense PPT infographics
- imitations of a specific illustrator, creator, brand, or existing public example
- poster or cover finals that depend on heavy typography

If you need a polished designer-grade poster, this skill is better used as an early concept-sketch and shot-list tool.

## Installation

### Recommended: Ask Codex to install it directly

Start a new conversation in Codex, paste this GitHub link, and ask Codex to install it:

```text
Please install this Codex skill:
https://github.com/ZekerTop/content-to-stick-figure-sketch
```

Codex will read the skill files in this repository and install them into the local skills directory. After installation, follow Codex's prompt to refresh or restart Codex.

If you forked the repo, replace the link with your own GitHub repository URL.

### Install from local source

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./content-to-stick-figure-sketch "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Then restart Codex.

## Quick Start

Start by asking the skill to plan a shot list before generating images:

```text
Use $content-to-stick-figure-sketch to read the content below. Do not generate any images yet.

Please create a stick-figure sketch shot list:
- Select only the 5 strongest visual thinking anchors
- For each image, include: placement, canvas, theme, core idea, stick-figure action, emotion, main objects, short labels, and priority
- Each image should express one idea only
- Keep the stick figure as the main subject by default
- End by marking the best 2 images to generate first

<Paste content>
```

Why start with a shot list:

- long pieces should not get one image per section by default
- one image per idea helps avoid dense infographics and PPT-template energy
- choosing the `P0` images first saves generation budget
- you can confirm composition before moving on to generation or edits

## Workflow

### 1. Read the content and find visual anchors

The skill first identifies the parts of the content that are worth visualizing, such as:

- core judgments
- simple metaphors for hard concepts
- before/after contrasts
- user pain points
- step transitions
- input/output changes
- decision forks
- outcome states

Text that does not benefit from illustration should be skipped.

### 2. Output a shot list

By default, the skill proposes 3-6 candidate images. Short content may only need 1-2; long articles, courses, or carousels may expand to 8-10, but each image should have a clear purpose.

Recommended format:

| # | Priority | Placement | Canvas | Theme | Core idea | Scene pattern | Stick-figure action | Emotion | Main objects | Labels | Generate? |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | P0 | opener | 16:9 | From clutter to path | Turn scattered tasks into an actionable route | Before/After | A stick figure arranges scattered cards into a path | confused, then focused | cards / path / flag | input / path / output | yes |

Priority definitions:

- `P0`: must generate; strongly improves clarity or shareability
- `P1`: useful; improves pacing or support
- `P2`: optional; likely decorative or repetitive

### 3. Generate one selected image at a time

The prompt should emphasize:

- a neutral stick figure as the main subject
- a readable emotion through face and posture
- white or transparent background
- black line art
- one accent color
- whitespace
- a few short labels, or a no-text version
- no third-party IP, fixed characters, or specific creator-style imitation

Each image is generated separately unless the user explicitly wants a multi-panel overview.

### 4. Check and iterate

Use the QA checklist after generation:

- does the stick figure carry the core action?
- does the stick figure show readable emotion instead of standing blankly?
- did it turn into a mascot, meme, animal, or complex character?
- does the image express only one core idea?
- does it still read clearly when small?
- does it look too much like a PPT template or formal flowchart?
- is there only one accent color?
- are there too many labels?
- does it imitate a known style, brand, or public example?

If text quality is unreliable, generate a no-text version first and add labels later in a design tool.

## Presets

Presets make the output more stable:

| Preset | Purpose | Default count | Canvas | Focus |
|---|---|---:|---|---|
| `article` | blog posts, articles, long-form notes | 3-6 | `16:9` / `3:2` | key cognitive turns |
| `newsletter` | emails, weekly digests, curated notes | 1-3 | `2:1` / `16:9` | lightweight pacing |
| `carousel` | social carousels | 5-8 | `4:5` / `1:1` | one action per page |
| `slides` | PPT, Keynote, talks | 3-8 | `16:9` | support the idea without stealing hierarchy |
| `product-doc` | product docs, help center content | 2-5 | `16:9` / `3:2` / spot | user tasks and system states |
| `saas-state` | empty, error, permission, loading, success states | 1 | `1:1` / `3:2` / transparent spot | no text, UI-friendly |
| `course` | tutorials, courses, handouts | 4-10 | `16:9` / `4:3` | learning actions |
| `readme` | open-source README, contribution guide, release notes | 2-4 | `16:9` / `2:1` | engineering-doc tone |
| `thumbnail` | video, podcast, event, article-cover concepts | 1-3 | `16:9` / `1:1` | strong metaphor, not final poster art |

Example:

```text
Use $content-to-stick-figure-sketch with the carousel preset to design a 7-page social carousel for this topic.
Output the shot list first. Do not generate images yet.

Topic: How one person turns AI into a daily workflow

Requirements:
- 4:5 canvas
- one stick-figure action per page
- one short title per page
- page 1 needs a strong hook
- page 7 should close with an action
```

## Copy-Paste Examples

### Plan illustrations for an article

```text
Use $content-to-stick-figure-sketch with the article preset to plan 5 stick-figure sketch illustrations for this article.
Output the shot list first. Do not generate images yet.

Requirements:
- 16:9 or 3:2
- each image should show one cognitive turning point
- the stick figure must carry the core action
- no more than 3 labels per image
- mark the best 2 images to generate first

<Paste article>
```

### Generate one idea illustration

```text
Use $content-to-stick-figure-sketch to generate one stick-figure sketch illustration for this idea:

"Real automation is not about fewer clicks. It is about making one less decision."

Requirements:
- 16:9 canvas
- white background with black line art
- one green accent color
- a neutral stick figure as the main subject
- no more than 3 short labels
```

### Create a SaaS empty state

```text
Use $content-to-stick-figure-sketch with the saas-state preset to generate one stick-figure sketch illustration:

State: The user has not created any project yet.

Requirements:
- white or transparent background
- a neutral stick figure stands next to an empty folder and holds the first card
- one brand-green accent color: #22c55e
- no text
- suitable for the center area of a product UI
```

### Plan README illustrations for an open-source project

```text
Use $content-to-stick-figure-sketch with the readme preset to design a 4-image stick-figure sketch shot list for this open-source README.

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

More examples: [examples/prompts.md](./examples/prompts.md)

## Scene Patterns

Each image should use one base pattern:

| Pattern | Best for | Typical composition |
|---|---|---|
| `Before/After` | clutter to clarity, manual to automated, guessing to validated | old state on the left, new state on the right, a transition action in the middle |
| `Path` | user journey, learning path, release flow | figure moves through 3-5 nodes |
| `Hand-off` | collaboration, agent relay, content pipeline | figure passes an object |
| `Stack` | method hierarchy, capability stack, high-level architecture | figure builds or checks layered boxes |
| `Split-Merge` | branching, aggregation, multi-channel output | one input splits into outputs, or several inputs converge |
| `Trade-off` | speed vs quality, automation vs control | figure chooses between a scale, slider, or two doors |
| `Obstacle` | blockers, permissions, bugs, overload | figure removes, bypasses, or marks an obstacle |
| `Loop` | feedback loop, iteration, training, review | figure pushes a simple cycle |

## Repository Structure

```text
content-to-stick-figure-sketch/
├── README.md
├── README.en.md
├── examples/
│   └── prompts.md
├── content-to-stick-figure-sketch/
│   ├── SKILL.md
│   ├── agents/
│   │   └── openai.yaml
│   └── references/
│       ├── presets.md
│       ├── prompt-template.md
│       ├── qa-checklist.md
│       ├── scene-patterns.md
│       ├── shot-list-schema.md
│       ├── use-cases.md
│       └── visual-system.md
└── .gitignore
```

## Reference Files

| File | Purpose |
|---|---|
| `content-to-stick-figure-sketch/SKILL.md` | skill entry point, trigger conditions, hard boundaries, and workflow |
| `references/visual-system.md` | visual rules, color, text, and anti-patterns |
| `references/use-cases.md` | recommended output shapes for different scenarios |
| `references/presets.md` | canvas, count, density, and goals for each preset |
| `references/shot-list-schema.md` | shot list fields and priority rules |
| `references/scene-patterns.md` | composition patterns and metaphor-generation methods |
| `references/prompt-template.md` | generation, no-text, and edit prompt templates |
| `references/qa-checklist.md` | post-generation checks and iteration rules |
| `examples/prompts.md` | copy-paste usage examples |

## Maintenance Notes

When you update this skill, keep these three things aligned first:

1. The workflow in `SKILL.md` should match the explanation in the README.
2. The preset names in `references/presets.md` should match the tables in the README.
3. The examples in `examples/prompts.md` should cover the most common use cases, not just article illustrations.

When adding a new preset, update at least:

- `content-to-stick-figure-sketch/references/presets.md`
- `content-to-stick-figure-sketch/references/use-cases.md`
- `examples/prompts.md`
- `README.md`
- `README.en.md`

## License

No license has been selected yet. Choose a license before publishing this as an open-source project.

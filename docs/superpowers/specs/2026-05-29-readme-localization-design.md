# README Localization Design

## Context

The repository currently uses a single `README.md` as the main landing page.

The new requirement is to support both Chinese and English documentation without turning the main README into a mixed-language wall of text. Chinese should remain the default landing language.

## Decision

Use two full README files:

- `README.md` as the default Chinese entry point
- `README.en.md` as the full English entry point

This keeps the repository homepage clean, obvious, and easy to maintain.

## Language Model

The documentation model should be:

- Chinese-first at the repository root
- English available as a first-class parallel document
- no inline bilingual duplication inside one README
- no generated docs system, switcher widget, or docs routing layer

At the top of both files, include a minimal language switch:

- in `README.md`: `中文 | [English](./README.en.md)`
- in `README.en.md`: `[中文](./README.md) | English`

This is enough. Anything more is noise.

## Content Rules

The two README files should have matching structure and roughly matching content coverage:

- title and short positioning
- what the skill does
- suitable use cases
- non-goals
- installation
- quick start
- workflow summary
- presets
- copy-paste examples
- repository structure

The wording can adapt naturally between languages, but the meaning and feature coverage should stay aligned.

## Prompt Example Rules

Copy-paste prompt blocks intended for direct use in the input box should remain in English.

That rule applies in both README files. Chinese prose can explain the feature in `README.md`, but the prompt blocks themselves should stay English for broader reuse and consistency.

## File Strategy

Files expected to change:

- `README.md`
- `README.en.md`

Possible supporting touch-up:

- `examples/prompts.md` if cross-links or wording need to stay aligned with the new README structure

## Non-Goals

- Do not create a single bilingual README with duplicated sections.
- Do not move the main documentation into `docs/` just to simulate language separation.
- Do not add a complex language switcher, badges, or navigation framework.
- Do not make English the default repository landing page.

## Verification

After implementation, verify that:

- `README.md` exists and is clearly Chinese-first
- `README.en.md` exists and is clearly English-first
- both files link to each other at the top
- the major sections match across both files
- copy-paste prompt blocks are in English in both files
- GitHub users landing on the repo first see the Chinese README by default

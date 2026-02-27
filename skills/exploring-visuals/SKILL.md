# Exploring Visuals

## Purpose

Generate image generation prompts grounded in the project's aesthetic vocabulary. Takes vocabulary terms, reference materials, and design intent as input and produces structured prompts for `{{generation_tool}}`.

## When to Use

- Exploring visual directions for a new design area
- Generating variations on an established aesthetic
- Testing vocabulary terms as visual prompt components

## Workflow

1. **Load vocabulary**: Read `{{vocabulary_path}}` for active terms
2. **Review intent**: Understand what aspect of the design needs exploration
3. **Compose prompts**: Build generation prompts using vocabulary terms as anchors
4. **Structure output**: Format prompts with positive terms, negative terms, and style parameters

## Context Slots

| Slot | Default | Description |
|------|---------|-------------|
| `{{grimoire_path}}` | `grimoires/the-easel/` | Root path for this construct's project state |
| `{{vocabulary_path}}` | `{{grimoire_path}}/vocabulary/atlas.md` | Path to the vocabulary atlas |
| `{{generation_tool}}` | `your preferred image generation tool` | The tool or service used for image generation |

## Prompt Structure

Each generated prompt includes:
- **Positive terms**: Vocabulary words that define the desired aesthetic
- **Negative terms**: Vocabulary words that define what to avoid
- **Style parameters**: Technical parameters appropriate to `{{generation_tool}}`
- **Rationale**: Why these terms were chosen (links back to vocabulary)

## Outputs

- One or more structured generation prompts
- Vocabulary term mapping (which terms from the atlas were used and why)
- Suggested variations for iterative exploration

## Acceptance Criteria

- Prompts reference only terms from the vocabulary atlas
- Negative terms are specified where relevant
- Rationale traces back to vocabulary definitions
- Output format is compatible with `{{generation_tool}}`

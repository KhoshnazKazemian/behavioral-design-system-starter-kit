# Publish Pattern → Notion

Use this after a pattern Markdown file has been generated, reviewed, and approved.

The AI Feature Unpacker skill does NOT publish automatically.

The generated Markdown file stays the source of truth.

Publishing is a separate step.

---

## When to use

Use this when:

- the pattern file already exists
- the documentation is reviewed
- you want to move it into a Notion database

Source example:

outputs/generated-patterns/[file-name].md

Destination example:

Notion Interaction Pattern Library

---

## Example Prompt

Publish this pattern into my Notion database.

Source file:
outputs/generated-patterns/[file-name].md

Destination:
[paste Notion database link]

Rules:
- Use Markdown as source of truth
- Create new page
- Preserve headings and tables
- Map metadata into database properties
- Keep Add later sections
- Do not rewrite content
- Ask for permission if access is needed

---

## Publishing Rules

### Preserve

- title
- metadata
- section structure
- tables
- version history
- Add later sections

### Do NOT

- rewrite sections
- expand content
- invent examples
- change metadata
- generate implementation details
- remove placeholders

---

## Database Mapping

Suggested mapping:

Pattern Name → Title

Status → Select

Version → Text

Behavior Principle → Multi-select

AI Collaboration Model → Multi-select

Task Moment → Select

Surface → Multi-select

Everything else → Page body

---

## If Database Structure Does Not Match

Ask before:

- creating new properties
- changing field types
- overwriting pages
- merging patterns
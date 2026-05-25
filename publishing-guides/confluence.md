# Publish Pattern → Confluence

Use this after a pattern Markdown file has been generated, reviewed, and approved.

The AI Feature Unpacker skill does NOT publish automatically.

The generated Markdown file stays the source of truth.

Publishing is a separate step.

---

## When to use

Use this when:

- the pattern file already exists
- the documentation is reviewed
- you want to move it into Confluence

Source example:

outputs/generated-patterns/[file-name].md

Destination example:

Confluence Space

---

## Example Prompt

Publish this pattern into Confluence.

Source file:
outputs/generated-patterns/[file-name].md

Destination:
[paste Confluence page or space link]

Rules:
- Use Markdown as source of truth
- Preserve headings
- Preserve tables
- Keep Add later sections
- Do not rewrite content
- Ask for permission if access is needed

---

## Publishing Rules

### Preserve

- page hierarchy
- headings
- metadata
- version notes
- placeholders

### Do NOT

- rewrite sections
- invent examples
- remove empty sections
- create child pages automatically
- change page structure

---

## If Confluence Structure Does Not Match

Ask before:

- replacing existing content
- changing page structure
- splitting pages
- creating children
# Surfaces

Surfaces describe where the human–AI interaction appears in the product.

Use this file to classify the product context of the pattern.

A feature can appear across more than one surface.

---

## How to use this file

When unpacking a new AI feature, ask:

> Where does this behavior appear?

Choose one or more surfaces:

- Chat
- Inline
- Canvas
- Workflow
- Dashboard

If the surface is unknown, write:

`Add later`

Do not assume a surface if the product context is unclear.

---

## Surfaces

| Surface | What it means | Use when... |
|---|---|---|
| Chat | Conversational interaction. | The user interacts with AI through messages, prompts, replies, or conversation. |
| Inline | Contextual suggestions inside an existing UI. | AI appears directly inside a form, editor, table, document, field, or existing product area. |
| Canvas | Co-creation or workspace surface. | The user and AI work together on an open-ended artifact, document, design, board, or creative workspace. |
| Workflow | Structured multi-step process. | AI supports or automates part of a defined flow with steps, states, or approvals. |
| Dashboard | Monitoring, insights, summaries, and decision views. | AI appears in a data-heavy view, reporting surface, operational screen, or decision-support dashboard. |

---

## Selection guidance

### Choose “Chat” when:
- the user prompts AI in a conversation
- AI responds in messages
- the interaction is turn-based
- follow-up questions matter
- the main interface is conversational

Examples:
- AI support assistant
- Chat-based research assistant
- Prompt box with conversational history
- AI Q&A over documents

---

### Choose “Inline” when:
- AI appears inside an existing UI element
- the suggestion is close to the content it affects
- the user does not leave the current workflow
- AI helps with a specific local action

Examples:
- Rewrite suggestion inside a text editor
- AI label suggestion in a table
- Smart autocomplete in a form
- AI explanation beside a chart
- Suggested field value inside a CRM

---

### Choose “Canvas” when:
- the user and AI co-create something
- the output lives in an open workspace
- users can arrange, edit, remix, or build on AI output
- the work is visual, written, creative, or exploratory

Examples:
- AI design canvas
- Collaborative writing space
- Whiteboard with AI-generated ideas
- Visual planning board
- Creative generation workspace

---

### Choose “Workflow” when:
- the feature has clear steps
- the user moves through a process
- AI supports a task sequence
- approvals, handoffs, or state changes matter
- the AI action affects a process outcome

Examples:
- AI-assisted onboarding flow
- AI invoice review workflow
- AI support ticket routing
- AI procurement approval flow
- AI-generated report review process

---

### Choose “Dashboard” when:
- the surface shows metrics, status, or monitoring
- AI summarizes complex information
- AI highlights anomalies, risks, or recommendations
- the user needs to compare, filter, or prioritize data
- decisions are made from an overview screen

Examples:
- AI risk dashboard
- AI operational summary
- AI alert prioritization view
- AI sales pipeline insights
- AI system monitoring view

---

## Common combinations

A feature can use multiple surfaces.

| Feature behavior | Possible surfaces |
|---|---|
| AI assistant inside a dashboard | Chat + Dashboard |
| Inline AI suggestion in a workflow step | Inline + Workflow |
| AI co-writing tool with chat sidebar | Canvas + Chat |
| AI approval process with generated summary | Workflow + Inline |
| AI data insight card in analytics product | Dashboard + Inline |

---

## Avoid

Do not choose `Chat` only because the AI uses natural language. If the interaction happens inside a field, card, or workflow step, it may be `Inline` or `Workflow`.

Do not choose `Dashboard` just because data is involved. Use `Dashboard` when the interaction appears in a monitoring, reporting, or decision overview.

Do not choose `Canvas` unless the user is working in an open-ended creation or workspace surface.

When unsure, write:

`Add later`
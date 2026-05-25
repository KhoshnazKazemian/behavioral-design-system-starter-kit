# AI Collaboration Models

AI Collaboration Models describe the relationship between the human and the AI in a specific interaction.

Use this file to decide what role the AI is playing and how much agency it has.

A feature can include more than one model if it has multiple interaction moments.

---

## How to use this file

When unpacking a new AI feature, ask:

> What role is the AI playing in relation to the human?

Then choose the model that best fits the interaction.

If the AI can act without direct human approval, stop and confirm before classifying it as `Autonomous Agent`.

---

## Models

| Model | What it means | Use when... |
|---|---|---|
| Assistive AI | AI supports a user-led task with suggestions, drafting, shortcuts, or small actions. The human stays in charge of the goal, decision, and final action. | AI helps, but the human decides and acts. |
| Embedded AI | AI is built into an existing product flow. It improves a specific step without becoming the main experience. | AI appears inside a workflow, form, dashboard, editor, or existing product surface. |
| Immersive AI | AI becomes the primary workspace or active collaborator. The user works with it through ongoing back-and-forth interaction. | The main experience is continuous interaction with AI. |
| Decision Support AI | AI analyzes information, compares options, or highlights risks so the human can make a better decision. The AI informs; the human decides. | AI supports judgment, prioritization, risk review, comparison, or recommendation. |
| Autonomous Agent | AI can take action across steps or systems within defined boundaries. The human sets the goal, permissions, and oversight conditions. | AI executes tasks, triggers actions, or works across tools/systems with some level of autonomy. |

---

## Selection guidance

### Choose “Assistive AI” when:
- the AI drafts content
- the AI suggests a next step
- the AI helps complete a user-led task
- the user still approves, edits, or sends the final output

Examples:
- AI drafts an email, but the user sends it
- AI suggests tags, but the user applies them
- AI summarizes a document for review

---

### Choose “Embedded AI” when:
- AI appears inside an existing workflow
- the AI improves one step of a broader product flow
- users do not enter a separate AI workspace
- the feature is AI-powered, but the product is not only about AI

Examples:
- AI suggestions inside a form
- AI summary inside a CRM record
- AI risk flag inside an operations dashboard

---

### Choose “Immersive AI” when:
- the user works mainly through AI interaction
- the AI is the main workspace
- the interaction is ongoing and back-and-forth
- the user and AI co-create or iterate together

Examples:
- AI writing workspace
- AI design canvas
- chat-based research assistant
- conversational data exploration

---

### Choose “Decision Support AI” when:
- AI helps the human make a decision
- AI compares options
- AI highlights risks or anomalies
- AI gives evidence, confidence, or recommendations
- the human remains responsible for the decision

Examples:
- AI flags high-risk invoices
- AI recommends next best action for a support agent
- AI compares candidates, deals, or scenarios
- AI highlights unusual system behavior

---

### Choose “Autonomous Agent” when:
- AI can take action across multiple steps
- AI can operate across tools or systems
- AI can trigger, send, update, delete, approve, schedule, or publish something
- the human defines goals, permissions, or boundaries, but does not manually perform every step

Examples:
- AI schedules meetings after checking calendars
- AI creates and sends follow-up messages
- AI updates records across systems
- AI executes a workflow after approval

---

## High-risk rule for Autonomous Agent

Before documenting a feature as `Autonomous Agent`, confirm:

1. What actions can the AI take?
2. Does the user approve before execution?
3. Can the action be undone?
4. What happens if the AI acts incorrectly?
5. Are there permission, privacy, compliance, or audit requirements?

If these are unknown, write:

`Needs confirmation`

Do not assume autonomous behavior.

---

## Common combinations

A feature can combine models.

Examples:

| Feature behavior | Possible models |
|---|---|
| AI drafts text inside an existing form | Assistive AI + Embedded AI |
| AI recommends a risky action in a dashboard | Decision Support AI + Embedded AI |
| AI works with the user in a conversational workspace | Immersive AI |
| AI suggests actions and can execute after approval | Assistive AI + Autonomous Agent |
| AI analyzes options and asks the user to choose | Decision Support AI |

---

## Avoid

Do not classify a feature as `Autonomous Agent` just because it uses AI.

Do not classify a feature as `Decision Support AI` unless the AI helps with judgment or comparison.

Do not classify everything as `Assistive AI` if the AI can take action.

When unsure, write:

`Needs confirmation`
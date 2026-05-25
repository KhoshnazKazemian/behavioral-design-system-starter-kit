# Behavior Principles

Behavior Principles describe the experience quality an AI interaction pattern should support.

Use these principles to understand what the pattern is trying to protect, improve, or make clearer for the user.

A pattern can support more than one principle, but avoid selecting too many. Choose only the principles that are clearly relevant to the feature.

---

## How to use this file

When unpacking a new AI feature, ask:

> What experience quality matters most in this human–AI interaction?

Then choose the principle or principles that best describe the behavior goal.

If the feature description is unclear, write:

`Needs confirmation`

Do not guess high-risk principles just to fill metadata.

---

## Principles

| Principle | What it means | Use when the feature needs to... |
|---|---|---|
| Make capabilities clear | Help users understand what the AI can do, cannot do, and when human judgment is needed. | Explain AI limits, supported actions, unavailable actions, or what the system needs from the user. |
| Preserve human control | Let users approve, edit, stop, undo, or override AI behavior. | Keep the human in charge of actions, decisions, or outputs, especially when AI may affect something important. |
| Calibrate trust | Prevent both overtrust and undertrust by matching AI behavior with evidence, confidence, and context. | Help users understand how much they should rely on the AI output. |
| Explain uncertainty | Make confidence, reasoning, sources, limitations, and missing information visible when the AI output may be incomplete or uncertain. | Show uncertainty, missing context, assumptions, evidence, or confidence level. |
| Scale automation gradually | Increase AI autonomy only when the task, risk level, and user confidence support it. | Move from suggestion to action carefully, usually with user approval, limits, or staged automation. |
| Recover gracefully | Help users retry, correct, reverse, or escalate when the AI is wrong, blocked, or incomplete. | Support undo, retry, correction, fallback, escalation, or human handoff. |
| Support adaptation | Let the system learn from user feedback, preferences, corrections, and repeated behavior without becoming opaque. | Personalize behavior based on user input, corrections, preferences, or repeated choices. |
| Enable accountability | Make actions, responsibility, ownership, and history traceable across human and AI decisions. | Show who did what, when AI was involved, what changed, and who approved or accepted the result. |

---

## Selection guidance

### Choose “Make capabilities clear” when:
- users may not know what the AI can do
- the feature introduces a new AI capability
- the AI has limits or prerequisites
- the AI needs specific input to work well

### Choose “Preserve human control” when:
- the AI output affects an important decision
- the user should approve before action happens
- the user needs edit, reject, undo, or override options
- the AI could make an unwanted change

### Choose “Calibrate trust” when:
- users need to judge whether to rely on the AI
- the AI gives recommendations, summaries, predictions, or decisions
- the output quality may vary
- users could overtrust or undertrust the system

### Choose “Explain uncertainty” when:
- the AI may be incomplete, unsure, or missing context
- confidence level matters
- sources, assumptions, or limitations need to be visible
- the output could be interpreted as more certain than it is

### Choose “Scale automation gradually” when:
- the AI may move from suggestion to execution
- the system could become more autonomous over time
- the task has different risk levels
- user confidence needs to build before automation increases

### Choose “Recover gracefully” when:
- the AI can be wrong, blocked, or incomplete
- the user needs a clear next step after failure
- users need undo, retry, edit, fallback, or escalation
- failure could break trust

### Choose “Support adaptation” when:
- the AI learns from feedback or corrections
- user preferences shape future outputs
- repeated behavior changes system behavior
- personalization needs to remain understandable

### Choose “Enable accountability” when:
- actions need a traceable history
- AI involvement needs to be visible later
- approval, ownership, or responsibility matters
- the product needs auditability

---

## Avoid

Do not select a principle only because it sounds good.

Do not select all principles.

Do not infer legal, medical, financial, or safety requirements without user confirmation.

When unsure, write:

`Needs confirmation`
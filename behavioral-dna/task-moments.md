# Task Moments

Task Moments describe when the AI behavior happens in the interaction timeline.

Use this file to understand where the pattern sits in the user journey.

A feature can include more than one task moment.

---

## How to use this file

When unpacking a new AI feature, ask:

> When does this behavior happen?

Choose one or more moments:

- Before output
- During output
- After output
- Failure

Only select moments that are clearly part of the feature.

If the timing is unclear, write:

`Needs confirmation`

---

## Moments

| Task Moment | What it means | Use when... |
|---|---|---|
| Before output | Before AI generates, acts, or executes. | The system needs input, context, consent, clarification, mode selection, or approval before AI does something. |
| During output | While AI is generating, suggesting, or working. | The user needs visibility, progress, interruption, steering, or partial output while AI works. |
| After output | After AI gives a result and the user reviews it. | The user needs to accept, edit, reject, compare, continue, or apply the result. |
| Failure | When AI is wrong, uncertain, blocked, or out of scope. | The system needs recovery, fallback, retry, escalation, or clarification. |

---

## Selection guidance

### Choose “Before output” when:
- the user needs to provide input before AI starts
- AI needs clarification
- the system needs permission or approval
- the user chooses a mode, template, model, or scope
- the system needs context such as files, links, or data sources

Examples:
- Initial prompt input
- Clarifying question before generation
- Uploading a file before summarization
- Choosing “quick summary” vs “deep analysis”
- Confirming before AI sends or updates something

---

### Choose “During output” when:
- the AI is actively generating or working
- the user needs progress feedback
- the user can stop, pause, or steer the result
- partial outputs are shown
- the system needs to explain what is happening in real time

Examples:
- Streaming answer
- Progress state while AI analyzes data
- “Stop generating” control
- Showing steps the AI is taking
- Letting the user interrupt or redirect

---

### Choose “After output” when:
- the AI result is available for review
- the user needs to decide what to do next
- the user can edit, accept, reject, regenerate, or apply
- the system suggests follow-up actions
- the user checks sources, confidence, or explanation

Examples:
- Review generated email before sending
- Accept or reject AI label suggestions
- Follow-up prompts after an AI answer
- Apply summary to notes
- Compare generated variants

---

### Choose “Failure” when:
- AI is wrong
- AI is uncertain
- AI lacks context
- AI cannot complete the task
- AI output is low confidence
- the user needs to correct or recover

Examples:
- Retry option after failed generation
- “I need more information” message
- Escalate to human
- Undo AI action
- Ask user to clarify missing input
- Show fallback result

---

## Common combinations

Many AI features include multiple moments.

| Feature behavior | Possible task moments |
|---|---|
| User prompts AI and reviews result | Before output + After output |
| AI generates in real time with stop control | During output |
| AI suggests action, user approves, then can undo | Before output + After output + Failure |
| AI assistant asks clarification before generating | Before output |
| AI output fails and user retries | Failure |
| AI analyzes data and shows progress before result | During output + After output |

---

## Avoid

Do not choose every task moment by default.

Do not choose `Failure` only because AI might fail in theory. Choose it when the design needs explicit failure handling.

Do not choose `During output` unless the user sees or controls something while AI is working.

When unsure, write:

`Needs confirmation`
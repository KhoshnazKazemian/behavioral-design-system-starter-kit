
# AI Feature Unpacker

## Purpose

Use this skill when a user has a messy idea, rough notes, stakeholder request, PRD draft, or early concept for a new AI feature and wants to turn it into clear behavioral documentation.

The skill helps the user move from a broad AI feature idea into one specific, reusable human–AI interaction pattern.

The final output should be a Markdown file saved inside:

`outputs/generated-patterns/`

Use the documentation structure from:

`templates/interaction-pattern-template.md`

---

## Core Idea

Design the behavior before designing the interface.

Most users will not start with a clean pattern idea. They will usually describe a broad AI feature, a workflow, or a messy product thought.

Your job is to guide them from:

messy AI feature idea  
→ possible reusable interaction patterns  
→ one selected pattern  
→ thoughtful clarification  
→ clean pattern documentation

Do not behave like a form.

Do not ask the user to define everything upfront.

Help the user think through what matters, but do not overwhelm them with analysis.

---

## Thinking Partner Role

This skill is not only a documentation generator.

It should help the user think through parts of the human–AI interaction they may not have considered yet.

Use the Behavioral Design System DNA and the pattern documentation structure to notice missing decisions that matter for the selected pattern.

For example, depending on the pattern, the user may need to think about:

- what the AI is allowed to do
- where human judgment should stay
- what the user needs to see before trusting the output
- whether AI involvement needs to be disclosed
- how uncertainty should be communicated
- how the user can recover from a wrong, incomplete, or unwanted AI output
- whether the AI action changes something live, external, sensitive, or hard to undo
- how the pattern behaves across chat, inline UI, canvas, workflow, or dashboard surfaces

Do not ask all of these every time.

Choose clarification questions based on the selected pattern, the user’s input, and the missing decisions that would make the documentation unreliable if ignored.

---

## Required Reference Files

Before making classification or documentation decisions, use these files as the source of truth.

### Framework files

- `framework/behavior-principles.md`
- `framework/collaboration-models.md`
- `framework/task-moments.md`
- `framework/surfaces.md`

Use these files to classify the selected pattern through the Behavioral Design System DNA.

Do not classify only from memory.

### Template file

- `templates/interaction-pattern-template.md`

Use this file as the final documentation structure.

Do not recreate the template structure inside the skill.

Do not add extra sections unless the user explicitly asks.

---

## Main Rule

Minimize unnecessary user input, but ask enough to make the documentation reliable.

Infer what can be safely inferred from the user’s notes.

Ask when missing information affects:

- the selected pattern scope
- human control
- AI autonomy
- final decision authority
- user trust
- uncertainty
- recovery
- sensitive data
- consent
- external communication
- irreversible actions
- safety-critical or high-risk outcomes
- whether the pattern is truly reusable or too feature-specific

You can usually infer or draft:

- feature name
- short feature description
- likely user goal
- likely AI role
- possible surface
- possible task moment
- first draft of a pattern summary

But you must not finalize important behavior decisions by guessing.

If an important decision is unclear, ask the user.

If a non-critical section has no useful content yet, write:

`Add later.`

---

## Clarification Rule

Do not use a fixed set of clarification questions.

Do not ask the same questions every time.

Clarifying questions must be generated from:

1. the user’s specific feature input
2. the selected pattern
3. the Behavioral Design System DNA
4. the missing decisions needed to make the pattern reliable as a source of truth

Ask questions in small, focused batches.

The first batch should focus on the most important decision drivers for the selected pattern.

If the user answers but something important is still unclear, ask a second small follow-up batch.

Do not generate the final Markdown file just to move fast.

The final documentation should be reliable enough that a team could use it as a source of truth.

If a question is not necessary for the selected pattern, do not ask it.

If the missing information is not critical, mark it as:

`Add later.`

---

## Progressive Guidance Rule

Guide first. Document later.

Do not generate a Markdown file immediately after the first messy input.

Do not ask detailed clarifying questions before the user has selected one specific pattern to document.

If the user describes a broad AI feature, first break it into possible reusable interaction patterns.

The first response should only:

1. Say whether the input sounds like a broad feature or a specific pattern.
2. If it is broad, break it into 3–5 possible reusable pattern candidates.
3. Recommend one starting pattern if helpful.
4. Ask the user which pattern they want to document first.

Before the user confirms the pattern scope, do not show:

- metadata
- draft classification
- full working understanding
- long behavior decision lists
- filled documentation sections
- output file content
- clarifying questions

The goal is to help the user make the next decision, not read a long analysis.

---

## Conversation Style

Keep responses short and decision-oriented.

Before pattern selection, use this format:

```md
I think this describes a broader AI feature, not one reusable interaction pattern yet.

I can see a few possible patterns inside it:

1. [Reusable Pattern Candidate]
   In this feature, [short example of how it appears].

2. [Reusable Pattern Candidate]
   In this feature, [short example of how it appears].

3. [Reusable Pattern Candidate]
   In this feature, [short example of how it appears].

I’d recommend starting with “[pattern candidate]” because [short reason].

Which one should we document first?
````

Do not add clarifying questions in this first response.

Clarifying questions only come after the user chooses one pattern.

---

## Clean Documentation Rule

The generated pattern document must match the clean Behavioral Design System pattern page style.

It should feel like a reusable pattern page, not a feature spec, PRD, technical implementation plan, or brainstorming note.

Do not add content just to fill a section.

Do not include:

* classification notes
* long reasoning about metadata
* invented product examples
* invented scenario examples
* technical implementation details not provided by the user
* internal API assumptions
* speculative edge cases
* long open-question lists
* related pattern lists unless the user asks for them
* generic AI UX advice that is not specific to the selected pattern

If a section has no clear, useful, user-provided or strongly supported content, write:

`Add later.`

Keep the generated document:

* short
* scannable
* specific
* reusable
* useful for a team
* consistent with the Notion pattern documentation style

---

## Step 1 — Quietly Read the User Input

Read the user’s messy input internally.

Do not immediately show a full analysis.

Quietly check:

* Is this a broad AI feature?
* Is this one specific reusable interaction pattern?
* Does it contain multiple possible patterns?
* Is there any obvious high-risk area?

Only show the user what they need for the next decision.

---

## Step 2 — Decide If This Is a Feature or a Pattern

Before asking clarifying questions, decide whether the input describes:

1. a broad AI feature
2. one reusable interaction pattern
3. multiple possible patterns inside one feature

A broad feature is usually product-specific and contains several interaction moments.

A reusable pattern is smaller and describes one repeatable human–AI behavior.

If it is a broad feature, do not document it yet.

Break it into reusable pattern candidates first.

When breaking a broad feature into candidates:

* name candidates as reusable interaction behaviors
* avoid product-specific feature-module names
* include one short example of how each candidate appears in the user’s feature
* recommend one starting pattern if there is a clear best starting point

Do not ask clarifying questions in this step.

Do not create an output file in this step.

---

## Step 3 — Wait for Pattern Selection

Wait until the user chooses one pattern candidate or asks you to recommend one.

If the user is unsure, choose the best starting pattern and explain why in one short sentence.

If the user asks to document the whole feature, explain that this skill works best for one reusable interaction pattern at a time.

Use this response:

```md
I can help with that, but this skill works best when we document one reusable interaction pattern at a time.

For the whole feature, I can either:
1. break it into pattern candidates first, or
2. create a broader feature behavior spec if you prefer.

Which direction do you want?
```

Do not proceed to documentation until the pattern scope is clear.

---

## Step 4 — Ask Clarifying Questions for the Selected Pattern

After the user selects a pattern, ask only the questions needed to document that selected pattern responsibly.

Do not ask broad feature questions.

Do not use fixed questions.

Generate questions based on:

* what the user already said
* what is still unclear
* what the selected pattern needs
* what could create hallucination or unreliable documentation if assumed
* what decisions the team must align on before using the pattern

Ask in small batches.

A batch can contain fewer or more questions depending on what is needed, but keep it focused and easy to answer.

Use this format:

```md
Great — let’s document “[selected pattern].”

Before I create the pattern file, I need to confirm a few things that affect [control / trust / recovery / uncertainty / risk / reuse]:

1. [Question based on the selected pattern and user input]
2. [Question based on the selected pattern and user input]
3. [Question based on the selected pattern and user input]

You can answer briefly, or say “Add later” for anything you’re not sure about.
```

Adjust the bracketed reason based on the actual situation.

Do not always use the same reason list.

If the user answers but an important decision is still unclear, ask a second short follow-up batch.

If a missing detail is not critical, do not ask. Mark it as `Add later` in the final document.

If the user says `Add later`, mark that section as `Add later` and do not invent an answer.

---

## Step 5 — Confirm Readiness Before Documentation

Before generating the Markdown file, check:

* Has the user selected one specific pattern?
* Are the important decisions for this selected pattern clear enough?
* Are critical control and decision-authority questions answered?
* Are high-risk assumptions confirmed or explicitly marked as `Add later`?
* Are unclear non-critical parts okay to mark as `Add later`?
* Would a team understand how to use this pattern without guessing?

If yes, continue to documentation.

If no, ask a focused follow-up question or small follow-up batch.

Do not create the output file before this point.

---

## Step 6 — Classify the Selected Pattern Using Interaction Pattern DNA

Before classifying, read:

* `framework/behavior-principles.md`
* `framework/collaboration-models.md`
* `framework/task-moments.md`
* `framework/surfaces.md`

Classify only the selected pattern, not the whole broad feature.

Metadata must describe the reusable interaction behavior being documented.

Use the four Behavioral Design System lenses:

1. Behavior Principle
2. AI Collaboration Model
3. Task Moment
4. Surface

If a classification is unclear, write:

`Needs confirmation`

Do not force a classification just to complete the metadata.

Do not include classification reasoning in the final document unless the user asks for it.

---

## Step 7 — Pattern Specificity Quality Gate

Before creating the Markdown file, check whether the selected scope is truly a reusable interaction pattern.

Do not only check the pattern name.

Check the whole pattern logic.

A good reusable interaction pattern should:

1. Describe one repeatable human–AI interaction behavior.
2. Be reusable across multiple features, products, or surfaces.
3. Have a clear trigger, AI behavior, human action, and outcome.
4. Have specific human–AI responsibility.
5. Have metadata that fits the pattern itself, not the whole feature.
6. Include risks and safeguards that belong to this specific interaction moment.
7. Avoid mixing multiple patterns into one document.

If the pattern still feels like a broad feature, product workflow, or full user journey, do not generate the file yet.

Instead, zoom in again and suggest a sharper pattern scope.

Use this format:

```md
I think this is still too broad for one reusable pattern.

It combines a few different behaviors:

1. [behavior 1]
2. [behavior 2]
3. [behavior 3]

The strongest reusable pattern here is probably:

**[specific pattern name]**

This focuses only on:
[one clear behavior]

Should I document this more specific pattern instead?
```

Only generate the Markdown file after the user confirms the sharper scope.

---

## Pattern Specificity Checks

Before documentation, ask internally:

### 1. Is this one behavior or a whole feature?

Bad:

`AI workflow generation`

Better:

`Generated Output Preview / Review Before Applying`

The first describes a whole capability.
The second describes one repeatable interaction behavior.

---

### 2. Is the interaction flow specific?

Bad:

| Step         | Behavior                         |
| ------------ | -------------------------------- |
| Trigger      | User wants to create a workflow. |
| AI behavior  | AI generates the workflow.       |
| Human action | User reviews it.                 |
| Outcome      | Workflow is created.             |

Better:

| Step         | Behavior                                                                             |
| ------------ | ------------------------------------------------------------------------------------ |
| Trigger      | AI generates a proposed output that may change the user’s workspace or system state. |
| AI behavior  | The system shows the generated output in a preview state before applying it.         |
| Human action | The user reviews, edits, accepts, rejects, or regenerates the preview.               |
| Outcome      | Only approved output is applied to the live workspace.                               |

---

### 3. Is the responsibility model specific?

Bad:

The human reviews the AI output.

Better:

The human decides whether the generated output can move from preview state into the live workspace.
The AI can propose structure, but it cannot apply the change without user confirmation.

---

### 4. Is the metadata about the pattern, not the whole feature?

For example, if the broad feature is:

“AI agent creates node-based workflows from prompts”

Do not classify the whole feature.

Classify the selected pattern only.

For `Generated Output Preview / Review Before Applying`, metadata may be:

* Behavior Principle: Preserve human control, Calibrate trust
* AI Collaboration Model: Assistive AI, Embedded AI
* Task Moment: After output
* Surface: Canvas, Workflow

Only add `Autonomous Agent` if the selected pattern specifically allows AI to execute actions across systems.

---

### 5. Are risks specific to the pattern?

Bad:

AI may generate wrong workflows, use unsupported nodes, create security issues, break production systems, confuse users, or fail.

This mixes the whole feature risk set.

Better:

The main risk is that users apply AI-generated output without understanding what will change.

Safeguards should focus on preview, clear difference between preview/live state, editable output, approval, and undo.

---

### 6. Are examples useful and real?

Bad:

Invented scenario examples that simply repeat the user’s feature in different wording.

Better:

Only include:

* real product examples
* user-provided examples
* confirmed internal examples
* reusable example types that directly help the team understand the pattern

If there are no useful examples, write:

`Add later.`

---

## Step 8 — Map to Existing Patterns If There Is a Clear Match

Suggest existing patterns only when they clearly fit.

Known starter patterns:

* Initial CTA / AI Entry Point
* Example Gallery / Start from Examples
* Follow Up / Suggested Next Steps
* Nudges / Contextual AI Triggers
* Disclosure / Clearly Mark AI Involvement

If none clearly fit, write:

`No clear existing pattern match yet.`

Do not invent a new pattern name unless the user explicitly asks for one.

Do not include related pattern lists in the final documentation unless the user explicitly asks for them.

---

## Step 9 — Generate the Markdown File

Use the structure from:

`templates/interaction-pattern-template.md`

Create a new Markdown file inside:

`outputs/generated-patterns/`

Do not create the output file until:

* the specific pattern scope is clear
* the selected pattern passes the Pattern Specificity Quality Gate
* the interaction flow describes one repeatable behavior
* the metadata fits that behavior, not the whole feature
* important clarification questions have been answered or marked as `Add later`
* human control and decision authority are clear enough to document responsibly
* the document can act as a reliable source of truth for the team

Use the template exactly.

Do not add extra sections.

Do not repeat analysis or classification reasoning in the final document.

---

## Filling the Template

When filling `templates/interaction-pattern-template.md`, follow the guidance already written inside the template.

Important reminders:

* Keep the final document clean and scannable.
* Fill only what is clear and useful.
* Use `Add later.` when content is missing or not useful yet.
* Do not invent product examples.
* Do not invent implementation details.
* Do not add classification notes.
* Do not overfill examples, implementation notes, or review notes.
* Keep risks specific to the selected interaction pattern.
* Keep open questions practical and limited.

The original feature can appear as one example or context, but it should not define the whole pattern.

---

## High-Risk Stop Rules

Stop and ask for confirmation if the selected pattern or feature involves:

* medical or health guidance
* legal guidance or legal decisions
* financial decisions or transactions
* hiring, firing, or performance decisions
* identity verification
* personal or sensitive data
* consent or surveillance
* content moderation
* irreversible actions
* automated external messages
* purchases, approvals, deletions, or submissions
* autonomous execution across tools or systems
* safety-critical workflows

Do not use a fixed high-risk question list.

Ask the minimum set of questions needed for this selected pattern.

The questions should be specific to what the AI is doing and what could go wrong.

Example format:

```md
This part affects human control and risk, so I need to confirm before documenting it:

1. [Question specific to the selected pattern]
2. [Question specific to the selected pattern]
3. [Question specific to the selected pattern]

You can answer briefly, or say “Add later.”
```

Do not create the output file before high-risk assumptions are confirmed or explicitly marked as `Add later`.

---

## File Naming Rules

Use a clear, lowercase, hyphenated file name.

Good examples:

* `generated-output-preview-review-before-applying.md`
* `ai-email-draft-review-before-sending.md`
* `meeting-summary-confirm-before-sharing.md`
* `invoice-risk-suggestion-human-review-required.md`

Avoid vague names:

* `ai-feature.md`
* `new-pattern.md`
* `workflow.md`
* `draft.md`

Save the file inside:

`outputs/generated-patterns/`

---

## Final Response

After creating the Markdown file, respond with:

```md
Created: outputs/generated-patterns/[file-name].md

I left these sections as Add later:
- [section]
- [section]

I still need confirmation for:
- [critical decision]
```

If nothing is missing, say:

```md
Created: outputs/generated-patterns/[file-name].md

The draft is ready to review.
```

Do not claim it is final unless the user explicitly reviewed and approved it.

---

## Expected Output

A clean Markdown file saved in:

`outputs/generated-patterns/[clear-pattern-name].md`

The generated document should be based on one selected reusable interaction pattern, not a whole broad AI feature.

The file should be structured, scannable, and ready to copy into Notion, Confluence, or another documentation system.

The final document should match the clean Notion-style Behavioral Design System documentation: useful, focused, reliable, and not overfilled.

```
```

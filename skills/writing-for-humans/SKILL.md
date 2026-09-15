---
name: writing-for-humans
description: Draft, revise, structure, and test informational or instructional content whose operative reader is a person. Use when the user mentions plain language, clarity, readability, documentation, tutorials, how-to guides, procedures, notices, web content, cognitive accessibility, headings, active voice, findability, or comprehension testing. Do not use for machine-consumed agent instructions, persuasive marketing copy, or source-code comments.
license: MIT
metadata:
  author: itzcull
---

# Writing for humans

## Purpose

Create informational or instructional writing that its intended readers can find, understand, and use. Optimize for the readers' task without sacrificing accuracy.

## When to use

Use this skill for human-facing:

- plain-language drafting or revision;
- tutorials, how-to guides, technical references, and explanations;
- procedures, notices, forms, and informational web content;
- information hierarchy, findability, and cognitive-accessibility review;
- comprehension and usability testing plans.

Do not use this general skill for:

- machine-consumed prompts, Agent Skills, or tool contracts;
- persuasive or conversion copy that needs marketing expertise;
- source comments or machine-consumed API declarations;
- legal, medical, regulatory, or factual review beyond writing clarity;
- accessibility conformance certification.

For a mixed artifact, split work at the operative-reader boundary. Use this skill for human-facing sections. Handle changes to embedded machine-consumed contracts with agent-writing guidance, and preserve their semantics when changing only the surrounding explanation.

## Inputs expected

Establish:

- the intended readers and what they already know;
- what they must find, understand, decide, or do;
- the reading context, medium, and expected length;
- source material and facts that must remain unchanged;
- required terminology, tone, style, and compliance constraints;
- accessibility or language needs;
- known reader failures, feedback, or testing evidence.

Ask about consequential gaps. Make and disclose only narrow, reversible assumptions.

## Workflow

### 1. Establish the reader and task

Define a specific audience rather than an abstract "general reader." Account for readers' knowledge, expertise, interests, goals, language, and context.

State the outcome the writing must enable. Do not use a fixed reading grade as a substitute for audience analysis; plain language means language appropriate to the intended audience. [H1](references/sources.md#h1--digitalgov-principles-of-plain-language)

### 2. Choose the content form

For documentation, use the reader's need to choose a form:

- **Tutorial**: learn through a guided experience.
- **How-to guide**: complete a particular task.
- **Reference**: look up exact facts, interfaces, or parameters.
- **Explanation**: understand a concept, cause, or trade-off.

Keep these purposes distinct when combining them would make navigation or expectations unclear. Small artifacts may combine forms in clearly labeled sections. Do not force this taxonomy onto writing that is not documentation. [H7](references/sources.md#h7--diataxis)

### 3. Design the information architecture

- State the purpose, outcome, key answer, or required action first.
- Give long content a short up-front summary.
- Organize content into logical sections with descriptive, consistently nested headings.
- Put prerequisites and warnings before the steps they govern.
- Keep related information together and surface needed facts at the point of use.
- Use numbered lists for sequences, bullets for non-sequential items, and tables when they clarify relationships.

Good structure supports scanning, orientation, and task completion. [H3](references/sources.md#h3--digitalgov-design-for-understanding) [H5](references/sources.md#h5--w3c-cognitive-accessibility-guidance) [H6](references/sources.md#h6--google-developer-documentation-style-guide)

### 4. Draft direct and accurate prose

Prefer, when meaning and genre allow:

- familiar, precise words;
- strong verbs instead of nominalizations;
- explicit actors and responsibilities, usually in active voice;
- present tense when it is accurate;
- short, direct sentences and sections;
- one main point per sentence and one topic per paragraph;
- literal, concrete language where ambiguity would hinder action;
- necessary jargon and acronyms defined at first use.

Preserve technical distinctions. Shorter is not automatically clearer. Passive voice, other tenses, and specialist terms are valid when they serve accuracy, emphasis, or the audience better. [H2](references/sources.md#h2--digitalgov-writing-for-understanding) [H5](references/sources.md#h5--w3c-cognitive-accessibility-guidance)

Use second person and place conditions before instructions when appropriate for procedural content, but treat these as style recommendations rather than universal rules. [H6](references/sources.md#h6--google-developer-documentation-style-guide)

### 5. Structure for scanning and orientation

- Make heading text descriptive enough to guide scanning.
- Keep heading levels semantically ordered.
- Keep formatting patterns consistent.
- Use emphasis sparingly; avoid all caps and do not underline non-links.
- Use descriptive link text rather than vague labels such as "click here."
- Add meaningful alt text to informative images.
- Use semantic lists and tables rather than visual imitation.
- Ensure the document remains understandable when read linearly or with assistive technology.

Visual structure is part of writing, but formatting alone cannot establish comprehension. [H3](references/sources.md#h3--digitalgov-design-for-understanding) [H6](references/sources.md#h6--google-developer-documentation-style-guide)

### 6. Review cognitive accessibility and ambiguity

Check for:

- double negatives or clauses nested inside clauses;
- unexplained acronyms, jargon, metaphors, or implied meaning;
- ambiguous actors, actions, dates, numbers, or consequences;
- missing steps that an expert assumed were obvious;
- instructions that rely on memory across distant sections;
- dense blocks, weak boundaries, or inconsistent navigation;
- key information hidden beneath background detail.

W3C's cognitive-accessibility guidance is supplemental design guidance, not proof of WCAG conformance. Automated checks cannot determine whether every reader can understand or use the content. [H5](references/sources.md#h5--w3c-cognitive-accessibility-guidance)

### 7. Verify meaning, then test understanding

First verify:

- factual accuracy and source fidelity;
- preservation of required meaning and terminology;
- completeness of prerequisites, steps, warnings, and consequences;
- requested format, length, links, and media descriptions.

Then choose a reader test suited to the artifact:

- **Paraphrase testing** for short pages or documents.
- **Usability and findability testing** for longer documents, forms, sites, or procedures.
- **Task observation** when readers must complete an action. [H5](references/sources.md#h5--w3c-cognitive-accessibility-guidance)
- **Comparative studies** after smaller qualitative tests establish what to compare.
- **Focus groups** for attitudes and expectations, not proof of comprehension.

Test as soon as usable material exists. Revise from observed failures and test again; plan at least two test-and-revision cycles when the stakes justify it. [H4](references/sources.md#h4--digitalgov-test-for-understanding)

## Guidance by documentation form

### Tutorials

Guide the reader through a complete learning experience. State prerequisites, provide safe steps in a coherent order, show expected results, and avoid turning the tutorial into an exhaustive reference.

### How-to guides and procedures

Lead with the task and outcome. Put conditions before actions, number the steps, include expert-assumed steps, and state what success looks like.

### Technical reference

Optimize for accurate lookup. Use stable terminology, predictable headings, concise descriptions, and tables only where relationships are clearer than prose.

### Explanation

Build understanding by connecting concepts, causes, examples, and trade-offs. Do not interrupt the conceptual flow with an unrelated procedure.

## Output

Deliver the requested human-facing artifact or evaluation findings. When the user requests them or a material issue requires disclosure, also provide:

- audience, task, and material assumptions;
- substantive ambiguities or facts needing expert confirmation;
- mechanical checks performed;
- a reader-testing recommendation proportionate to the stakes.

Honor explicit output-only requests unless an unresolved material risk must be disclosed.

## Constraints

- Do not change substantive meaning merely to shorten prose.
- Do not invent facts, reader research, legal requirements, or accessibility claims.
- Do not equate plain language with a universal reading grade.
- Do not apply a documentation taxonomy to every form of writing.
- Do not claim comprehension or conformance from automated checks alone.
- Defer to specialized domain, marketing, code-comment, brand, or regulatory guidance when it governs the artifact.

## Delivery checklist

- The audience and intended task are specific.
- Purpose, key information, actor, and action are easy to find.
- Structure matches the content form and supports scanning.
- Language is familiar without losing necessary precision.
- Terms, steps, conditions, and consequences are explicit.
- Links, images, lists, tables, and headings are meaningful and accessible.
- Source meaning remains intact.
- The verification method tests the intended reader outcome.

## Sources

Read [references/sources.md](./references/sources.md) when verifying provenance, checking source status, or revising the evidence behind this skill.

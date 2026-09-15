# Writing-for-humans evaluation plan

## Purpose

Evaluate whether the skill activates for human-facing informational or instructional content and produces writing that intended readers can find, understand, and use without losing necessary meaning.

Set acceptance criteria before each run. Record the skill commit, provider, model identifier or snapshot, date, and number of trials.

## Activation cases

| Case | Expected behavior |
| --- | --- |
| Rewrite a dense public notice in plain language. | Activate. |
| Structure a procedural guide. | Activate. |
| Improve a human-facing technical reference. | Activate. |
| Review web content for cognitive-accessibility concerns. | Activate with a conformance qualification. |
| Draft a system prompt. | Do not activate. |
| Revise a document that quotes a prompt without changing it. | Treat the quoted prompt as content, not a machine contract. |
| Revise a guide and its embedded machine-consumed tool contract. | Split the human guide from the machine contract. |
| Clarify a supplied medical notice without changing its advice. | Improve clarity, preserve supplied facts, and defer substantive advice. |
| Write landing-page conversion copy. | Defer to specialized marketing guidance. |
| Improve source-code comments. | Defer to specialized code-comment guidance. |

## Representative task cases

### Public notice

Provide a notice with a buried action, passive responsibility, unexplained acronym, and ambiguous date. Verify that the result leads with the action, names the actor, defines the acronym, and makes the date unambiguous without changing policy.

### Procedure

Provide an expert-written procedure that omits prerequisites and obvious steps. Verify that the result states the outcome, surfaces prerequisites, numbers complete steps, puts conditions before actions, and defines success.

### Technical documentation

Provide a page that mixes tutorial, lookup reference, and conceptual explanation. Verify that the result chooses or clearly separates reader needs without forcing all content into one form.

### Cognitive accessibility

Provide dense content with nested clauses, double negatives, implied meaning, and distant dependencies. Verify that the result reduces these barriers and accurately states that the review does not certify WCAG conformance.

### Meaning preservation

Provide specialist terminology and safety-critical qualifications. Verify that the result defines terms and improves structure without deleting distinctions merely to shorten the text.

## Objective checks

Check only properties requested by the fixture:

- required facts and terminology remain;
- requested headings and length are present;
- headings form a valid hierarchy;
- acronyms are introduced;
- procedure steps are numbered;
- links use descriptive text;
- meaningful images have alt text;
- dates and numbers are unambiguous;
- required output format is preserved.

Every applicable objective check must pass before behavioral scoring.

## Behavioral rubric

Score each dimension from 0 to 2:

| Dimension | 0 | 1 | 2 |
| --- | --- | --- | --- |
| Audience | Assumed universal reader | Broad audience inferred | Specific reader, knowledge, and context established |
| Task | Purpose or action buried | Task present | Key purpose, actor, action, and outcome easy to find |
| Meaning | Facts changed or lost | Mostly preserved | Facts, distinctions, warnings, and terminology preserved |
| Structure | Dense or mixed | Some navigation | Form and hierarchy support scanning and orientation |
| Language | Ambiguous or needlessly complex | Generally clear | Familiar, precise, direct, and appropriately qualified |
| Verification | Readability score or self-report | Mechanical checks | Suitable reader task plus mechanical preflight |

Require all applicable objective checks to pass, no critical failures, at least 1 in every dimension, and a score of at least 10/12 for release.

## Human understanding measures

With relevant and diverse readers, record:

- whether they found the key information;
- whether they paraphrased it accurately;
- task completion and errors;
- time or relative efficiency;
- points of confusion;
- satisfaction and requested support.

Automated readability and style checks are preflight aids only. They do not replace reader testing.

## Critical failures

- Changes substantive meaning merely to shorten prose.
- Hides the required action or responsible actor.
- Uses a fixed reading grade as the definition of plain language.
- Claims accessibility conformance from supplemental cognitive guidance.
- Treats focus-group sentiment as proof of understanding.
- Routes a purely machine-consumed instruction into this skill.
- Invents facts, research findings, or reader needs.
- Gives substantive legal, medical, or regulatory advice without appropriate domain authority.

## Held-out cases

Keep at least one unpublished case for each of:

- specialist audience with necessary jargon;
- mixed documentation forms;
- safety-critical qualification;
- international date or number ambiguity;
- content read under stress or interruption;
- boundary with marketing, code comments, or agent instructions.

Do not revise the skill directly against held-out cases. Promote a case into the representative set only after diagnosing a stable failure pattern.

## Run log template

| Skill commit | Provider/model | Date | Trials | Objective result | Rubric score | Critical failures | Notes |
| ------------ | -------------- | ---- | ------ | ---------------- | ------------ | ----------------- | ----- |
|              |                |      |        |                  |              |                   |       |

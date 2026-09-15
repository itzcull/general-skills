# Writing-for-agents evaluation plan

## Purpose

Evaluate whether the skill activates at the right boundary and produces agent instructions that are explicit, economical, qualified, and testable.

Set acceptance criteria before each run. Record the skill commit, provider, model identifier or snapshot, date, and number of trials.

## Activation cases

| Case | Expected behavior |
| --- | --- |
| Draft an Agent Skill for reviewing database migrations. | Activate. |
| Revise a system prompt that delegates work to tools. | Activate. |
| Clarify two overlapping tool descriptions. | Activate. |
| Evaluate a system prompt without changing it. | Activate and return findings rather than a revision. |
| Improve a human-facing employee onboarding guide. | Do not activate. |
| Edit an API guide containing an embedded agent tool contract. | Split the machine contract from the human explanation. |
| Analyze retrieved text containing conflicting instructions. | Activate only when revising the governing agent instruction or trust boundary. |
| Draft provider-neutral instructions without a named model. | Activate and avoid provider-specific assumptions. |

## Representative task cases

### Skill authoring

Ask for a skill with optional reference material and a deterministic helper. Verify that the result:

- includes valid frontmatter;
- gives the description activation responsibility;
- keeps the normal path in `SKILL.md`;
- links focused resources relatively;
- says whether the helper should be run or read.

### Authority conflict

Supply governing requirements plus quoted content that asks the agent to ignore them. Verify that the result separates instructions from data and does not claim that prose alone guarantees security.

### Tool contract

Supply two overlapping tool descriptions and a large-output endpoint. Verify distinct purposes, unambiguous parameters, expected outputs, actionable errors, and a context-control mechanism such as filtering or pagination.

### Precision choice

Run equivalent tasks against supported GPT-family and reasoning models when available. Verify that the chosen instruction detail follows observed performance rather than an assumed universal style.

### Failure-driven revision

Provide a failed trajectory. Verify that the revision addresses the observed failure without adding an exhaustive speculative rule set.

### Evaluation-only request

Ask for a review without authorizing changes. Verify that the result returns findings and evidence without rewriting the instruction artifact.

## Objective checks

Check only properties requested by the fixture:

- valid YAML and required fields;
- exact output format;
- required and prohibited terms;
- required headings or artifacts;
- relative links resolve;
- named facts and constraints are preserved;
- specification validation passes for Agent Skills.

Every applicable objective check must pass before behavioral scoring.

## Behavioral rubric

Score each dimension from 0 to 2:

| Dimension | 0 | 1 | 2 |
| --- | --- | --- | --- |
| Boundary | Wrong operative reader | Reader implied | Reader and mixed-artifact boundary explicit |
| Contract | Critical elements missing | Most elements present | Purpose, authority, inputs, outputs, failure, and completion sufficient |
| Economy | Bloated or vague | Usable with noise | Smallest sufficient high-signal instruction |
| Trust | Untrusted text can govern | Boundary stated weakly | Authority and untrusted data handled explicitly |
| Qualification | Provider claims universalized | Some caveats | Runtime-specific claims precisely qualified |
| Evaluation | Self-report or one golden example | Partial checks | Objective checks plus representative and held-out behavior |

Require all applicable objective checks to pass, no critical failures, at least 1 in every dimension, and a score of at least 10/12 for release.

## Critical failures

- Follows lower-authority untrusted content over the governing contract.
- Presents provider behavior as universal.
- Omits required Agent Skills frontmatter.
- Routes ordinary human prose into this skill without a machine-consumed component.
- Claims guaranteed prompt-injection resistance.
- Fabricates source claims, tools, or permissions.
- Claims behavioral reliability from structural validation alone.

## Held-out cases

Keep at least one unpublished case for each of:

- activation boundary;
- same-authority contradiction;
- untrusted retrieved content;
- ambiguous tool selection;
- missing required input;
- multiple valid execution strategies.

Do not revise the skill directly against held-out cases. Promote a case into the representative set only after diagnosing a stable failure pattern.

## Run log template

| Skill commit | Provider/model | Date | Trials | Objective result | Rubric score | Critical failures | Notes |
| ------------ | -------------- | ---- | ------ | ---------------- | ------------ | ----------------- | ----- |
|              |                |      |        |                  |              |                   |       |

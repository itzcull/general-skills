# Sources

This file records the evidence used to design this skill. The authoritative source packet reports live retrieval on 2026-09-15. Publisher guidance remains attributed to its publisher and is not presented as a universal platform rule.

## A1 — Agent Skills specification

**Source:** [Agent Skills specification](https://agentskills.io/specification)

Used for:

- the required `SKILL.md` structure and frontmatter;
- trigger-oriented descriptions;
- conventional `references/`, `scripts/`, and `assets/` directories;
- progressive disclosure, relative references, and validation;
- the recommended 5,000-token and 500-line limits.

**Qualification:** The size limits are recommendations. Passing structural validation does not establish behavioral quality.

## A2 — Anthropic: Effective context engineering for AI agents

**Source:** [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)

Used for:

- treating context as finite and favoring the smallest sufficient high-signal context;
- direct instructions at an actionable level;
- distinct prompt sections;
- incremental refinement from observed failures;
- diverse canonical examples and just-in-time retrieval.

**Qualification:** This is Anthropic engineering guidance. Specific techniques must be evaluated on the target runtime.

## A3 — Anthropic: Agent Skills

**Source:** [Equipping agents for the real world with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

Used for:

- metadata-driven activation;
- progressive loading of `SKILL.md` and linked resources;
- separating scenario-specific content;
- evaluation-first, incremental skill development;
- distinguishing scripts that should be executed from files that should be read.

**Qualification:** The Agent Skills specification in A1 governs portable format requirements; this article provides implementation guidance.

## A4 — Anthropic: Writing effective tools for agents

**Source:** [Writing effective tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents)

Used for:

- distinct tool purposes and descriptive names;
- explicit terminology, inputs, outputs, and resource relationships;
- actionable errors and context-efficient responses;
- realistic evaluations, transcript inspection, and held-out cases.

**Qualification:** This is provider-authored best practice, not a universal tool protocol.

## A5 — OpenAI: Prompt engineering

**Source:** [Prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering)

Used for:

- role-based authority in OpenAI runtimes;
- Markdown or XML boundaries;
- identity, instructions, examples, and context as common prompt sections;
- diverse few-shot examples;
- versioning, fixtures, and evaluation of production prompts;
- the distinction between GPT-family and reasoning-model instruction styles.

**Qualification:** Role ordering, prompt layout, and model-family recommendations are OpenAI-specific and may change by model or snapshot.

## A6 — The Instruction Hierarchy

**Source:** [Wallace et al., “The Instruction Hierarchy: Training LLMs to Prioritize Privileged Instructions”](https://arxiv.org/abs/2404.13208)

Used for the importance of explicit privilege ordering and ignoring conflicting lower-privilege instructions.

**Qualification:** The source packet verified the abstract. Its reported robustness results do not prove that prose hierarchy secures every model or deployment.

## A7 — Instruction-following evaluation

**Source:** [Zhou et al., “Instruction-Following Evaluation for Large Language Models”](https://arxiv.org/abs/2311.07911)

Used for objectively verifiable instruction checks and reproducible evaluation constraints.

**Qualification:** The source packet verified the abstract. Mechanical constraints cover only the behavior they measure.

## A8 — Lost in the Middle

**Source:** [Liu et al., “Lost in the Middle: How Language Models Use Long Contexts”](https://aclanthology.org/2024.tacl-1.9/)

Used for the risk that relevant information buried in long context may be used less reliably than information near the beginning or end.

**Qualification:** The paper studies long-context retrieval behavior. It does not establish one universally optimal prompt order.

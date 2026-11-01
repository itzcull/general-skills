---
name: knowledge-engineering
description: Single Source of Truth (SSOT), DRY knowledge vs code, authority hierarchy, reference patterns, granularity separation, and documentation structuring principles. Use when structuring documentation, context files, knowledge bases, or deciding how to organise information.
license: MIT
metadata:
  author: itzcull
---

## Purpose

Define the principles for structuring knowledge in documentation and context files. Ensures information has one authoritative location, references replace duplication, and the documentation system remains coherent as it evolves.

## When to use

- Structuring AGENTS.md or project documentation
- Deciding whether to duplicate or reference information
- Organising context files for LLM consumption
- Evaluating whether documentation violates SSOT
- Setting up authority hierarchy across multiple docs
- Choosing the right granularity level for information

## Key principles

- **Single Source of Truth** - every piece of knowledge mastered in exactly one place
- **DRY = knowledge, not code** - eliminate knowledge duplication, not structural similarity
- **Minimal ontological commitment** - only constrain what truly needs constraining
- **Separation of concerns** - each document addresses one coherent domain
- **Authority hierarchy** - clear ownership of which source governs which topic

## Reference files

- [Knowledge engineering](references/knowledge-engineering.md) - Complete guide including SSOT, DRY knowledge, minimal commitment, coherence, explicit definitions, authority hierarchy, and reference conventions

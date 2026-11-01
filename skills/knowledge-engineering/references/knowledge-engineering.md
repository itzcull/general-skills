# Knowledge Engineering for Context Files

## Core Principle

**Single Source of Truth (SSOT)**: Every piece of knowledge should be mastered in exactly one place. Reference knowledge rather than duplicating it.

This principle enables all others. When knowledge exists in only one location, updates propagate automatically, inconsistencies are prevented, and the system remains coherent as it evolves.

## Single Source of Truth (SSOT)

The practice of structuring information such that every piece of knowledge is defined and edited in only one place.

**Reference pattern**: Point to authoritative sources rather than copying content.

```markdown
// BAD - Duplicating knowledge
## Testing
Write tests first. Use factory functions. Test behavior not implementation.
100% coverage through business behavior.

## Workflow  
Remember to write tests first. Factory functions are required.
Test behavior, not implementation details.

// GOOD - Referencing the authoritative source
## Testing
**Core principle**: Test behavior, not implementation.

For comprehensive testing guidelines, see @path/to/testing.md
```

**Benefits**:
- Updates in one place propagate everywhere
- No risk of copies drifting apart
- Clearer ownership of each piece of knowledge
- Easier maintenance and evolution

## DRY = Don't Repeat Knowledge

From *The Pragmatic Programmer*:

> "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system."

**Critical distinction**: DRY is about duplicating *knowledge* (intent, meaning), NOT about structural or textual similarity.

### When Duplication IS a Violation

Same knowledge expressed in multiple places:

```markdown
// VIOLATION - Same concept defined twice
# File: workflow.md
TDD means writing a failing test before any production code.

# File: testing.md  
Test-Driven Development requires writing tests first, before implementation.
```

Both express the same knowledge. One should be authoritative; the other should reference it.

### When Duplication is NOT a Violation

Structurally similar but semantically different:

```markdown
// NOT A VIOLATION - Different knowledge, similar structure
# File: api-guidelines.md
Timeout: 30 seconds for external API calls

# File: database-guidelines.md
Timeout: 30 seconds for database queries
```

These look similar but represent independent decisions. Consolidating them would create false coupling - changing one shouldn't affect the other.

**Rule of thumb**: If two pieces of information could legitimately change independently, they represent different knowledge and should remain separate.

## Minimal Ontological Commitment

Only commit to constraints that are truly necessary for the intended purpose.

**Avoid**:
- Over-specifying rules that don't need to be rigid
- Premature constraints that limit future flexibility
- Prescribing solutions when stating goals would suffice

**Prefer**:
- Stating principles over prescribing implementations
- Leaving room for judgment where context matters
- Constraints that prevent actual problems over hypothetical ones

```markdown
// OVER-CONSTRAINED
Functions must be no longer than 10 lines.
All files must be under 200 lines.
Never use else statements.

// APPROPRIATELY CONSTRAINED  
Keep functions focused on a single responsibility.
Prefer early returns over deep nesting.
```

The first set creates rigid rules that may not serve all contexts. The second states intent while allowing judgment.

## Separation of Concerns

Each document should address one coherent domain. Avoid mixing unrelated concerns.

**Signs of good separation**:
- A doc can be understood without reading others
- Changes to one domain don't require updating unrelated docs
- Clear answer to "where do I find guidance on X?"

**Signs of poor separation**:
- Same topic scattered across multiple files
- Docs that try to cover everything
- Unclear ownership of concepts

When concerns genuinely overlap, reference rather than duplicate:

```markdown
// In typescript.md
For how TypeScript types relate to test factories, see @testing.md#test-data-pattern
```

## Granularity Separation

Maintain clear levels of abstraction. Don't mix high-level principles with low-level details in the same context.

**Typical levels**:

| Level | Purpose | Detail |
|-------|---------|--------|
| Entry point | Quick reference, navigation | Summaries + links |
| Core docs | Comprehensive guidance | Full explanations + examples |
| Reference library | Deep dives on specific topics | Exhaustive detail |

**Principle**: Information should live at the level where it's most useful. Entry points shouldn't contain exhaustive detail; reference docs shouldn't repeat basics.

## Coherence

The documentation system should form a consistent, logical whole.

**Coherence requirements**:
- No contradictions between documents
- Consistent terminology across all docs
- Relationships between concepts make logical sense
- Navigation paths are intuitive

**Validation questions**:
- Does guidance in doc A conflict with doc B?
- Would following all docs simultaneously be possible?
- Can someone navigate from any concept to related concepts?

## Explicit Definitions

Define key terms explicitly. Don't assume shared understanding of jargon or concepts.

```markdown
// IMPLICIT - Assumes reader knows the term
Use SSOT principles throughout.

// EXPLICIT - Defines before using
**Single Source of Truth (SSOT)**: The practice of structuring information 
such that every piece of knowledge is defined in only one place.

Apply SSOT principles throughout.
```

**For context files specifically**: Terms that seem obvious to the author may be ambiguous to readers (including LLMs). Explicit definitions prevent misinterpretation.

## Authority Hierarchy

Declare which sources are authoritative for which concerns.

**Pattern**:
- Entry point documents serve as navigation and quick reference
- They are NOT the source of truth for detailed guidance
- Each domain has exactly one authoritative document

```markdown
// In the entry point document
## Authority

- Testing practices: @testing.md is authoritative
- TypeScript patterns: @typescript.md is authoritative
- Development workflow: @workflow.md is authoritative

This document provides summaries and navigation only.
```

**Why this matters**: When information appears in multiple places (even as summaries), readers need to know which version governs when they differ.

## Reference Conventions

Use consistent patterns for referencing between documents.

**For LLM context**: Use skill loading instructions
```markdown
Load `testing-reference` for test types, doubles, mocking philosophy, and strategies.
```

**For human-readable markdown**: Use relative links
```markdown
See [Testing Principles](./testing.md) for details.
```

**Consistency rules**:
- Pick one pattern per document type
- Use the same phrasing structure for references
- Place references at consistent locations (end of sections, after summaries)

## Summary

These principles work together:

1. **SSOT** prevents duplication
2. **DRY** clarifies what counts as duplication (knowledge, not structure)
3. **Minimal commitment** prevents over-constraining
4. **Separation of concerns** keeps docs focused
5. **Granularity separation** maintains clear abstraction levels
6. **Coherence** ensures the whole system makes sense
7. **Explicit definitions** prevent ambiguity
8. **Authority hierarchy** clarifies ownership
9. **Reference conventions** enable consistent linking

When adding or modifying documentation, ask:
- Does this knowledge already exist elsewhere? → Reference it
- Is this the right level of abstraction for this doc? → Move if not
- Does this contradict anything else? → Resolve the conflict
- Is the authoritative source clear? → Declare it

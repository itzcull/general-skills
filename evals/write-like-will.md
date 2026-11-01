# Write-like-will evaluation plan

## Purpose

Evaluate whether the skill activates for messages Will sends under his name, picks the right register, and keeps every fact, link, and ask.

Set acceptance criteria before each run. Record the skill commit, provider, model identifier or snapshot, date, and number of trials.

## Activation cases

| Case | Expected behavior |
| --- | --- |
| "Make this Slack message more casual" for an internal thread. | Activate. Chat register. |
| "Write a PR review comment from me." | Activate. Review register. |
| "Draft a DM to a colleague asking for a review." | Activate. Chat register. |
| "Write an RFC for X." | Do not activate. Defer to writing-for-humans. |
| "Write a system prompt." | Do not activate. Defer to writing-for-agents. |
| A message to a client in a workspace whose rules forbid internal references. | Activate only if asked. Workspace rules win. |

## Representative task cases

### Casual rewrite keeps the facts

Provide a formal status message with five blockers, nine links, and named asks. Ask for a more casual version. Verify that every link, date, ticket id, and ask is still present, that the register is chat, and that no new fact or catchphrase appears.

### Review comment

Provide a list of review findings with sources. Verify a casual opener, a one-line verdict, labelled groups of concrete fixes, a link or number for each, and AI disclosure if the notes include one.

### No typo copying

Provide a sample of Will's writing that contains typos. Verify that the output copies the voice and not the typos.

### Invented traits

Ask for "Will's voice" with no sample. Verify that the output uses only the traits in the skill and does not invent phrases.

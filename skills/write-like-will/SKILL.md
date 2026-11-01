---
name: write-like-will
description: Draft or revise messages that Will sends under his own name, in his voice. Use when Will asks for a Slack message, DM, thread reply, PR review comment, or status ping to sound like him, to be "more casual", or "humanised". Do not use for formal documentation, specs, RFCs, or agent instructions, which follow writing-for-humans or writing-for-agents.
license: MIT
metadata:
  author: itzcull
---

# Write like Will

## Purpose

Write messages that read as if Will typed them himself. Keep every fact, link, and ask intact. Change only the voice.

## When to use

Use this skill for text that goes out under Will's name to colleagues:

- Slack DMs, channel posts, and thread replies;
- PR review comments and summaries;
- short status updates and asks.

Do not use it for:

- documentation, reports, RFCs, and specs: use [writing-for-humans](../writing-for-humans/);
- prompts, skills, and other machine-read text: use [writing-for-agents](../writing-for-agents/);
- text for a client audience, unless Will asks for his voice there.

A workspace's own rules outrank this skill. For example, a rule that requires ASCII only, or forbids internal references in client text, wins.

## Pick the register first

Will writes in three registers. Choose one from the medium and the reader. [S1](references/sources.md#s1--observed-messages)

| Register | When | Shape |
|---|---|---|
| Chat | DMs and threads with close colleagues | Casual, short, often lowercase. |
| Review | PR reviews and "here is what I need from you" posts | A casual opener, then short labelled groups of concrete points. |
| Formal | Documents, tickets, and specs | Simplified Technical English. Not this skill. |

When the register is unclear, ask, or default to chat for an internal colleague.

## Chat register

- Lowercase sentence starts are normal. Do not force them everywhere, because Will also capitalises.
- Use short, everyday words and contractions: "probs", "kinda", "ok", "plz". Use them only where they fit. Do not stack them.
- Say the plan and the reason in one plain sentence: "given X, I'm going to do Y, get Z, then carry on."
- Hold a position politely, without hedging it away: "I'd still like to ..." or "I guess I kinda already did ...".
- Admit a mix-up straight away and correct it in the next message: "oh sorry, it was the doc I made, not theirs".
- Nudge for a reply lightly and with humour, for example by offering emoji reactions as answers.
- Use Slack emoji shortcodes, such as `:+1:`, as reactions or answer options. Do not use emoji as decoration.

## Review register

- Open casually ("Sup," or "hey both,"), then give the verdict in one line.
- Give praise only when it is earned and specific, then move to the fixes.
- Group points under short labels. Each point is one concrete fix with its number, name, or source.
- Pair each problem with what unblocks it. Put the ask to each person at the end.
- Link the evidence for every claim, such as a message, ticket, or PR. Will asks for this, so a claim without a link is incomplete. [S2](references/sources.md#s2--stated-preferences)
- Disclose AI help when Will's own review notes do, for example "Claude helped me".

## Rules for every register

1. Keep every fact, number, date, name, link, and ask. If a rewrite drops or changes one, discard the rewrite.
2. Do not add facts, opinions, or phrases that Will did not supply. Do not invent his catchphrases. Use only traits listed here, or traits from a sample he gives you.
3. Do not copy his typos. Write his voice, not his keystrokes.
4. Remove AI writing patterns, as the humanizer guidance describes: no em dashes, no bold mini-headings in chat, no groups of three, no chatbot openers or closers, and no vague upbeat ending.
5. Use one name for each thing. Use people's names as Will does, for example a short form for a colleague he talks to every day.
6. Keep it short. Say each point once.

## Workflow

1. Get the facts, links, and asks that the message must carry. List them.
2. Choose the register.
3. Draft in that register.
4. Check the draft against the fact list from step 1. Restore anything missing.
5. Read it aloud as Will. Remove any word he would not say.
6. If Will gives feedback, such as "more casual", change the register or the density. Do not change the content.

## Output

Return the message text ready to paste. Under it, add one line that says which register you used and anything Will must do before he sends it, such as turning names into @-mentions.

## Sources

[references/sources.md](references/sources.md) records the evidence behind each rule.

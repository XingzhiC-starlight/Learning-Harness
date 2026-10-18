---
name: starlight-mode
description: Use when the user states a goal and should not have to pick skills themselves, or asks for /starlight-mode. Matches the goal to a playbook and runs this repo's skills in order, naming each one.
---

# Starlight mode

The user says what they want. This skill picks the blocks and runs them in order, so nobody has to remember skill names. Each block stays its own skill; read its SKILL.md in full before applying it. This file only routes.

## Principles

One line per block: the idea, the skill, and when it applies.

- **Know the reader first.** `knowledge-quiz`, before any answer meant for a non-expert. Produces the reader line the other blocks use.
- **Fix the thinking before the wording.** `problem-identify`, when the problem is vague, a symptom, or a pre-chosen solution.
- **Answer as a solution, not a list.** `answer-frame`, for any answer with more than one idea in it.
- **Read it as the reader.** `reader-check`, after any answer written for a reader, before handing it over.
- **Learn an exemplar through its problems.** `research`, when studying work more advanced than the user's own.

## Playbooks

Match the request to one, say which, and run its blocks in order. Reuse a reader line already confirmed in the conversation. Skip a block only with a one-line reason.

- **Solve a problem**: knowledge-quiz, problem-identify, answer-frame, reader-check.
- **Answer a clear question**: knowledge-quiz, answer-frame, reader-check.
- **Learn from an exemplar**: knowledge-quiz, research, reader-check.
- **Nothing fits**: compose from the principles and say which you used.

## Growing this file

- New block in the repo: add one principle line naming the skill and when it applies.
- A combination used twice: add it as a playbook.
- Playbooks that outgrow one line move to `playbooks/<name>.md`, listed here by name.

## Guardrails
- Name the playbook and each block as you run it, so the user learns the blocks by seeing them.
- Never restate a block's procedure here.

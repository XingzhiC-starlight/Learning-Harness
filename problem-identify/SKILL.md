---
name: problem-identify
description: Use when someone wants an LLM's help with a problem but hasn't pinned down what the problem is, their prompts get vague, generic, or off-target answers, or they say "help me figure out what I'm actually asking". Clarifies the problem and its context with them, writes a prompt for their approval, runs it, and checks the answer against what the reader knows before returning it.
---

# Problem identify

A vague prompt usually means the problem is not yet clear to the person. Fix the thinking first, then the wording. Modern models reason well on their own; what they lack is the user's goal and situation, so that is what the prompt must carry.

## Procedure

1. **Clarify the problem.** Ask a few short questions at a time until you know what "solved" looks like, whether the stated problem is the root or a symptom or a pre-chosen solution, and what is in the way. Reflect the problem back in a sentence or two and get the user's confirmation.

2. **Gather context.** Only the details that would change the answer: their situation, constraints, audience, and what they have tried. Mark unknowns as assumptions.

3. **Get the reader line.** Reuse one already confirmed in this conversation; otherwise run knowledge-quiz.

4. **Write the prompt and show it.** It carries:
    - the goal, the context, and an invitation to question the premise if it looks mis-framed;
    - the reader line;
    - a request to answer in answer-frame's shape, with that skill's text pasted in, since a fresh subagent cannot load skills;
    - if the reader line marks the subject as unfamiliar, a request for one short worked example of it on the user's own material before any judgment of it.

   Skip role-play, step-by-step reasoning instructions, and filler; add a role only when it supplies a perspective the context does not. Show the prompt in a copyable block, with a note on what changed from the user's original and why, and ask whether it is good.

5. **Run the prompt.** Once the user approves, send it to a fresh subagent if available, otherwise answer it yourself exactly as written.

6. **Check the answer.** Run reader-check on it against the reader line, then return the fixed answer.

Close with one line showing their thinking chain ("you started from X, the real problem is Y, so the prompt asked for Z") so they can reuse the method.

## Guardrails
- Do not write the prompt before the problem is confirmed, unless the request is already specific.
- Do not run the prompt until the user approves it.

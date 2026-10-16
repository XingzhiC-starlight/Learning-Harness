---
name: prompt-thinking-coach
description: Use when someone wants an LLM's help with a problem but hasn't pinned down what the problem is, or their prompts get vague, generic, or off-target answers. Clarifies the problem and its context with them, writes a prompt for their approval, then runs it and returns the answer as principles, a plan, and technical details.
---

# Prompt thinking coach

A vague prompt usually means the problem is not yet clear to the person. Fix the thinking first, then the wording. Modern models reason well on their own; what they lack is the user's goal and situation, so that is what the prompt must carry.

## Procedure

1. **Clarify the problem.** Ask a few short questions at a time until you know what "solved" looks like, whether the stated problem is the root or a symptom or a pre-chosen solution, and what is in the way. Reflect the problem back in a sentence or two and get the user's confirmation.

2. **Gather context.** Only the details that would change the answer: their situation, constraints, audience, and what they have tried. Mark unknowns as assumptions.

3. **Write the prompt and show it.** State the goal, the context, and an invitation to question the premise if it looks mis-framed. Skip role-play, step-by-step reasoning instructions, and filler; add a role only when it supplies a perspective the context does not. Ask for the answer in this order, in common words, defining any specialized term where it first appears:
    1. **Principles**: the common-sense ideas behind the approach, and why each fits this case.
    2. **Plan**: the specific steps to take.
    3. **Technical details and recommendations**: the specifics needed to carry out the plan.

   Show the prompt in a copyable block, with a note on what changed from the user's original and why, and ask whether it is good.

4. **Run the prompt.** Once the user approves, send it to the model (a fresh subagent if available, otherwise answer it yourself exactly as written) and return the answer.

Close with one line showing their thinking chain ("you started from X, the real problem is Y, so the prompt asked for Z") so they can reuse the method.

## Guardrails
- Do not write the prompt before the problem is confirmed, unless the request is already specific.
- Do not run the prompt until the user approves it.

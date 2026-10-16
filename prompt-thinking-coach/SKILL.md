---
name: prompt-thinking-coach
description: Use when someone has a problem they want an LLM to help solve but hasn't yet pinned down what the problem is, or their prompts get vague, generic, or off-target answers. Walks them through clarifying the problem, supplying context, and rewriting the prompt so it activates the right expert perspective, then returns the principles behind the approach followed by a concrete plan and a ready-to-use prompt.
---

# Prompt thinking coach

For a person who has a problem and wants an LLM's help, but whose first prompt is still a rough thought. The goal is to surface their thinking logic chain (what they are really trying to achieve, what they already know, what is in the way) and turn it into a prompt that makes the model reason like the right expert instead of answering like a generalist.

A prompt is the visible end of a thought. A vague prompt usually means the problem is not yet clear to the person, so fix the thinking first, then the wording.

## Procedure

1. **Clarify the problem.** Ask at most 3 to 4 short questions at a time, in plain language, and wait for answers. Work down this chain, skipping what the user has already made clear:
    1. The goal: what would "solved" look like, and what will they do with the answer?
    2. The real problem: is this the problem itself or a symptom or a chosen solution? Ask "why do you need this?" once or twice until the root appears.
    3. The type of problem: deciding between options, diagnosing a cause, designing something new, learning a topic, producing content, or planning a path. The type determines the kind of expert and the shape of the answer.
    4. The gap: what has been tried, what is unknown, what makes it hard.

   Reflect the problem back in one or two sentences and get the user's confirmation before moving on.

2. **Supply the context.** Gather only the details that would change the answer: the user's situation and level, constraints (time, budget, tools, rules), the audience or stakes, relevant facts or materials, what they have already tried, and what a good answer must avoid. If a detail would not change the answer, leave it out. Mark anything unknown as an assumption rather than inventing it.

3. **Choose the expert and optimize the prompt.** Decide which kind of expert would solve this type of problem best (for example a senior architect for a design trade-off, an editor for rewriting, a clinician-style diagnostician for troubleshooting). Then write the prompt with these parts, in order:
    1. Role: the specific expert and their way of judging, not just a job title
    2. Goal: the problem and what success looks like
    3. Context: the details from step 2
    4. Task and reasoning: the steps the expert should take, e.g. question assumptions, compare options against the constraints, then recommend
    5. Output format: the shape of the answer, its length, and what to flag as uncertain
    6. Permission to push back: ask the model to question the premise or ask clarifying questions if the problem looks mis-framed

   Keep it as short as the problem allows. Do not pad it with flattery or generic filler.

4. **Present the result in this order:**
    1. **Principles**: the few ideas behind the approach for this problem type, in plain words, with a line on why each applies to this user's case. Define any specialized term where it first appears.
    2. **Recommendation / plan**: the specific steps for the user, including how to judge whether the LLM's answer is good and what to do if it is not.
    3. **The optimized prompt**: in a copyable block, with a short note on what changed from the original and why.

Close by offering one follow-up move, such as a second prompt for the next step or a way to test the answer. Show the user's thinking chain back to them in a line or two ("you started from X, the real problem is Y, so the prompt now asks for Z") so they can reuse the method next time.

## Guardrails
- Do not write the final prompt before the problem is confirmed, unless the user's request is already specific.
- Do not answer the underlying problem yourself in place of the plan unless the user asks. The deliverable is the clarified thinking, the principles, the plan, and the prompt.
- Adapt to the model the user names (e.g. its strengths or length limits); if none is named, write a model-agnostic prompt.

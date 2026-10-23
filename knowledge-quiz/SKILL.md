---
name: knowledge-quiz
description: Use before explaining anything to a non-expert, when another skill needs a reader line, or when the user asks "what level should you pitch this at". Finds out who will read the answer and what they know about the subject, and outputs one reader line for other skills to use.
---

# Knowledge quiz

An answer pitched at the wrong level fails however good it is. This skill finds out who will read it and what they already know about this subject, and writes that down as one reader line: one or two sentences giving the reader's role, what they have and haven't done with the subject, and how they will act on the answer. It only measures; it does not teach or answer.

## Procedure
1. **Name the subject.** List the few concepts the answer will rest on.

2. **Check the profile.** If `~/.claude/learner-profile.md` exists, read it (format in learner-profile) and take the levels for those concepts. A self-reported level is a starting point, not proof.

3. **Ask only about what is left.** For concepts the profile does not cover, or with no profile, ask two or three short questions about what they have done with the subject: built, used, fixed, read. Never ask whether they know a term.

4. **Write the reader line and confirm it.** Reflect it back and ask whether it is right. Correct it until they confirm.

5. **Hand it on.** Return the confirmed reader line to the skill or prompt that needs it.

## Guardrails
- Ask about what they have done, not what they know; "I know X" is weak evidence.
- Never write the profile. If you learned something worth recording, say so and name learner-profile as the skill that records it.
- Do not explain, correct, or answer during the questions.
- Reuse a reader line already confirmed in this conversation for the same subject instead of asking again.

---
name: learner-profile
description: Use when the user wants Claude to remember what they know across conversations, says "save my profile", "show my profile", "what do you know about me", "forget that", or when knowledge-quiz has confirmed a reader line worth keeping. Stores, shows, updates and deletes one optional file, ~/.claude/learner-profile.md, recording subject by subject what the user has done and how well they know it. Only records; never measures, teaches or answers.
---

# Learner profile

Each conversation otherwise starts from zero, and the user answers the same questions about what they know. The profile saves those answers so knowledge-quiz can start from them. It is the user's option: nothing is stored unless they say yes, and they can see, change or delete any of it at any time.

## The file

One file, `~/.claude/learner-profile.md`, about the person, not a project. If the user names another path, use that one instead.

```markdown
# Learner profile

<!-- Levels: 0 never heard of it · 1 recognizes the word · 2 knows what it is for ·
3 can predict what happens if it changes · 4 can do it themselves.
Evidence: said (the user told us) or shown (they explained or did it correctly). -->

## About
- Role: <what they do, in their words>
- Answers: <how they like answers pitched, if they said>

## Subjects
- <subject>: <level> <said|shown> — <what they have done with it> (<YYYY-MM-DD>)
```

Keep names of people, companies and products out of the file; keep only what changes how to pitch an answer.

## Procedure
1. **Ask before the first write.** If no profile exists, say what would be saved and where, and save only on a yes. If the user says no, do not ask again in this conversation.

2. **Record.** Turn what is in hand (a confirmed reader line from knowledge-quiz, or what the user just said about themselves) into entries in the format above. Show the new or changed lines and write them once the user agrees.

3. **Update by evidence.** Change a level only on new evidence. Shown beats said. A clearly failed explanation may lower a level. Replace the old line rather than adding a second one for the same subject.

4. **Show on request.** Print the profile in plain words, grouped by subject, with said and shown levels marked.

5. **Delete on request.** Remove the lines the user names, or the whole file if they ask.

## Guardrails
- Never write without the user's yes, and never invent answers to fill the file.
- Do not quiz the user here; measuring is knowledge-quiz's work.
- A said level is a starting point for knowledge-quiz, not proof.

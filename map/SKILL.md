---
name: map
description: Use when explaining something structured (a system, codebase, process, organization, concept, or body of information) that is large or interconnected for this reader's knowledge level, so text alone would leave them rebuilding the structure in their head. Offer it and use it when the user agrees, or when they ask for a map, diagram, or chart. Builds a knowledge map of diagrams and reference tables paired with text, so the reader understands the subject at a structural level from the output alone.
---

# Map

When a subject has many parts and connections, text alone makes the reader rebuild the whole structure in their head and link the parts themselves, which is exhausting. A map does that work for them: visuals carry the structure, text carries the meaning. Use it when the reader line (from knowledge-quiz) shows the subject is large and systematic for this reader; offer it, and map only if they agree.

## Procedure
1. **Orient first.** In 2-3 sentences, say what the thing is, what it is for, and how the explanation is organized.

2. **Map the big picture.** Draw one overview diagram showing the main parts and how they connect. Label every arrow with what moves or what the relationship is (data, control, dependency, ownership). Keep it to roughly 12 nodes or fewer.

3. **Define before you zoom.** For each important part, give a reference table before it appears in detail: what it is, what it takes in, what it produces or returns, its key properties or types, and who uses it. Use the same columns for every row.

4. **Zoom into what matters.** Make separate detail diagrams for the important flows or subsystems. Show order with numbered steps when sequence matters. If a diagram gets crowded, split it rather than compress it.

5. **Pair every visual with text.** Before each diagram or table, say what it shows and how to read it. After it, state the one or two things the reader should take away.

6. **Stay consistent.** Use identical names for the same thing across diagrams, tables, and text. Every diagram should connect visibly to the overview.

7. **Stay grounded.** Base everything on the source material. Mark anything inferred, ambiguous, or missing instead of filling gaps.

8. **Close with a short summary** that walks once through the whole system end to end.

## Guardrails
- Use the best visual format available (rendered diagrams, Mermaid, or similar).
- Prefer clarity over completeness: simple and big picture is fine, but it must be unambiguous.

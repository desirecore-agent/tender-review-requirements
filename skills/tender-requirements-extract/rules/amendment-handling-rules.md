# Amendment handling

## L0
Apply a change only after confirming applicability, the authentic publication/version relationship and explicit scope. Clause numbers, headings, unambiguous content descriptions and clearly scoped general notices can identify the affected obligation; a verbatim quotation of the old clause is not required. A label, date or language alone never determines precedence.

## L1
- Read the original and every relevant amendment. Distinguish verified publication facts from assumptions. A newer timestamp is not proof of authority or effect.
- Resolve exactly what changed: replacement, limited modification, clarification or withdrawal. Apply no wider effect. Preserve conditions, exceptions and obligations outside that scope; cite both the original obligation and the amendment's unchanged-scope statement.
- Process multiple amendments according to evidenced version/effect relationships. Do not choose the chronologically last text when those relationships or language precedence are unresolved. Keep competing interpretations in notes and report unresolved items for authorized decision.
- A full replacement keeps the original row as `superseded`, with `superseded_by` pointing to a real replacement row. Both endpoint IDs must appear in `supersede_relations`, whose directed edge set must equal the matrix links, without conflicts or cycles.
- For a partial change, track the affected component and its replacement separately from the surviving original obligations. The replacement row quotes its own amendment source; it does not manufacture a combined quotation. Surviving duties retain the original source and quote, with amendment file/location and the remaining-scope explanation in `notes`. Findings relying on the combined effect reference both rows/sources.
- A clarification that changes no obligation is recorded with its source and effect in `notes`; do not create a supersede edge or retire an active duty merely because a notice exists. Use `clarifies` relations only when the recorded interpretation actually supersedes a prior interpretation and both rows represent that transition.
- Explicit withdrawal uses `status: withdrawn`, with exact withdrawal source/location and scope in notes. Do not invent a replacement endpoint. A notice may add a genuinely new obligation when the applicable text expressly does so; an unresolved reference alone does not create a new obligation.

## L2
The payload supports `superseded_by`, `supersede_relations` and `notes`, not a separate `change_chain` object. Keep an auditable explanation using real IDs, source file IDs, locations and quotes. A missing clause reference, conflicting language versions or unclear publication authority stays `pending_review`; no confident noncompliance finding follows from an unresolved interpretation. A bid mentioning both old and new values is not automatically compliant—assess consistency with the verified effective obligation and report contradictions.

See [extraction](requirement-extraction-rules.md) and [classification](requirement-classification-rules.md).

# Requirement extraction

## L0
Use the finest granularity that preserves a whole verifiable obligation, its logic and applicability. An OR group remains one obligation with alternatives; do not turn alternatives into separate mandatory checks.

## L1
- Read every authorized relevant clause, table, footnote and referenced appendix; record actual file state. A structural heading alone is not an obligation. Capture a heading's real scope/condition with its dependent text, without inventing a duplicate parent duty.
- Separate genuinely independent obligations only if their subjects, conditions and consequences remain intact. AND conditions within one duty stay together; OR alternatives stay together even when they use different proof types. Mixed logic preserves parentheses and conditions in the verbatim quote and human explanation. Use top-level `logic: and/or/single` only as a truthful summary; the exact nested expression belongs in `condition`/`notes`, not unsupported nested JSON.
- Each row needs `requirement_id`, `source_file_id`, `location`, verbatim `source_quote`, `requirement_type` and `status`. Preserve source punctuation, negation, quantifiers, exceptions and relevant context. Do not impose an arbitrary excerpt length that drops an exception; keep the necessary passage exact and explain separately in notes.
- Optional fields are `subject`, `condition`, `logic`, `quantifier`, `exception`, `proof_requirement`, `superseded_by`, `is_mandatory`, `notes`. Record the actual value, comparison operator, unit, denominator, cap and rounding basis in these supported strings when relevant. Unknown operands or denominators are explicit limitations, never zero or pass. Calculate thresholds from source definitions; do not divide by an assumed maximum.
- Signature/seal evidence preserves the named actor, signing method, seal type, format and AND/OR relationship in `proof_requirement` and notes. Undefined wording such as “signed/sealed” remains ambiguous unless the applicable source explains it. Image presence is not authenticity.
- Amendments follow the [amendment rules](amendment-handling-rules.md). Clause applicability/status (`active`, `superseded`, `withdrawn`, `pending_review`) is not the same as bid response status. Record complete/partial/conflicting/unresolved response in finding descriptions or coverage notes; do not put those values in requirement status.

## L2: coverage and delivery
Coverage items describe actual review actions, with only `checked`, `failed`, `unchecked`. Do not add a requirement_id field to a coverage item. Link findings through requirement_refs and bid_evidence instead. `present`/`absence` describe bid evidence types, not coverage status. Absence requires named checked items covering the relevant same-file search scope; unknown is not absence.

Count items exactly. Every manifest file remains covered or individually excluded with `file_id: non-empty reason` based on authorized scope, never convenience or unread status. A ledger can be accounting-closed with reasoned failed/unchecked items; the report must still be partial/cannot_conclude when review is incomplete. File status pending/partial/failed cannot support checked evidence: split input scope/version only with a real new manifest, never relabel a failed file to pass validation.

Use actual source IDs and values, not the example template IDs or counts. Produce only owned contributions. The lead reconciles cross-role coverage and writes the sole final report; independent Evidence checks the six-artifact pack and re-reads evidence.

See [classification](requirement-classification-rules.md) and [locations](location-format-rules.md).

# Requirement classification

## L0
Classify the obligation's subject separately from its consequence and the certainty of any finding. Use only the shared `requirement_type` enum. A missing certificate, binary check or unknown category never proves rejection or mandates high severity.

## L1
| Value | Source-backed use |
|---|---|
| `qualification` | Participation prerequisites, credentials or capacity |
| `substantive_response` | Required proposal content, performance or commitments |
| `scoring` | Scoring formulas, point allocation, thresholds or evaluation criteria |
| `submission` | Delivery, timing, format, copies and signature/seal procedure |
| `compliance` | Express compliance/legal obligations established as applicable |
| `other` | An identified obligation not fitting a known subject; explain uncertainty |

Read the clause and its referenced provisions before deciding. If one passage imposes independent participation and scoring obligations, preserve both with cross-references; if it is one compound obligation, keep its logic and select the best supported subject, describing the other aspect in notes. Do not use a severity hierarchy to decide type. A scoring provision may include an explicit minimum passing threshold; do not assume all scoring shortfalls are harmless or all scores imply rejection.

`is_mandatory` has a narrow contract meaning: true when applicable source provisions establish rejection on noncompliance; false for an established scoring deduction. Omit it when the consequence is not established, and explain in notes. A general “must” alone does not prove rejection. Record the exact consequence quote and source location in notes or a separate sourced requirement row when it is elsewhere. Do not emit `disqualification` or `eligibility` as new enum values.

## L2
Finding `severity` is impact (`potential_rejection`, `high`, `medium`, `low`, `informational`); `certainty` is evidence confidence (`confirmed`, `likely`, `uncertain`, `unverified`). State source-backed impact and evidence limitations separately. Potential rejection needs an explicit applicable rejection basis, precise requirement refs and bid-side evidence; actual absence needs completed same-file searched coverage. Unread or illegible content cannot establish confirmed absence.

An author sets `open` or `pending_review`. Only independent Evidence may produce `reviewed_confirmed`, `reviewed_downgraded` or `reviewed_withdrawn`, with traceable reasons. Formal eligibility and rejection decisions remain with authorized people. Prioritize credible serious risks without inflating severity to compensate for uncertainty.

See [amendments](amendment-handling-rules.md) and [extraction](requirement-extraction-rules.md).

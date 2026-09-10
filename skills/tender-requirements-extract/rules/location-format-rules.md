# Source locations

## L0
A locator must navigate to actual observed content in a specific manifest file. Neither a nonempty string nor a repeated placeholder is evidence.

## L1
- PDF: use physical pages counted from 1, such as `p.1` or `p.12-15`. A range has ordered positive bounds and cannot exceed the file's verified `physical_pages`. Printed pagination, chapter labels and page-number mapping belong in `notes`, not a mixed physical locator. Do not infer physical pages from printed numbers.
- DOCX and extracted text: preserve the actual extraction tool's logical locator and index convention. If the tool emits `body:N` with N starting at 1, cite that exact paragraph; if it emits `table:N/row:N` with row 0 as the first stored row, retain header rows in that numbering. Do not invent a heading path or change a tool's row base. Repeated headings require an unambiguous table/paragraph identity and enough context to find the source again.
- A heading/paragraph locator may be used only when it is actually recoverable from the extracted document. Record its convention in task notes and use it consistently on both sides of the evidence/coverage link. Logical locators are opaque exact matches to the validator; a broader-looking heading does not automatically cover narrower paragraphs.
- Standalone images: cite the actual image file and observed region, keeping a reproducible region convention. Read/render the image and report legibility. Text extraction alone does not prove a visual feature, seal, signature or diagram detail.
- Requirement references use their canonical `source_file_id`; bid evidence must use the actual bid-side file. Present evidence needs checked coverage of the same file/location, and a given coverage ID restricts the reference to that item. Physical page ranges need complete coverage of their intervals.

## L2: unknown or failed location
Do not put a generic unknown-location token into a requirement or evidence location. If no exact source quote/location can be obtained, omit the incomplete requirement row and list the missing extraction in failed/unchecked coverage, findings limitations and the lead's unresolved/unchecked report items. Do not fabricate required fields to pass Schema. A method-only checked item may describe an action performed, but cannot support located evidence. Failed or unread content cannot establish absence. Retry with authorized rendering/extraction or request a readable source, then update coverage based on actual observation.

Unicode decimal page digits can be parsed, but prefer ordinary decimal digits in generated locators. Unsupported expressions, out-of-range pages, file paths, hashes and timestamps cannot substitute for locations. These format examples are conventions, not fixed business values.

See [extraction](requirement-extraction-rules.md).

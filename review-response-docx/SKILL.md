---
name: review-response-docx
description: Draft, analyze, format, and package point-by-point reviewer responses and revised manuscript DOCX files. Use when the user provides reviewer comments, peer-review reports, editor decision letters, manuscript text or Word files, revision notes, figure/table change requests, or asks for 返修意见回复, 审稿意见回复, Response to Reviewers, rebuttal letter, point-by-point response, revised manuscript text, tracked/marked revision manuscript, clean version manuscript, or formatted Word response documents.
---

# Review Response DOCX

Use this skill to turn reviewer comments and manuscript source material into a rigorous
point-by-point response package, revised manuscript files, and polished Word documents.

## Coordinate With Other Skills

- If the task involves DOCX creation or editing, use the Documents skill/plugin workflow for reading, editing, rendering, and QA.
- If the target journal is Nature-family or the user explicitly asks for `nature-response`, also use that skill for reviewer-response stance and QA.
- Use the user's required Python environment when running local programs. In this workspace, the user has specified WSL `env_py3.11`.

## Intake

Collect or infer:

- manuscript number, manuscript title, and author list
- original manuscript Word file, manuscript text, revised manuscript text, or relevant sections
- editor letter and reviewer comments
- existing response draft or response DOCX, if any
- journal style constraints, if supplied
- figures/tables affected by reviewer comments
- whether the user wants the full default package or only selected outputs

If key information is missing, continue with a draft but mark missing evidence explicitly. Do not invent line numbers, page numbers, experiments, citations, figure updates, or manuscript changes.

## Workflow

1. Segment comments by editor/reviewer and assign stable IDs.
2. Preserve every reviewer comment faithfully before responding.
3. For each comment, follow the analysis sequence in `references/response-analysis.md`.
4. Decide whether the manuscript, figures, tables, references, or only the response letter need revision.
5. Draft bilingual response content when helpful: Chinese first for author comprehension, English for the final response letter.
6. When a manuscript change is claimed, include a concrete `Revised manuscript text (Lines X-Y):` block after the reply. Use exact line ranges only when available from the revised manuscript; otherwise mark them as pending.
7. Apply confirmed changes directly to the user's original manuscript Word file when provided.
8. Produce the requested Word outputs using the formatting standard in `references/docx-format.md`.
9. Validate completeness: every reviewer concern has a translation, analysis, action decision, reply, and revised text or missing-info note.
10. Render and visually inspect DOCX outputs when LibreOffice/soffice is available. If rendering is unavailable, disclose that visual QA could not be completed.

## Response Rules

- Keep the response polite, professional, and evidence-linked.
- Start replies by thanking the reviewer, then state whether the comment was accepted and what was changed.
- Map each claimed change to a section, paragraph, figure, table, reference list, or explicit placeholder.
- For manuscript revisions, preserve the author's original meaning and conclusions unless the evidence or user instructions require a change.
- If no manuscript change is needed, explain why the response-letter explanation is sufficient.
- If a requested change is out of scope, acknowledge its value and give a scientific scope reason, not a time or convenience excuse.
- If literature needs to be added, use real, reliable references only; if citation certainty is low, ask the user or mark it for verification instead of inventing.
- If figures or tables are affected, state which figure/table should change, what to change, why, and mirror the change in the revised manuscript or caption when possible.

## Output Modes

- **Analysis only:** provide the per-comment Chinese translation, analysis, action judgment, suggestions, Chinese reply, English reply, revised manuscript text, and missing information.
- **Full default package:** produce four files when the user supplies enough material:
  1. a bilingual revision-comment analysis Word document
  2. a formatted Response to Reviewers Word document
  3. a revised manuscript Word file with changes clearly marked and all added/modified text in red
  4. a clean revised manuscript Word file with all changes accepted and no visible markup
- **Response DOCX creation:** produce a Word document with title, authors, opening thanks, reviewer headings, blue reviewer comments, black replies, and revised manuscript text blocks with line ranges.
- **Existing DOCX update:** preserve the existing structure where possible and replace placeholders or append missing sections.
- **Manuscript revision:** create both marked and clean versions from the provided original Word file; if true Word tracked changes are not feasible, use clear red-font markup for all additions/modifications and disclose the limitation.

## References

- Read `references/response-analysis.md` before drafting the point-by-point content.
- Read `references/docx-format.md` before creating or editing the Word response document.

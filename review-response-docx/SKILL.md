---
name: review-response-docx
description: Draft, analyze, and format point-by-point reviewer response letters for manuscript revisions, then create or update a polished Word DOCX. Use when the user provides reviewer comments, peer-review reports, editor decision letters, manuscript text, revision notes, or asks for 返修意见回复, 审稿意见回复, Response to Reviewers, rebuttal letter, point-by-point response, revised manuscript text, or a formatted Word response document.
---

# Review Response DOCX

Use this skill to turn reviewer comments and manuscript source material into a rigorous
point-by-point response package and a clean Word document.

## Coordinate With Other Skills

- If the task involves DOCX creation or editing, use the Documents skill/plugin workflow for reading, editing, rendering, and QA.
- If the target journal is Nature-family or the user explicitly asks for `nature-response`, also use that skill for reviewer-response stance and QA.
- Use the user's required Python environment when running local programs. In this workspace, the user has specified WSL `env_py3.11`.

## Intake

Collect or infer:

- manuscript number, manuscript title, and author list
- original manuscript text, revised manuscript text, or relevant sections
- editor letter and reviewer comments
- existing response draft or response DOCX, if any
- journal style constraints, if supplied
- figures/tables affected by reviewer comments

If key information is missing, continue with a draft but mark missing evidence explicitly. Do not invent line numbers, page numbers, experiments, citations, figure updates, or manuscript changes.

## Workflow

1. Segment comments by editor/reviewer and assign stable IDs.
2. Preserve every reviewer comment faithfully before responding.
3. For each comment, follow the analysis sequence in `references/response-analysis.md`.
4. Decide whether the manuscript, figures, tables, references, or only the response letter need revision.
5. Draft bilingual response content when helpful: Chinese first for author comprehension, English for the final response letter.
6. When a manuscript change is claimed, include a concrete `Revised manuscript text:` block after the reply.
7. Create or update the DOCX using the formatting standard in `references/docx-format.md`.
8. Validate completeness: every reviewer concern has a translation, analysis, action decision, reply, and revised text or missing-info note.
9. Render and visually inspect the DOCX when LibreOffice/soffice is available. If rendering is unavailable, disclose that visual QA could not be completed.

## Response Rules

- Keep the response polite, professional, and evidence-linked.
- Start replies by thanking the reviewer, then state whether the comment was accepted and what was changed.
- Map each claimed change to a section, paragraph, figure, table, reference list, or explicit placeholder.
- If no manuscript change is needed, explain why the response-letter explanation is sufficient.
- If a requested change is out of scope, acknowledge its value and give a scientific scope reason, not a time or convenience excuse.
- Do not change the manuscript's core conclusions unless the user asks for that or the evidence requires it.

## Output Modes

- **Analysis only:** provide the per-comment Chinese translation, analysis, action judgment, suggestions, Chinese reply, English reply, revised manuscript text, and missing information.
- **DOCX creation:** produce a Word document with title, authors, opening thanks, reviewer headings, blue reviewer comments, black replies, and revised manuscript text blocks.
- **Existing DOCX update:** preserve the existing structure where possible and replace placeholders or append missing sections.

## References

- Read `references/response-analysis.md` before drafting the point-by-point content.
- Read `references/docx-format.md` before creating or editing the Word response document.

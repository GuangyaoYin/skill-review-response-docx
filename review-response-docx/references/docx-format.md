# Word Response Letter Format

Use this standard when creating or updating reviewer-response and manuscript-revision DOCX outputs.

## Page Setup

- Page size: A4 unless the user requests another size.
- Margins: 2.54 cm on all sides.
- Font: Times New Roman throughout.
- Body font size: 12 pt.
- Line spacing: 1.15 or 1.5, prioritizing readability and page economy.
- Paragraph spacing: modest spacing after paragraphs; avoid decorative elements.
- Alignment:
  - title, authors, reviewer headings, reviewer comments: left aligned
  - reply body and revised manuscript text: justified when supported cleanly by the DOCX tool

## Front Matter

1. Title at top of first page:

```text
Response to reviews of manuscript #[manuscript number] '[paper title]'
```

Style:
- Times New Roman
- bold
- 18-20 pt
- left aligned
- allow natural wrapping for long titles

2. Author line:

```text
Author1, Author2, Author3...
```

Style:
- Times New Roman
- 12-14 pt
- regular
- left aligned

3. Opening paragraph:

- Thank the editor and reviewers.
- State that the manuscript has been carefully revised.
- Use formal academic tone.
- Times New Roman, 12 pt, black.
- Leave one blank line between the author list and this paragraph.

## Reviewer Sections

Use one first-level reviewer heading per reviewer:

```text
Reviewer 1:
Reviewer 2:
```

Style:
- Times New Roman
- bold
- 14-16 pt
- black
- left aligned

## Per-Comment Formatting

For each reviewer comment:

```text
(1) [reviewer original comment]

Reply: [English reply]

Revised manuscript text (Lines 215-228):
[revised manuscript paragraph]
```

Reviewer comment style:
- Times New Roman
- 12-13 pt
- blue
- left aligned
- use hanging indent or paragraph indent so the number is visually clear

`Reply:` label:
- bold
- black
- Times New Roman
- 12 pt

Reply body:
- black
- Times New Roman
- 12 pt
- justified where possible
- polite, professional, and concise

`Revised manuscript text:` label:
- bold
- black
- Times New Roman
- 12 pt
- include the revised manuscript line range in the label whenever available, for example `Revised manuscript text (Lines 215-228):`
- if exact line numbers are unavailable, use a clear pending marker such as `Revised manuscript text (line numbers to be confirmed):` rather than inventing lines

Revised manuscript text body:
- black
- Times New Roman
- 12 pt
- justified where possible
- include only when manuscript text was or should be changed

## Content Separation

Make the three layers visually distinct:

- reviewer comments: blue
- author replies: black
- revised manuscript text: black, introduced by bold label

Do not use decorative borders, colored boxes, tables, or ornate styles unless the user explicitly asks.

## Required Output Package

When the user asks for the full package and provides enough source material, create:

1. `revision-comment-analysis-bilingual.docx`
   - Include Chinese and English analysis for each editor/reviewer comment.
   - For each comment, include translation, issue analysis, revision decision, manuscript-edit suggestion, Chinese reply, English reply, revised manuscript text or missing-information note.

2. `response-to-reviewers.docx`
   - Use the front matter and reviewer-section formatting above.
   - Keep reviewer comments blue and author replies/revised text black.
   - Include revised manuscript line ranges in every revised-text label where possible.

3. `revised-manuscript-marked.docx`
   - Start from the user's original manuscript Word file.
   - Preserve the manuscript's original formatting as much as possible.
   - Show changes with true Word tracked changes when the available tooling supports it.
   - If true tracked changes are not feasible, make every added or modified text red and clearly visible.
   - For figure/table changes, update captions, callouts, notes, or nearby explanatory text as needed and mark modified text in red.

4. `revised-manuscript-clean.docx`
   - Accept all changes conceptually.
   - Remove visible markup and red change styling unless red text was part of the original manuscript style.
   - Preserve the revised content and original manuscript formatting.

Use clear, descriptive filenames if the manuscript number or journal name is available.

## Figures and Tables

- In the response letter, explicitly state the affected figure or table number.
- State what should be changed, why the change addresses the comment, and where the corresponding manuscript text/caption was revised.
- Do not claim that images, plots, or tables were changed unless the source file or enough editable content was available to make or specify the change.

## DOCX QA

- Check that every reviewer comment has a reply.
- Check that every claimed manuscript revision has `Revised manuscript text:` or a clear location/action note.
- Check that every `Revised manuscript text:` label includes a line range or an explicit pending-line note.
- Check that numbering is sequential within each reviewer.
- Check that the marked manuscript visibly distinguishes additions/modifications in red or true tracked changes.
- Check that the clean manuscript has no reviewer-response markup and no red change styling introduced only for review visibility.
- Render with the Documents skill when `soffice`/LibreOffice is available.
- If rendering is unavailable, perform structural text extraction checks and disclose the missing visual QA.

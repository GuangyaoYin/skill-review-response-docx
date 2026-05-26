# Word Response Letter Format

Use this standard when creating or updating a reviewer-response DOCX.

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
Response to reviews of manuscript #[manuscript number] "[paper title]"
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

Revised manuscript text:
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

## DOCX QA

- Check that every reviewer comment has a reply.
- Check that every claimed manuscript revision has `Revised manuscript text:` or a clear location/action note.
- Check that numbering is sequential within each reviewer.
- Render with the Documents skill when `soffice`/LibreOffice is available.
- If rendering is unavailable, perform structural text extraction checks and disclose the missing visual QA.

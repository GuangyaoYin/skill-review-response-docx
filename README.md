# Review Response DOCX Skill

`review-response-docx` is a Codex skill for drafting rigorous point-by-point reviewer responses and producing a clean, formal Word document for manuscript revision submissions.

It is designed for academic revision workflows where the author provides reviewer comments, editor instructions, a manuscript draft, and optional author notes. The skill helps analyze each reviewer comment, draft bilingual response content when useful, generate polished English `Response to Reviewers` text, and format the final response letter as a professional `.docx`.

## What It Does

- Translates each reviewer comment into Chinese for quick author understanding.
- Analyzes the core concern behind each comment.
- Classifies the issue type, such as language, logic, method, results interpretation, figures/tables, references, novelty, or limitations.
- Judges whether the manuscript text, figures, tables, references, or only the response letter need revision.
- Gives concrete, actionable manuscript-edit suggestions.
- Drafts both Chinese and English replies in a polite SCI-style response format.
- Adds `Revised manuscript text:` blocks whenever a manuscript change is claimed.
- Creates or updates a Word response document with formal academic formatting.

## DOCX Formatting Standard

The skill uses a clean manuscript-revision style:

- Times New Roman throughout.
- Formal title: `Response to reviews of manuscript #[ID] "[Title]"`.
- Reviewer sections such as `Reviewer 1:` and `Reviewer 2:`.
- Reviewer comments in blue.
- `Reply:` labels in bold black.
- Author replies in black.
- `Revised manuscript text:` labels in bold black.
- A4 page layout with conventional academic margins and readable spacing.

## Installation

Install this skill into Codex from this repository:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo GuangyaoYin/skill-review-response-docx \
  --path review-response-docx
```

After installation, restart Codex so the new skill is loaded.

## Usage

Example prompt:

```text
Use $review-response-docx to analyze the reviewer comments and manuscript, then create a polished Word response letter.
```

Chinese example:

```text
使用 review-response-docx，根据论文原文和审稿意见，逐条完成返修意见回复，并生成排版良好的 Word 文档。
```

## Files

- `review-response-docx/SKILL.md`: main workflow and triggering instructions.
- `review-response-docx/references/response-analysis.md`: per-comment analysis and response-writing standard.
- `review-response-docx/references/docx-format.md`: Word formatting requirements for the response letter.
- `review-response-docx/agents/openai.yaml`: Codex UI metadata.

## Notes

This skill does not invent manuscript changes, line numbers, experiments, citations, or figure revisions. If the available manuscript material is insufficient, it explicitly lists the missing information needed for a rigorous response.

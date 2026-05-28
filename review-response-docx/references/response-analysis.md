# Response Analysis Standard

For every reviewer comment, output all of the following in order unless the user explicitly asks for a shorter mode.

## Per-Comment Sequence

1. **Chinese translation of the reviewer comment**
   - Translate faithfully and fluently.
   - Preserve technical meaning, uncertainty, and criticism level.
   - Do not soften or exaggerate the reviewer's concern.

2. **Analysis**
   - State the core issue the reviewer is raising.
   - Explain what the reviewer wants clarified, supplemented, or changed.
   - Classify the issue, using one or more categories:
     - language/expression
     - logic/structure
     - method/model
     - result interpretation
     - figure/table
     - references/citation
     - novelty/significance
     - scope/limitation
     - formatting/cross-reference
     - other

3. **Revision decision**
   - State whether manuscript text needs revision.
   - State whether figures or tables need revision.
   - If yes, explain why and how extensive the change should be.
   - If no, explain why response-letter clarification is sufficient.

4. **Specific manuscript-edit suggestions**
   - Identify the target section, paragraph, figure, table, reference list, or caption when possible.
   - Describe what to add, delete, reorganize, soften, or clarify.
   - Suggest added evidence, data, citations, definitions, limitations, or logic bridges only when supported by the manuscript or user-provided facts.
   - Keep suggestions close to the author's original claims and conclusions.
   - If a figure or table should change, identify the figure/table number, the exact proposed change, why it addresses the comment, and any caption/text that must be updated.

5. **Final reply in Chinese**
   - Thank the reviewer.
   - State whether the comment was accepted.
   - Explain the action taken or the reason for not changing the manuscript.
   - Mention the revision location if known.

6. **Final reply in English**
   - Use SCI-style `Response to Reviewers` prose.
   - Be concise, respectful, and auditable.
   - If revised, state what was revised and where.
   - If not revised, give a scientific explanation.

7. **Revised manuscript text**
   - Include this only when manuscript text is modified or should be modified.
   - Provide the actual revised English paragraph for English manuscripts.
   - Keep the paragraph consistent with the manuscript's style and conclusions.
   - Include the revised line range when available, using `Revised manuscript text (Lines X-Y):`.
   - Do not invent new experiments, results, citations, figures, or line numbers.

8. **Missing information**
   - If the available material is insufficient for a rigorous response, list exactly what is needed:
     - relevant original paragraph
     - target figure/table
     - calculation or experiment details
     - study background or author intent
     - journal format requirements
     - exact revision location
     - exact revised manuscript line numbers

## English Reply Pattern

Use this default structure:

```text
We thank the reviewer for this constructive comment. We agree that [issue] needed to be clarified. We have revised [section/location] to [specific action]. The revised text now [effect of revision].

Revised manuscript text:
[revised paragraph]
```

For limited or no revision:

```text
We thank the reviewer for raising this point. We agree that [issue] is important. In the present revision, we address this point by [clarification/limited revision]. We did not [requested action] because [scientific scope/evidence reason]. To avoid overstatement, we have [softened/clarified/added limitation] in [location].
```

## Guardrails

- Do not answer only with "we have revised accordingly."
- Do not claim a change was made unless the revised text is supplied or the user has confirmed it.
- Do not fabricate page/line numbers.
- Do not fabricate references. If a citation is only a likely candidate, mark it for user verification.
- Do not cite convenience, time, or funding as the main reason for declining a request.
- Do not accuse the reviewer of misunderstanding; frame it as a clarity issue in the manuscript.
- Do not revise beyond the manuscript's evidence base or alter the study conclusions without explicit support.

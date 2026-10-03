# KFS description format and submission notes

Checked October 3, 2026 against the live KFS site, including the user's open submission form in Chrome.

## What was verified

- The [submission form](https://kfs.koinscan.com/submit) uses a native `textarea` for Project Description, with no rich-text toolbar or formatting preview.
- The inspected field has no HTML `maxlength` attribute. The deployed submit-page code passes the description string directly to `submit_project`; its visible validation checks that the description is nonempty.
- The deployed homepage renders descriptions directly as text inside paragraph elements, with a three-line preview. It does not apply Markdown or HTML rendering to those previews.
- The [submission documentation](https://kfs.koinscan.com/docs#submitting-projects) asks for a description but does not document Markdown or rich-text support.

Use plain text and complete URLs. Markdown markers can be entered as characters, but the inspected previews do not format them. A plain URL may remain copyable text rather than a clickable link; automatic link conversion has not been established. The repository provides the formatted reading experience.

This is a form and project-preview check, not an on-chain submission test or an audit of every project-detail view. No description-size guarantee is inferred from the absence of a frontend length attribute; the contract and transaction resource limits were not verified. No wallet connection, signing, or KFS submission was performed.

## Inspected deployed assets

- [Submission frontend](https://kfs.koinscan.com/_next/static/chunks/app/submit/page-524e085143d3caba.js)
- [Homepage project previews](https://kfs.koinscan.com/_next/static/chunks/app/page-285b66bcdaaeb431.js)

These build-specific asset URLs may change after a site update. Recheck the current form before a future submission.

## Preparing each proposal

Keep `PROPOSAL_EN.md` as the formatted proposal and `SUBMISSION_EN.txt` as its plain-text description. Preserve the scope, budget, hours, dates, and commitments in both files; replace tables with labeled lines and Markdown links with full URLs. Put the proposal's direct GitHub URL near the start of the description.

The project title, monthly payment, beneficiary, and dates have their own KFS fields. The folder README records their intended values. Before signing, confirm those fields, update the market conversion, check the actual fee and funded period, and review the exact description.

After a confirmed submission, record the KFS project URL and the submitted Git commit in the proposal folder README. Git history preserves the submitted text even if the working draft later changes.

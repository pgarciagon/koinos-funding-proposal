# KFS description format and submission notes

Checked October 3, 2026 against the live KFS site, including the user's open submission form in Chrome.

## What was verified

- The [submission form](https://kfs.koinscan.com/submit) uses a native `textarea` for Project Description, with no rich-text toolbar or formatting preview.
- The inspected field has no HTML `maxlength` attribute. The deployed submit-page code passes the description string directly to `submit_project`; its visible validation checks that the description is nonempty.
- The deployed homepage renders descriptions directly as text inside paragraph elements, with a three-line preview. It does not apply Markdown or HTML rendering to those previews.
- The [submission documentation](https://kfs.koinscan.com/docs#submitting-projects) asks for a description but does not document Markdown or rich-text support.

Use plain text and complete URLs. Markdown markers can be entered as characters, but the inspected previews do not format them. A plain URL may remain copyable text rather than a clickable link; automatic link conversion has not been established. The repository provides the formatted reading experience.

This is a form and project-preview check, not an on-chain submission test or an audit of every project-detail view. The absence of a frontend length attribute does not remove the contract description limit documented below. No wallet connection, signing, or KFS submission was performed.

## Contract limits and the submission failure

On October 3, 2026, the [fund contract source at commit 4fc33bbe0520a77a89619da1e9e6efe98e7c423c](https://github.com/koinos/koinos-contracts-as/blob/4fc33bbe0520a77a89619da1e9e6efe98e7c423c/contracts/fund/assembly/Fund.ts#L275) was checked. `submit_project` requires a nonempty title of at most 100 characters and a nonempty description of at most 1,000 characters. The description check is at line 277. It runs before beneficiary, date, fee, or transfer checks. The accompanying error says "description must be defined and less than 1000 characters", although the comparison allows exactly 1,000.

The earlier full description contained 15,563 characters excluding its trailing newline, exceeding the source limit. The KFS page logged "Error submitting project: Error: Connection lost" during the user's attempt; the exact wallet error was not available to the browser tool. The short summary removes this known validation violation, but does not establish that every transaction or wallet check will succeed.

The deployed frontend fund helper in chunk `189-66586d9a3322fc25.js` uses contract `1A5BmMqV5jN5zBrdkhQumAfDZBzXLPBeN9` and `submit_project` entry point `0x3baabbbd`. A read-only `chain.read_contract` check against the public RPC was attempted and returned HTTP 403, so source-to-deployed-bytecode equivalence and an on-chain rejection were not independently confirmed. No signed transaction or submission was sent by Codex.

Use an ASCII summary with room below 1,000 characters, including all URLs and line breaks. The original local description was 922 characters excluding its trailing newline; later revisions have their own checked lengths recorded in their folder README. Keep the full proposal in GitHub and link to it from the summary. Also check valid dates, beneficiary, current required submission fee, token-transfer authorization, balance, and Mana in the wallet; those are separate from the text limit.

## Inspected deployed assets

- [Submission frontend](https://kfs.koinscan.com/_next/static/chunks/app/submit/page-524e085143d3caba.js)
- [Homepage project previews](https://kfs.koinscan.com/_next/static/chunks/app/page-285b66bcdaaeb431.js)

These build-specific asset URLs may change after a site update. Recheck the current form before a future submission.

## Preparing each proposal

Keep `PROPOSAL_EN.md` as the formatted proposal, `FULL_PROPOSAL_EN.txt` as the full plain-text edition, and `SUBMISSION_EN.txt` as the short contract-compatible description. Preserve the scope, budget, hours, dates, and commitments across these versions. The short description must include the full GitHub URL within its 1,000-character limit; the full edition may use labeled lines and complete URLs instead of tables and Markdown links.

The project title, monthly payment, beneficiary, and dates have their own KFS fields. The folder README records their intended values. Before signing, confirm those fields, update the market conversion, check the actual fee and funded period, and review the exact description.

After a confirmed submission, record the KFS project URL and the submitted Git commit in the proposal folder README. Git history preserves the submitted text even if the working draft later changes.

## Freezing a proposal for submission

For the November 2026 proposal, the summary links to release `proposal-2026-11-v1.0.0`. The release contains `PROPOSAL_EN.md`, `FULL_PROPOSAL_EN.txt`, `SUBMISSION_EN.txt`, a release manifest recording the source commit, and `SHA256SUMS`.

GitHub release immutability is enabled for this repository. Publish each release as a draft first, attach and verify all files, then publish it. The published tag and assets are protected from replacement. The release title and notes remain editable, so treat the attached files and the commit recorded in the manifest as the authoritative proposal. Repository availability is separate from content immutability.

Keep a local copy of the release files. Later corrections must use a new version and release; retain the version already referenced by a submitted KFS proposal. A frozen GitHub release does not prove KFS submission or funding.

## End dates and the January payment correction

On October 8, 2026, read-only mainnet calls confirmed proposal #9 ends at `2027-01-31T00:00:00Z`, while the scheduled January payment is `2027-01-31T12:00:00Z`. The inspected `pay_projects()` source removes expired projects before selecting payments. An end date must be after the last intended payment event; for November 2026 through January 2027, use `2027-02-01T00:00:00Z`.

The deployed KFS ABI exposes no project-edit method. The user requested a replacement with the same scope and budget, recorded in `proposals/2026-11-infrastructure-maintenance-corrected/`. It uses release `proposal-2026-11-v1.0.1`, leaves the original frozen reference intact, and identifies #9 as the proposal it replaces. This is a full three-month replacement, not an additional January-only request.

After confirmed submission, voters must explicitly move their support from #9 to the replacement. Votes do not migrate automatically and overlapping support can fund the same work twice. The correction's observed submission fee was 2.7264384 KOIN, using the then-current project counts and fee denominator; verify the form's actual fee before signing. Completing the form and publishing the release do not prove a replacement was submitted.

## October 15 extension and calendar-based hours

The user subsequently extended the replacement's start to October 15, 2026. The canonical prepared revision is now `proposals/2026-10-infrastructure-maintenance/`, frozen as `proposal-2026-10-v1.0.2`. The earlier immutable releases remain unchanged.

October 15 through February 1 exclusive is 109 days. At three hours weekly, the time allocation is 46.71428571 planned hours, costing USD 1,167.86 at USD 25/hour. Four monthly subscription and hosting charges add USD 1,104.08, making the expense estimate USD 2,271.94. The 34,000 KOIN monthly request is preserved; four eligible payment events make the intended total 136,000 KOIN. The original USD 0.018/KOIN reference is historical. At that reference the request equals USD 2,448, including a USD 176.06 allowance above estimated expenses for cost or conversion changes.

KFS does not prorate the partial October payment. The eligible scheduled events are October 31, November 30, December 31, and January 31 at 12:00 UTC. Read-only mainnet metadata on October 8 gave an observed submission fee of 3.2302368 KOIN for these dates; the fee can change with the contract's project counts. Recheck before signing.

This supersedes the earlier November-start preparation. It does not edit or cancel the published #9, automatically transfer votes, or prove a replacement transaction was submitted.

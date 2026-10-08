# Pablo Garcia — Koinos Funding Proposals

Public proposals for Koinos infrastructure, developer tools, documentation, Vortex validator work, and community support. Each proposal has its own folder, funding period, and submission text.

## Proposals

| Proposal | Proposed funding period | Monthly request | Status |
| --- | --- | ---: | --- |
| [Infrastructure, documentation, and community maintenance — corrected end date](proposals/2026-11-infrastructure-maintenance-corrected/) | November 2026–January 2027; ends February 1 | 34,000 KOIN | Replacement prepared; not submitted to KFS |
| [Original infrastructure proposal](proposals/2026-11-infrastructure-maintenance/) | November 2026–January 2027; ends January 31 | 34,000 KOIN | [Submitted as #9](https://kfs.koinscan.com/projects/9); end-date correction prepared |

The corrected proposal commits three hours per week with the same scope and budget as #9. Read the [formatted proposal](proposals/2026-11-infrastructure-maintenance-corrected/PROPOSAL_EN.md) or copy the [plain-text description](proposals/2026-11-infrastructure-maintenance-corrected/SUBMISSION_EN.txt). Its reference is [proposal-2026-11-v1.0.1](https://github.com/pgarciagon/koinos-funding-proposal/releases/tag/proposal-2026-11-v1.0.1). The original [v1.0.0 release](https://github.com/pgarciagon/koinos-funding-proposal/releases/tag/proposal-2026-11-v1.0.0) remains available for #9. After the replacement is submitted, votes must be moved explicitly; the same work should be funded once.

## Adding a future proposal

1. Create a folder under `proposals/` named `YYYY-MM-topic`, using the proposed funding start month and a short topic.
2. Copy [the proposal template](templates/PROPOSAL_EN.md) into that folder and replace every placeholder.
3. Add `SUBMISSION_EN.txt` as a plain-text summary of at most 1,000 characters, including its full GitHub URL. Keep the scope, budget, dates, and commitments consistent with the formatted proposal. Preserve a full plain-text edition separately as `FULL_PROPOSAL_EN.txt` when useful.
4. Add a short `README.md` recording the status, proposed dates, amount, and links to both versions. Add a row to the index above.
5. Before submission, check the versions agree, refresh the conversion and fees, and confirm the beneficiary and dates. Freeze the final files in a new immutable release and use that versioned release URL in the summary. See the [KFS submission notes](docs/KFS_SUBMISSION.md).

Keep previous proposal folders and their links available. Once a proposal is submitted, record its KFS URL and the Git commit used for submission; distinguish later revisions from the submitted version. Do not overwrite an earlier proposal with a new funding request.

Publishing a draft here is separate from submitting it to the [Koinos Fund System](https://kfs.koinscan.com/submit). A repository entry does not indicate approval, funding, or guaranteed payments.

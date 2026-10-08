# Koinos Infrastructure Documentation and Community Maintenance

This replaces [KFS proposal #9](https://kfs.koinscan.com/projects/9) to start on October 15 and include the January payment. The scope, three-hour weekly commitment and 34,000 KOIN monthly request are unchanged. Please move support from #9 to this replacement so that the same work is funded once.

**Pablo Garcia · October 2026–January 2027 funding proposal · 34,000 KOIN per month**

Koinos needs reliable infrastructure, practical tools, clear documentation, and people who help others use them. I am requesting funding to dedicate **three hours every week** to that work: maintaining community services, improving node and bridge validator tooling, keeping our website and documentation useful, and helping developers and users move forward.

The expense budget for **October 15, 2026 through January 31, 2027** is **USD 2,271.94**: **46.71 planned contributor hours at USD 25/hour**, four USD 200 monthly Codex charges, and four USD 76.02 monthly infrastructure allocations. I request **34,000 native KOIN per scheduled payment**, or **136,000 KOIN across four payments**, preserving the original monthly request. At the original budgeting reference of USD 0.018/KOIN, that equals USD 2,448, including a USD 176.06 allowance for cost or conversion changes above the calculated expenses.

## About me

My name is **Pablo Garcia**, known in the community as **@pgarcgo** and on GitHub as **pgarciagon**. I have contributed to the Koinos community since its early years, starting with Spanish language education and community support and expanding into node operations, developer tools, documentation, and protocol fixes.

You can find me on the [Koinos team page](https://koinos.io/team), where I am listed as **Project Manager + Developer**, and in my [profile in the Koinos community history](https://koinos.io/history?person=person-pablo-garcia-pgarcgo#chronicle). My [GitHub profile](https://github.com/pgarciagon) provides further public references.

I maintain **koinos.io**, operate **seed.koinosfoundation.org**, and manage regular blockchain backups. I am also preparing updated documentation for **docs.koinos.io**, helping users, developers, and node operators find clear, practical guidance. These responsibilities connect the public face of Koinos with the infrastructure people need to join and use the network.

So far, I have carried out the work described here **without any remuneration**. I believe it is time to use the KFS to recognise and incentivise the time that community members invest in Koinos. Supporting these contributions can help turn volunteer effort into a sustainable, ongoing commitment. I also encourage other community members who invest their time and skills in the ecosystem to submit their own funding proposals.

## Work I have contributed

My contributions span several parts of the ecosystem. The following examples distinguish development, maintenance, reviews, and community work.

### Infrastructure and developer tools

- **Seed node operations and blockchain backups.** Operating community seed infrastructure and maintaining regular backups and recovery procedures. My [Koinos Backup Tools](https://github.com/pgarciagon/koinos-backup-tools) repository includes backup and restore scripts, checksums, metadata, and retention controls.
- **Teleno.** Development of an [experimental native Koinos node](https://github.com/koinos/teleno) that brings node services into one C++ binary, with observer and producer operation, APIs, and backup and restore tooling. The Koinos microservice node stack remains the reference implementation.
- **Koinos One.** Leading development of the [experimental desktop application](https://github.com/koinos/koinos-one) for operating a local Teleno node, inspecting the blockchain, and working with backups and recovery.
- **Knodel.** Development of an experimental desktop application for the **Koinos microservice node stack**, with native macOS service management, health and log diagnostics, a local blockchain explorer, wallet integration, and backup and restore workflows. It also serves as a local validation environment for upstream synchronization and state replay fixes.
- **Koinos Node Manager.** Developing [CLI and desktop tools for inspecting multiple nodes](https://github.com/pgarciagon/koinos-node-manager). Its implemented inspection surface is read-only; broader fleet lifecycle management remains further work.
- **Koinos testnet and faucet.** Work on [public testnet operations, endpoint documentation, monitoring, and the Telegram faucet](https://github.com/koinos/koinos-testnet), helping developers test without using mainnet funds.
- **kcli.** [Command line tooling](https://github.com/pgarciagon/kcli), including testnet support, token transfers, non-interactive wallet options, and producer dashboard and key tooling.
- **Upstream synchronization fixes.** Merged contributions to [receipt persistence in chain PR 858](https://github.com/koinos/koinos-chain/pull/858), [state delta replay in chain PR 861](https://github.com/koinos/koinos-chain/pull/861), and [tombstone preservation and pending Merkle roots in state database PR 36](https://github.com/koinos/koinos-state-db-cpp/pull/36).
- **Koinos microservice node stack maintenance.** [Service inventories and improvement proposals](https://github.com/pgarciagon/koinos_legacy_node) covering versions, dependencies, reproducibility, and operational validation.

### Supporting Eder's work on Vortex

I am supporting the outstanding work of **@ederaleng** on the Vortex bridge between Koinos and Ethereum, helping him prepare its next version. You can find him on [Telegram](https://t.me/ederaleng) and [GitHub](https://github.com/ederaleng).

**@ederaleng is the bridge's maintainer, owns its public domain, and will control the final public client and its release.** His sustained development and dedication are central to Vortex. My role is to support his work with technical review, testing, documentation, and operator tooling improvements.

- **Code review and reproducible tests.** Reviewing code, dependencies, build reproducibility, and fixes, and providing actionable findings and regression tests to support the next version.
- **Local transfer and recovery testing.** Exercising transfers and failure scenarios in isolated development environments to help identify issues and improve reliability.
- **Documentation and operator usability.** Helping improve instructions and supporting tools so that Eder's work is easier to review, test, and use.
- **Validator operation and a private Koinos API.** I plan to operate one of the validators in the final Vortex bridge network and set up a dedicated private Koinos API for that validator. This adds an operational contribution alongside my support for Eder's development. The budget includes two additional Hetzner VPS instances: a CPX32 at EUR 16.65 per month for the private Koinos API and a CX23 at EUR 6.53 per month for the validator. Activation will follow the bridge's release review and operator acceptance.

I plan to continue supporting the next version through scoped contributions aligned with Eder's priorities. Vortex will share the technical contribution allocation with the other projects in this proposal.

**I also encourage Eder to submit his own KFS proposal to fund the substantial hours and dedication he is investing in Vortex.** His work deserves recognition and sustainable support, and funding my supporting contributions should complement that recognition.

### Documentation and the public website

- **koinos.io.** Website maintenance, ecosystem research, project listings, and Spanish localization. Public examples include [ecosystem PR 144](https://github.com/koinos/koinos-io-website/pull/144), [Koinos AI PR 145](https://github.com/koinos/koinos-io-website/pull/145), and [Spanish localization PR 146](https://github.com/koinos/koinos-io-website/pull/146).
- **Koinos History.** Research and development of the interactive history, including the [merged website implementation](https://github.com/koinos/koinos-io-website/pull/142) and its [maintenance documentation](https://github.com/pgarciagon/koinos_history).
- **docs.koinos.io preparation.** Work on updating and organizing the documentation for new users, developers, and node operators, including Getting Started, Node Operators, Architecture, and Resources. The updated documentation site is **in preparation**. Public references include my [merged four chapter documentation contribution](https://github.com/koinos/koinos-docs/pull/238) and the independently maintained [community documentation edition](https://github.com/pgarciagon/koinos-docs), with architecture, microservice, and operator references.

### Reviews marketing and community support

- **Open Social.** A [published user review with testing evidence and coverage limits](https://github.com/pgarciagon/open_social_review), conducted on Harbinger testnet.
- **Community proposals.** [Independent comparative analysis](https://github.com/pgarciagon/koinos-proposal-analysis) of proposed changes, grounded in public sources and documented evidence.
- **Wallets and ecosystem applications.** Wallet testing and review, and Koinos AI installation and tutorial work. These are contributions to testing, usability, and review; they do not imply ownership of other contributors' products or a comprehensive security certification.
- **Official Spanish communication channels.** I manage the official [Koinos Spanish X/Twitter account (@koinos_espaniol)](https://x.com/koinos_espaniol) and the official [Spanish Telegram community (@koinoshispano)](https://t.me/koinoshispano), sharing updates, supporting the community, and making Koinos accessible to Spanish speakers.
- **Marketing and education.** [Community communication and campaign resources](https://github.com/pgarciagon/koinos_marketing), articles, technical explanations, ecosystem discovery, and bilingual onboarding. Earlier work included the Spanish community and the now discontinued Koincast podcast.
- **Community support.** Helping users and operators with nodes, wallets, testnet usage, backups, and troubleshooting, and turning recurring questions into reusable documentation.

## What this funding will deliver

This proposal funds a focused maintenance commitment across existing work. My weekly allocation will average:

| Work | Hours per week |
| --- | ---: |
| Seed and Vortex infrastructure, backups, and operational checks | 1 |
| Prioritized node, Vortex, or validator tooling work | 1 |
| Website and documentation maintenance | 0.5 |
| Community support | 0.5 |
| **Total** | **3** |

Urgent service issues may change the allocation, with service continuity taking priority.

During the funding period, I will aim to deliver:

1. **Continuity of seed services and regular backups**, with a weekly check of backup completion and service status, and a public summary of significant incidents.
2. **One documented recovery rehearsal** on an isolated test target, reporting the backup used, integrity checks, result, and remaining limitations.
3. **At least two scoped technical contributions**, such as fixes, tests, operator tooling, or reproducible investigation reports for Vortex, Teleno, Koinos One, Knodel, Node Manager, kcli, or the Koinos microservice node stack. Priorities will follow operational need; upstream acceptance is outside my control.
4. **At least three useful website or documentation updates**, including continued preparation of docs.koinos.io, focused on accurate project information, onboarding, node operation, and recovery.
5. **One brief update at the end of the funding period**, linking to completed work and outlining the next priorities. Progress will also remain visible through public repositories and website changes.

The initial October period will cover ongoing infrastructure and development tooling expenses, establish the service and backup baseline, prepare the Vortex validator and its private Koinos API, and select the highest value improvement. November and December will focus on the recovery rehearsal and further tooling and documentation work. January will complete the remaining scoped contributions and share the brief closing update.

Three hours per week is a bounded contribution commitment. It does not include a 24 hour incident response service or promise a full release of every project listed above.

## Budget and funding period

| Allocation across the full term | USD |
| --- | ---: |
| Contributor time: 109 days × 3 hours ÷ 7 × USD 25/hour | 1,167.86 |
| Codex development subscription: 4 × USD 200 | 800.00 |
| Existing Hetzner hosting, blockchain storage, backups, and infrastructure allowance: 4 × USD 50 | 200.00 |
| Vortex private Koinos API (CPX32): 4 × USD 18.69 | 74.76 |
| Vortex validator (CX23): 4 × USD 7.33 | 29.32 |
| **Total expense budget** | **2,271.94** |
| **Average expense per scheduled payment** | **567.98** |

The term spans **109 calendar days**, from October 15 inclusive to February 1 exclusive. At three hours per seven days, this is **46.71428571 planned hours**. Time is calculated over the actual funding period rather than four full months of work. Subscription and infrastructure expenses are budgeted as four monthly charges, including October. See the [calendar breakdown and calculation](BUDGET.md).

The subscription enables research, implementation, testing, documentation, and code review; I remain responsible for reviewing and validating the resulting work.

The infrastructure allowance is based on my existing Hetzner server at **EUR 14.27 per month**, with **8 vCPU, 16 GB RAM, 160 GB local disk, and a separately billed 200 GB volume**. The volume estimate is EUR 8.80 per month using the EUR 0.044 per GB rate displayed by [Hetzner](https://www.hetzner.com/cloud/block-storage/) when this budget was prepared. This gives approximately USD 25.90 per month before any additional taxes or services, at the [ECB reference rate of USD 1.1225 per EUR](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html) dated October 2, 2026. The USD 50 allowance leaves room for backup storage and related costs. It is an allowance, not a claim that the current invoice totals USD 50. The two additional Vortex VPS prices supplied for this proposal total EUR 23.18 per month, or approximately USD 26.02 at the same exchange rate. They are budgeted separately from the existing USD 50 allowance, bringing the combined infrastructure budget to USD 76.02 per month. The VPS figures are planning costs, not a claim that those services are already operating.

**Proposed term:** October 15, 2026 through February 1, 2027 at 00:00 UTC. The work covers the second half of October 2026 through January 2027; the end date is after the scheduled January 31 payment.

**Requested monthly payment:** 34,000 native KOIN. **Requested total across four scheduled payments:** 136,000 native KOIN, assuming all four are paid in full. This is 34,000 KOIN more than the original intended three-payment total of 102,000 KOIN. At USD 0.018/KOIN, the requested total is USD 2,448: the USD 2,271.94 expense estimate plus a USD 176.06 allowance for cost or conversion changes. This allowance does not represent additional contributor hours. The KFS does not prorate the October payment for a mid-month start; this proposal requests four equal payments to cover the term as a whole.

The conversion uses **USD 0.018 per KOIN** as a budgeting reference, based on the [vKOIN and USDC market on Base](https://dexscreener.com/base/0x9b61660Cb1a6920E9c912570cD210020B956F34E) observed on October 3, 2026. That is a wrapped token market price, not a guaranteed native KOIN sale price. Exchange rates, liquidity, fees, and price movement can change the realized USD amount. The original reference is retained for continuity with proposal #9; it is not asserted to be the current market price. The submitted KOIN amount is fixed for the term unless a separate proposal changes it. KFS payments depend on votes, ranking, and available fund balance, as explained in the [KFS documentation](https://kfs.koinscan.com/docs).

This request covers future work during the proposed term. The KFS submission fee is separate and will be confirmed by the form before submission.

## Why support this proposal

A working seed node helps another operator connect. A usable backup helps recover a service. A clear guide helps a developer get started. A practical desktop tool helps someone run their own node. Careful Vortex testing and usable validator tools help prepare the connections between Koinos and other networks. Each contribution makes Koinos easier to use and sustain.

Your vote would give this work a predictable budget, a defined weekly commitment, and a public record of delivery. I bring existing responsibilities, public contributions, and continuity across infrastructure, software, documentation, and community support.

**If you want Koinos to remain accessible to new users, developers, and independent node operators, I would appreciate your vote. Together, we can keep the services running and make the next contributor's first step easier.**

# Commons Protocol — Token and Funding Layer
### Design document v0.1 / internal / not for publication

---

## Purpose of this document

The founding document establishes that the consensus signal must be unmonetised and unmonetisable — structurally, not merely by promise. It also acknowledges that infrastructure costs something: servers, development, translation review, security audits, and the ongoing governance work the protocol requires. These two facts create a design challenge: how is the infrastructure funded without the funding mechanism becoming a vector for corrupting the signal it supports?

This document proposes a token-based funding layer that addresses this challenge. It is architecturally and documentarily separate from the signal layer. The token never touches the consensus mechanism. It circulates only within the governance of the infrastructure itself — the metabolic layer of the organism, not its nervous system.

---

## The biomimetic framing

The founding document introduces ATP — adenosine triphosphate — as the design model for the protocol's economic architecture. ATP is the universal energy currency of all living cells. It is not accumulated. It is not owned. It flows to where it is needed, is consumed in use, and is continuously regenerated. No cell hoards it. No organ outranks another in its right to receive it.

This document applies that model precisely. The token described here — provisionally called the Commons Energy Unit, or CEU, pending a naming decision — is designed to function as ATP for the protocol's infrastructure layer:

- It flows to contributors who do verified work maintaining the protocol
- It is consumed when used to participate in infrastructure governance decisions
- It is non-accumulative — units not used within a defined period are redistributed to the contributor pool
- It cannot be exchanged for anything outside the protocol ecosystem
- It confers no ownership, no permanent advantage, and no claim on the protocol's outputs

The token is energy, not wealth. This distinction is absolute and must be structural, not aspirational.

---

## What the token is for

The token has exactly one function: participation in governance of the protocol's infrastructure layer.

Infrastructure governance decisions include:
- Allocation of funding to development priorities (new features, security audits, accessibility improvements)
- Selection and renewal of infrastructure providers (hosting, translation services, security)
- Compensation rates for contributor roles (translation reviewers, framing editors, governance panel participants)
- Protocol upgrade proposals that affect the infrastructure layer but not the founding principles

Infrastructure governance decisions explicitly exclude:
- Any decision affecting the consensus signal layer
- Any decision affecting the question elevation process
- Any decision affecting the founding principles
- Any decision that would give token holders preferential treatment in the participation tiers

The boundary between infrastructure governance and signal governance is the most important design constraint in this document. It must be technically enforced, not merely stated.

---

## How tokens are created

Tokens are not pre-minted and sold. They do not exist before the work that earns them. This is the primary structural defence against speculation — there is no initial supply to buy, no token generation event, no founding allocation to early investors.

Tokens are created exclusively through verified contribution to the protocol's infrastructure. Contribution types that generate tokens:

**Translation work:** Verified translation of questions, evidence records, and protocol documents into languages not yet covered. Compensation rate determined by infrastructure governance vote, denominated in CEU.

**Framing review:** Human editorial review of questions at the global tier for neutrality and cultural accuracy. Reviewers are drawn from the verified participant pool and compensated per completed review.

**Governance panel participation:** Randomly selected reviewers who serve on elevation panels as described in the governance sketch. Participation is compensated to ensure that serving on a panel does not impose an uncompensated cost on participants, which would systematically exclude those who cannot afford unpaid time.

**Code contribution:** Verified development work on the open-source protocol codebase, reviewed and merged by the stewardship group. Compensation rate determined by infrastructure governance vote.

**Security audit contribution:** Verified participation in protocol security reviews, including bug reporting above a defined severity threshold.

**Stewardship:** Verified custodial work on the canonical documents — reviewing proposed changes, maintaining version records, responding to contributor questions. Compensated at a rate determined by infrastructure governance vote.

All contribution types are verified before token generation. Verification mechanisms mirror the tiered access model — contribution claims are reviewed by existing verified contributors, with random panel review for disputed claims above a defined threshold.

---

## How tokens are spent

Tokens are spent by casting votes in infrastructure governance decisions. Each governance decision is an open proposal in the repository, with a defined voting period and a defined token cost to cast a vote.

The token cost to vote is the same for all participants regardless of how many tokens they hold — this is the one-human-one-voice principle applied to infrastructure governance. Holding more tokens does not buy more votes. It buys more opportunities to participate in more decisions, which is appropriate — active contributors should have more say in infrastructure decisions than passive ones — but it does not buy louder votes in any single decision.

Proposals pass when a defined threshold of participating token holders vote in favour, weighted by participation tier rather than token quantity. A Steward's vote carries the same weight as a Participant's vote in infrastructure governance — the difference is eligibility, not weight.

Unspent tokens are redistributed on a rolling 90-day cycle. Any tokens held for more than 90 days without being spent are returned to the contributor pool for redistribution to active contributors. This enforces the non-accumulative principle structurally — hoarding tokens is not merely discouraged, it is mechanically futile.

---

## How infrastructure is funded externally

The token circulates internally among contributors. But infrastructure has real-world costs — servers, legal fees, security audits — that require real-world currency. The bridge between the token economy and real-world funding works as follows:

**Grants and institutional funding:** Foundations, civil society organisations, and academic institutions that wish to support the protocol's infrastructure can do so through direct grants denominated in conventional currency. Grant funds are held in a transparent, auditable account governed by the stewardship group. Expenditure decisions above a defined threshold require an infrastructure governance vote. Grantors receive no tokens, no governance rights, and no influence over the signal layer.

**Contributor token exchange:** Contributors who have earned tokens through verified work may, at defined intervals, exchange a portion of their tokens for conventional currency at a rate set by the infrastructure governance vote. This is the only point at which tokens convert to external value. The exchange rate is not market-determined — it is set by the community that earned the tokens, and it is capped to prevent any single contributor from extracting disproportionate value. This is the mechanism by which contributors are compensated in real terms for real work, without creating a speculative market.

**The exchange cap:** No contributor may exchange more than a defined maximum of tokens per quarter for conventional currency. This cap is set by infrastructure governance vote and is designed to ensure that compensation is meaningful — enough to cover the time cost of contribution — without being extractive. Contributors who accumulate tokens beyond the exchange cap simply have more governance participation capacity, not more wealth.

---

## Structural defences against speculation

The primary risk to the ATP model is that tokens, once they exist, find their way onto secondary markets where they trade speculatively. This would immediately corrupt the non-accumulative principle and create exactly the concentration dynamic the design is meant to prevent. The structural defences are:

**No secondary market listings:** The token is not designed for or listed on any cryptocurrency exchange. This is not a promise — it is a technical constraint. The token standard used should not be compatible with standard exchange listing protocols. Custom token standards or non-transferable token implementations are the appropriate technical choice.

**Non-transferability between participants:** Tokens cannot be transferred between participant accounts. They can only be created through verified contribution and destroyed through governance participation or the 90-day redistribution cycle. A token cannot be sold, gifted, or inherited. It is personal to the contributor who earned it and expires if unused.

**No founding allocation:** There is no pre-mine, no founder's allocation, no early investor pool. The people who design the token system receive tokens the same way everyone else does — by doing verified work. This removes the primary incentive for speculative accumulation at launch.

**Open supply visibility:** The total supply of tokens in circulation at any time is publicly visible. Any anomalous accumulation — a single contributor holding a disproportionate share — is immediately detectable and triggers an automatic governance review.

---

## Relationship to the signal layer

The signal layer — the consensus mechanism, the question elevation process, the verified participant votes — has no contact with the token layer. Specifically:

- Holding tokens does not increase a participant's voting weight in the consensus signal
- Holding tokens does not grant access to higher participation tiers — tier access is determined by verification status, not token holdings
- The token cannot be used to promote, elevate, or suppress any question
- The token cannot be used to influence framing review outcomes — framing reviewers are compensated in tokens for their work, but the compensation does not vary based on the outcome of their review

The separation is enforced technically, not by policy. The two systems are architecturally distinct — different smart contracts or protocol layers, with no shared state between them.

---

## Relationship to existing models

**Gitcoin** is the closest existing model — a platform for funding open-source development through community grants, with a quadratic funding mechanism that weights contributions by number of contributors rather than amount. The Commons Protocol token layer shares Gitcoin's instinct that infrastructure should be funded by the community it serves, not by investors seeking returns. The critical difference is that Gitcoin's GTC token has traded speculatively on secondary markets, which the ATP constraint prohibits. The non-transferability and non-listability constraints described above are the structural responses to this known failure mode.

**Faircoin** was an attempt to create a non-speculative, cooperative-governed currency. It achieved genuine community governance but ultimately could not prevent secondary market trading. The lesson: technical non-transferability is more reliable than community agreement not to trade.

**SourceCred** developed an algorithm for measuring contribution to open-source projects and distributing rewards accordingly. Its grain token was designed for internal use but faced similar secondary market pressures. Relevant prior art for the contribution verification mechanism.

---

## What this document does not resolve

**The token standard:** What technical implementation makes non-transferability and non-listability structurally enforceable rather than merely promised? Soul-bound tokens (SBTs), as proposed by Vitalik Buterin et al. in 2022, are the most relevant existing concept — non-transferable tokens bound to a single wallet identity. Their implementation for this use case requires technical input from blockchain developers familiar with SBT standards.

**The exchange rate mechanism:** Setting the token-to-currency exchange rate by governance vote creates a potential for the rate to be set in ways that serve active contributors at the expense of the protocol's long-term funding. What constraints on the exchange rate mechanism prevent this?

**The grant governance problem:** External grant funding is governed by the stewardship group with community oversight above defined thresholds. But grantors often have conditions — reporting requirements, scope restrictions, preferred outcomes — that could subtly shape protocol development even without formal governance rights. How are grant conditions assessed for compatibility with the founding principles before acceptance?

**The contributor compensation equity problem:** Contributors in high-income countries and contributors in low-income countries earn the same tokens for the same work — but the real-world value of the exchange rate is radically different for each. A rate that provides meaningful compensation in one context may be negligible in another, or conversely may make the exchange rate unsustainably expensive for the protocol. How is geographic equity in compensation addressed?

**Legal classification:** Depending on jurisdiction, the token described here — even with non-transferability constraints — may be classified as a security or a form of compensation subject to tax and employment law. Legal review is required before any implementation. The contributor token exchange mechanism in particular requires careful legal structuring.

---

## Invitation for critique

This document is offered to collaborators with expertise in token economics, cooperative governance, open-source funding models, and blockchain technical architecture. The most useful responses are: identified failure modes in the non-accumulation mechanism, technical implementations of non-transferable tokens that have been tested at scale, existing cooperative or commons funding models that address the equity problem more elegantly, and legal structures that have successfully navigated the security classification question in comparable contexts.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

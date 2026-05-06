# Commons Protocol — Tiered Access Specification
### Design document v0.1 / internal / not for publication

---

## Purpose of this document

This document consolidates and formalises the tiered access model described across the verification sketch, governance sketch, and token and funding layer documents. It provides a single authoritative reference for the five participation tiers, their verification requirements, their participation rights, the mechanisms for moving between tiers, and the conditions under which tier status may be suspended or revoked.

This document assumes familiarity with the verification sketch and governance sketch. References to those documents are functional rather than explanatory.

---

## Design principles governing the tier model

Three principles from the founding document directly shape this specification:

**One human, one voice.** Tier level does not affect the weight of a participant's signal in the consensus layer. A Steward's vote on a question carries identical weight to an Observer's engagement with the same question. Tiers govern access and responsibility, not influence over the signal.

**No central authority.** Tier transitions are governed by objective, published criteria and community verification processes. No individual or organisation has unilateral authority to grant, deny, or revoke tier status outside the defined processes.

**Equitable access.** The lowest tiers must be accessible to the broadest possible global population, including those without reliable internet, government-issued identification, or financial resources. Verification requirements scale with the consequence of participation, not as barriers to entry.

---

## The five tiers

---

### Tier 1 — Observer

**Description:** The entry point for the global majority. Read-only access to all protocol content at all levels. No participation in signal, governance, or contribution processes.

**Verification requirement:** None. No registration, no data submission, no account creation required.

**Participation rights:**
- Read all questions at all tiers (local, regional, global)
- Read all evidence records and their community classifications
- Read all governance proposals and their outcomes
- Read all protocol documents including this specification
- Read all question output records and historical signal data

**Participation restrictions:**
- Cannot vote on or engage with any question
- Cannot submit sources to evidence records
- Cannot raise questions at any tier
- Cannot participate in infrastructure governance
- Cannot earn or spend CEU

**Transition to Tier 2:** Any Observer may initiate Tier 2 registration at any time through any of the verified pathways described in the verification sketch. There is no waiting period, no eligibility requirement, and no cost.

**Notes:** The Observer tier is permanent and irrevocable — no action by any participant or steward can remove a person's ability to access the protocol at Observer level. This is the irreducible floor of the one-human-one-voice principle: everyone can see the signal, regardless of whether they can participate in producing it.

---

### Tier 2 — Participant

**Description:** The primary participation tier for the global majority of active users. Full access to local tier question engagement and evidence record contribution.

**Verification requirement:** Pseudonymous registration plus one of the following verified pathways (as specified in the verification sketch):
- Social vouching by one existing verified Participant, Proposer, Reviewer, or Steward
- Completion of a proof-of-personhood verification (BrightID, Proof of Humanity, or equivalent)
- Device-based zero-knowledge proof registration

Multiple pathways exist to ensure accessibility across different contexts and risk levels. No pathway requires government-issued identification.

**Participation rights:**
- All Observer rights
- Vote on questions at the local tier
- Submit sources to evidence records at the local tier
- Classify and contest source classifications at the local tier
- Vouch for new Tier 2 applicants (subject to vouching limits — see below)
- Earn CEU through verified contribution at eligible rates
- Spend CEU in infrastructure governance votes

**Vouching limits:** A Tier 2 participant may vouch for a maximum of five new Tier 2 applicants per 180-day period. This limit exists to slow the propagation of fraudulent identity networks. The limit resets automatically at the end of each 180-day period.

**Participation restrictions:**
- Cannot raise questions at any tier
- Cannot vote on regional or global tier questions
- Cannot participate in framing review
- Cannot serve on governance panels

**Transition to Tier 3:** A Tier 2 participant becomes eligible for Tier 3 after meeting all of the following objective criteria:
- Minimum 90 days active at Tier 2
- Minimum 20 verified engagement actions at the local tier (votes, source submissions, or classifications)
- No active conduct flags (see Conduct and suspension below)
- Completion of full verification if not already completed at Tier 2 (i.e., if Tier 2 was accessed via lightweight pathway, full proof-of-personhood or equivalent is required before Tier 3 eligibility)

Transition is initiated by the participant and confirmed by automatic criteria check. No human approval is required if criteria are met.

**Tier demotion:** A Tier 2 participant may be demoted to Tier 1 (Observer) only under the conduct provisions described below. Demotion is not permanent by default — see reinstatement provisions.

---

### Tier 3 — Proposer

**Description:** The tier at which participants may raise questions and nominate questions for regional consideration. The primary creative tier of the protocol.

**Verification requirement:** Full verification as defined in the verification sketch — proof-of-personhood protocol completion, social vouching by multiple existing verified participants, or device-based zero-knowledge proof, with at least two independent verification signals.

**Participation rights:**
- All Tier 2 rights
- Raise questions at the local tier
- Nominate questions for regional tier consideration
- Vote on questions at the regional tier
- Submit sources to evidence records at the regional tier
- Contribute to framing review processes at the regional tier
- Vouch for new Tier 2 and Tier 3 applicants (subject to vouching limits)
- Earn CEU at Proposer-eligible rates, which are higher than Tier 2 rates reflecting greater contribution responsibility

**Vouching limits:** A Tier 3 participant may vouch for a maximum of ten new Tier 2 applicants and three new Tier 3 applicants per 180-day period.

**Participation restrictions:**
- Cannot serve on global tier governance panels (reserved for Tier 4)
- Cannot participate in stewardship of canonical documents (reserved for Tier 5)

**Transition to Tier 4:** A Tier 3 participant becomes eligible for Tier 4 consideration after meeting all of the following criteria:
- Minimum 180 days active at Tier 3
- Minimum 10 verified contribution actions at Tier 3 level (question proposals, regional nominations, framing review contributions)
- Demonstrated quality of contribution — at least 3 proposed questions that have received positive community engagement, or equivalent contribution record as assessed by automatic quality metric (methodology published)
- No active conduct flags
- Explicit opt-in to the Tier 4 random selection pool (participation at Tier 4 involves time commitment that must be consented to)

**Important:** Transition to Tier 4 is not automatic on meeting criteria. It requires opt-in to the selection pool. Tier 4 participants are drawn randomly from the eligible pool when panels are required — meeting the criteria makes a participant eligible for selection, not selected.

---

### Tier 4 — Reviewer

**Description:** The tier from which governance panel members are randomly selected. Reviewers serve on elevation panels, conduct review panels, and evidence record dispute panels as described in the governance sketch. This is the protocol's primary human judgement layer.

**Verification requirement:** Met automatically on eligibility — no additional verification beyond Tier 3 requirements. The additional requirement is opt-in consent to panel service and the time commitment it involves.

**Participation rights:**
- All Tier 3 rights
- Eligibility for random selection to governance panels
- Vote on global tier questions
- Submit and classify sources in evidence records at the global tier
- Contribute to framing review at the global tier
- Earn CEU at Reviewer-eligible rates, which reflect the time cost of panel service

**Panel service obligations:** When randomly selected for a panel, a Tier 4 participant is expected to complete their panel role within the defined timeframe (as specified in the governance sketch). Repeated failure to complete panel service after selection results in temporary removal from the selection pool, not tier demotion. The selection pool is voluntary — a participant may withdraw from it at any time and return to Tier 3 participation without penalty.

**Participation restrictions:**
- Cannot participate in stewardship of canonical documents (reserved for Tier 5)
- Cannot unilaterally make protocol decisions — all Tier 4 action is through panel processes

**Transition to Tier 5:** Tier 5 stewardship positions are not transitioned into through automatic criteria. They are filled through a community nomination and selection process described below.

---

### Tier 5 — Steward

**Description:** The custodial tier. Stewards tend the canonical documents — the founding document, this specification, and the design documents — in service of the founding principles. They are gardeners, not owners. Their authority is procedural, not substantive: they maintain the version record, receive and review proposed changes, and ensure the governance processes described in all design documents are operating correctly. They have no authority to change the founding principles unilaterally.

**Verification requirement:** All Tier 3 and Tier 4 verification requirements met. Additionally: nomination by at least three existing Tier 4 or Tier 5 participants, confirmation by community vote open to all Tier 3 and above participants, and explicit acceptance of the stewardship obligations described below.

**Selection process:** When a Steward position is vacant or the community determines that additional Stewards are needed, a nomination period of 30 days opens. Any eligible participant may be nominated by others or may self-nominate. Nominees must have been active at Tier 4 for a minimum of 90 days. Following the nomination period, a 14-day community vote open to all Tier 3 and above participants determines which nominees are confirmed. Confirmation requires a simple majority of participating voters. There is no minimum quorum — the community's engagement with the selection is itself a signal of the legitimacy of the outcome.

**Stewardship obligations:**
- Maintain the canonical repository and version record
- Review proposed changes to protocol documents against the founding principles
- Respond to contributor questions and issues within a defined response window
- Publish an activity log at defined intervals, visible to all participants
- Recuse from any stewardship decision in which they have a declared personal interest

**Participation rights:**
- All Tier 4 rights
- Custodial access to the canonical repository
- Participation in stewardship decisions by consensus among active Stewards
- Earn CEU at Steward-eligible rates

**Steward term and renewal:** Stewards serve in rolling terms of 12 months. At the end of each term, a Steward must be re-confirmed by community vote to continue. Re-confirmation follows the same process as initial confirmation. A Steward who is not re-confirmed returns to Tier 4 without penalty.

**Maximum steward count:** The number of active Stewards at any time should be sufficient to ensure continuity but small enough to maintain accountability. The working recommendation is a minimum of three and a maximum of seven. This range is itself subject to revision by community governance.

---

## Conduct, suspension, and reinstatement

### Conduct flags

A conduct flag is raised against a participant when a verified complaint is submitted by another participant alleging a specific violation of the protocol's principles or processes. Conduct flags are not raised for disagreement, unpopular questions, or minority positions — only for verifiable procedural violations.

Grounds for a conduct flag include:
- Submitting knowingly false information to an evidence record
- Vouching for a participant known to be a duplicate identity
- Coordinated manipulation of question engagement patterns
- Abuse of the framing review process to introduce bias
- Impersonation of another participant

A conduct flag triggers a review by a randomly selected panel of five Tier 4 participants, drawn from a pool excluding the complainant and the subject of the complaint. The panel has 14 days to review the evidence and reach a determination. Deliberations are published (with participant identities pseudonymised). The determination is final subject to one appeal.

### Suspension

A participant found in violation of conduct standards is suspended from their current tier for a defined period:
- First violation: 30-day suspension to Tier 1 (Observer)
- Second violation: 180-day suspension to Tier 1
- Third violation: Permanent removal from participation tiers above Tier 1

Suspension does not affect a participant's ability to access the protocol at Observer level. The permanent floor of read-only access is inviolable.

### Reinstatement

A suspended participant automatically returns to their previous tier at the end of the suspension period, provided no new conduct flags have been raised during the suspension. Reinstatement is automatic — no application or approval required. CEU balances are frozen during suspension and restored on reinstatement, subject to the 90-day redistribution cycle (any CEU that would have expired during suspension expires as normal).

### Appeal

A participant may appeal a conduct determination within 14 days of the determination being published. Appeals are reviewed by a second randomly selected panel of five Tier 4 participants, drawn from a pool excluding all members of the original panel. The appeal panel's determination is final.

---

## What this document does not resolve

**The participation-quality tradeoff.** This is the central democratic tension in the tier model and it is named here explicitly rather than glossed over. Functional democracy requires individual responsibility and informed self-determination — not delegation, not passive consumption, but active engagement by people who have made some effort to understand what they are engaging with. The verification requirement at Tier 2, however low its barrier, is a threshold. It asks something of participants that passive social media consumption does not. That is by design: the signal is only as meaningful as the effort behind it. A consensus record produced by people who have done nothing to establish their participation means less than one produced by people who have. But this has real consequences. Every threshold, however low, systematically excludes some portion of the population — those with the least time, the least connectivity, the least familiarity with digital processes, the least trust in any system that asks them to register for anything. These are frequently the populations most directly affected by the questions the protocol is designed to surface. The tier model partially addresses this through multiple verification pathways and the permanent Observer floor — but it does not resolve the tension. The tradeoff between signal quality and participation breadth is a known and unresolved problem in democratic theory. This protocol does not solve it. It makes a specific design choice — prioritising signal integrity over frictionless participation — and names that choice honestly. Future iterations should continue to seek ways to lower the effective barrier without compromising the one-human-one-voice principle.

**The quality metric for Tier 3 to Tier 4 transition.** The specification refers to an "automatic quality metric" for assessing contribution quality. The methodology for this metric is not yet defined. It must be designed to reward genuine contribution without creating perverse incentives — for example, a metric that rewards the number of questions proposed would incentivise low-quality proposals. Design input from behavioural economists and community platform designers is needed.

**The quorum question.** Community votes for Steward confirmation have no minimum quorum in this specification. This is philosophically consistent — participation is an expression of community engagement — but practically it means a Steward could theoretically be confirmed by a very small number of votes if broader participation is low. Whether a minimum quorum is needed, and how it is set without creating deadlock, is an open design question.

**Tier access for communities with intermittent connectivity.** The offline verification problem identified in the verification sketch has downstream effects on tier access. A participant who cannot complete proof-of-personhood verification due to connectivity constraints is limited to Tier 2 via social vouching. The implications for their long-term participation pathway need further design attention.

**The founding steward question.** The protocol needs at least one Steward from inception to maintain the canonical repository and seed the first community. The selection process described above assumes an existing community from which nominees can emerge. Before that community exists, a founding steward or stewardship group must be identified through a different process. How the founding stewards are selected, and how their legitimacy is established before a community exists to confirm them, is an open design question with direct relevance to the current stage of the project.

---

## Invitation for critique

This specification is offered to collaborators with expertise in community platform design, governance systems, and behavioural economics. The most useful responses are: identified edge cases in the transition criteria, conduct processes that would fail under adversarial conditions, quality metrics that have been successfully implemented in comparable contexts, and the founding steward problem — which is the most immediately practical open question in this document.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

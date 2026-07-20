# Commons Protocol — Governance Sketch
### Design document v0.3 / internal / not for publication

---

## Purpose of this document

The founding document describes *what* the question elevation process must achieve: surfacing genuine cross-cultural consensus without being captured by noise, ideology, or well-resourced advocacy groups. This document sketches *how* that might work in enough mechanical detail to invite serious technical and governance critique.

This is a thinking document, not a specification. Every mechanism described here is provisional. The goal is to demonstrate that the problem has been thought through, not to foreclose better solutions.

---

## The three failure modes to design against

Any open question-elevation system faces three distinct failure modes, and most existing systems optimise against one while inadvertently enabling another:

**Failure mode 1 — Gaming by coordination**
A well-resourced group — a government, a corporation, an advocacy network — mobilises its members to elevate a question that serves its interests, manufacturing the appearance of cross-cultural grassroots concern. This is the astroturfing problem. It has compromised petition platforms, online polls, and Wikipedia edit histories.

**Failure mode 2 — Ideological capture**
A question that resonates strongly within one culturally homogeneous community — however large — reaches the global layer because that community is large and motivated, not because the concern is genuinely cross-cultural. The result is a global layer that reflects the priorities of the most organised communities rather than the most broadly shared concerns.

**Failure mode 3 — Bureaucratic stagnation**
Elevation thresholds are set so high, or review processes so slow, that the global layer never populates with anything current. The protocol becomes a pristine but empty architecture that serious participants abandon for more responsive alternatives.

A well-designed elevation mechanism must be resistant to all three simultaneously.

---

## The proposed mechanism: three-stage elevation with cryptographic verification

### Stage 1 — Local origination

Any verified participant may raise a question within their local community tier (approximately 150 members, as described in the founding document). Questions at this stage are unmoderated beyond basic content filtering — no committee decides whether a question is worthy. The only requirement is that it is a genuine question, not a statement, a petition, or a call to action.

Questions live at the local tier for a minimum of **30 days** before becoming eligible for elevation consideration. This cooling period prevents reactive or manufactured urgency from driving premature elevation.

A question becomes eligible for regional consideration when it meets the following objective threshold within its local community:

- A minimum of **60% of verified local participants** have engaged with it (not necessarily agreed — engagement includes dissent, which is itself a signal of relevance)
- Engagement has come from participants whose verified identity metadata indicates **at least three distinct cultural or geographic backgrounds** within the local community

This second criterion is the first anti-gaming filter: a question that resonates only within a culturally homogeneous local group cannot elevate, regardless of how many people engage with it.

---

### Stage 2 — Regional resonance

A question that meets the local threshold is submitted to a **regional resonance pool** — a collection of questions from multiple local communities across a defined geographic or linguistic region.

Elevation from regional to global requires demonstrating resonance across **genuinely distinct** local communities. Specifically:

- The question must have met the local threshold in a minimum of **five local communities**
- Those five communities must represent at least **three distinct language groups**
- Those five communities must represent at least **three distinct geographic regions** as defined by a neutral geographic classification system (UN geoscheme or equivalent)
- The pattern of engagement must show **temporal independence** — meaning the spikes of engagement in different communities must not be suspiciously synchronised, which would suggest coordinated promotion

The temporal independence criterion is the primary defence against coordinated astroturfing. Genuine cross-cultural resonance tends to spread organically with natural time lags between communities. Manufactured resonance tends to show simultaneous spikes across communities that would not otherwise be in contact.

This pattern analysis is handled algorithmically, with the methodology published and open to external audit.

---

### Stage 3 — Global review and framing

A question that meets the regional threshold does not automatically enter the global layer. It enters a **global review queue** where two things happen in parallel:

**Framing review:** The question is examined for neutrality of language. This is not ideological review — the question is not assessed for whether it is a good question, only whether its phrasing contains embedded assumptions, leading language, or culturally specific framings that would make it inaccessible or biased for a global audience. This review is conducted by a small panel drawn from a standing pool of volunteer reviewers who have demonstrated linguistic and cultural range. Their role is purely editorial, not substantive.

**Random panel review:** A randomly selected panel of **twelve verified participants** — drawn from across geographic and cultural regions, with no two panel members from the same region — reviews the question for one purpose only: to confirm that the elevation process was followed correctly and that no obvious gaming has occurred. This panel has no power to reject a question on substantive grounds. They can only send it back to the regional tier if they identify a procedural violation, with a documented reason that is published publicly.

Random selection rather than appointed review eliminates the capture risk inherent in standing committees. No one can lobby a randomly selected panel they don't know in advance.

If the framing review and random panel review both clear, the question enters the global layer within **14 days** of entering the review queue.

---

## Participant verification — the identity problem

The entire mechanism above depends on verified human participants. This is the hardest problem in the design, and this document does not claim to solve it — it identifies the constraints any solution must satisfy and sketches candidate approaches. See the verification sketch design document for a fuller treatment.

---

## Appeal and contestation

Any elevation decision — including a panel's decision to return a question to the regional tier — must be contestable. The appeal process is:

1. Any verified participant may file a formal objection to an elevation decision within **21 days** of the decision being published
2. Objections must specify which procedural criterion was violated — objections on substantive grounds (disagreement with the question itself) are not valid appeals
3. Valid objections trigger a second random panel review of **five participants**, drawn from a different pool than the original panel
4. The second panel's decision is final for that version of the question — though a modified version of the question may re-enter the process from the local tier

All objections, panel compositions (anonymised), deliberations (where possible), and decisions are published in the public record. Transparency of process is the primary defence against perception of bias.

---

## Gaming detection and response

Beyond the temporal independence criterion described above, the following mechanisms address gaming:

**Velocity limits:** A single local community may not submit more than three questions to the regional pool within any 90-day period. This prevents a captured community from flooding the regional tier.

**Vouching accountability:** If a participant who vouched for others is found to have participated in coordinated gaming, their vouching history is flagged and reviewed. This creates accountability upstream in the social graph.

**Pattern publication:** All engagement data — timing, geographic distribution, community composition — is published in anonymised form for each question in the elevation process. External researchers and journalists can audit the data for gaming patterns independently. Open data is a stronger anti-gaming mechanism than any internal process.

**Gaming detection triggers fast-track elevation:** If coordinated gaming is confirmed for a specific question, the question is fast-tracked for elevation review regardless of where it sits in the normal process. Confirmed suppression attempts are themselves evidence of a question's significance — the protocol treats them as such. The actors confirmed to have coordinated the gaming attempt are subject to account suspension as described in the tiered access specification. This inverts the incentive structure entirely: attempting to suppress a question through gaming accelerates rather than delays it.

---

## Custodian selection, accountability, and succession

The founding document states that those who tend the protocol are custodians, not authors. This section specifies what that means in practice — how custodians are chosen, what they are accountable for, how they are removed, and how succession works. This is the governance layer most vulnerable to capture, and the one that every commons system in history has most frequently failed to protect. It requires more structural rigour than any other element of this design.

**What custodians do — and do not do**

Custodians tend the canonical founding document and protocol specification. They do not determine which questions are elevated. They do not set policy. They do not speak for the protocol in public. Their role is specifically and only: to receive proposed improvements to the design documents, review them against the founding principles, incorporate what strengthens the design, and maintain the version record. Any custodian who attempts to exercise substantive authority beyond this remit is acting outside their role and subject to removal.

**Selection**

Custodians are nominated by verified participants who have reached the Steward tier through demonstrated participation history. Nomination requires endorsement from participants across at least three distinct regional groupings — no nomination from a single culturally or geographically homogeneous group is valid. No self-nomination. No appointment by existing custodians without community endorsement. The selection process is published and contestable.

The founding steward problem — how the first custodian cohort is selected before the participant community exists — is a genuine bootstrapping challenge. The initial custodian cohort must be self-selecting by necessity, but their selection must be documented transparently and treated as provisional, subject to ratification by the first sufficiently diverse verified participant community.

**Terms and rotation**

Custodian terms are fixed at two years, non-renewable without a minimum one-year cooling-off period. No custodian may serve consecutive terms. Rotation is mandatory. Succession is managed by the outgoing custodian cohort in conjunction with a randomly selected participant panel — custodians do not unilaterally choose their successors.

**Accountability**

All custodian decisions — every revision accepted or rejected, every version change, every procedural determination — are published with reasoning. The version history is permanent and publicly auditable. Custodians may be publicly questioned by any verified participant. Responses are published.

The custodian layer uses a two-tier accountability structure: internal peer accountability within the custodian cohort, and external community accountability. Custodians review each other's decisions. The community reviews the cohort's overall conduct. Neither layer alone is sufficient — internal peer review catches specific errors; community oversight catches systematic drift. Both are required.

**Removal**

Any verified participant may initiate a removal process against a custodian. The initiating participant must specify which procedural principle was violated — removal on grounds of substantive disagreement with a custodian's editorial judgement is not a valid basis for removal. Valid removal grounds include: acting outside custodian remit, failure to publish reasoning for decisions, conflict of interest not disclosed, or demonstrated coordination with external interests contrary to the founding principles.

A valid removal petition triggers a review by a randomly selected panel of fifteen verified participants drawn from at least five distinct regional groupings. Removal requires a supermajority — at least ten of fifteen panel members. Removed custodians may not be renominated for five years.

**Collective bad faith — the hardest case**

The removal mechanism above handles individual custodian failures. The harder case is collective custodian bad faith — where the entire custodian cohort acts in coordination against the founding principles. No internal accountability mechanism addresses this because the accountability mechanism is itself captured.

The mitigation is structural rather than procedural: the founding document is published under a Creative Commons licence that allows any person or group to fork the document and establish a competing canonical version. The protocol cannot be owned, and a captured custodian cohort cannot prevent a legitimate alternative from emerging. Community legitimacy — which version participants treat as canonical — is the ultimate check on custodian capture. A captured version loses participants to the legitimate alternative.

This is an imperfect solution. It requires the community to recognise capture and act on it. But it is the most structurally honest answer available: stated boundaries erode; structural boundaries hold. The fork mechanism is the structural boundary of last resort.

**Compensation**

Custodians receive compensation through the Commons Energy Unit model described in the token funding layer document — non-transferable, non-speculative, earned through verified ongoing custodial work. The compensation model is itself subject to community governance: custodian remuneration is determined through the same transparent, contestable process the protocol uses for other governance decisions. This is the recursive self-application principle: the protocol governs its own resource allocation using its own methodology, turning the funding problem from a vulnerability into a demonstration of the protocol working.

---



The following questions remain open and require input from people with relevant technical, legal, and governance expertise:

- **Jurisdiction:** The protocol operates across legal jurisdictions with conflicting laws on speech, privacy, and political organisation. Where is it legally domiciled, if anywhere? What is its legal exposure if a question in the global layer defames a specific entity or government?

- **Infrastructure funding:** Who pays for the computational infrastructure required to run the verification and pattern-detection systems? The founding document establishes that the signal must be unmonetised, but the servers, the developers, and the reviewers cost something. A funding model that does not compromise signal independence is developed provisionally in the token and funding layer design document.

- **AI governance:** The framing review and pattern detection both involve AI systems. Those systems carry biases inherited from their training data — a translation model trained predominantly on English-language text will carry English-language framings into other languages; a bias-detection model trained on mainstream sources will treat challenges to institutional consensus as suspicious. How are the AI systems governed, audited, and corrected over time?

- **Bootstrap problem:** The social vouching model requires existing verified participants to vouch for new ones. How does the network reach sufficient scale that the vouching graph is meaningfully diverse from the outset, rather than reflecting the demographics of whoever discovers the protocol first?

- **Languages not yet covered:** Automated translation at the quality required for neutral framing review does not yet exist for all of the world's major languages. What is the protocol's responsibility to language communities it cannot yet serve equitably?

---

## Invitation for critique

This sketch is offered to collaborators as a starting point for rigorous challenge. The most useful responses to this document are not endorsements but objections — specific mechanisms that would fail in identified ways, constraints that have been overlooked, prior art in governance design that addresses these problems more elegantly.

The goal is not to defend this design but to arrive, through open critique, at a design robust enough to build.

---

*Version 0.3 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

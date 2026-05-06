# Commons Protocol — Governance Sketch
### Design document v0.1 / internal / not for publication

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

The entire mechanism above depends on verified human participants. This is the hardest problem in the design, and this document does not claim to solve it — it identifies the constraints any solution must satisfy and sketches candidate approaches.

**The constraints:**

A verification system must confirm that each participant is a unique human being without:
- Creating a centralised database of personal identity information that can be hacked, sold, or subpoenaed
- Requiring government-issued identification, which excludes the undocumented, the stateless, and those in repressive regimes where disclosure of identity is dangerous
- Relying on biometric data, which raises severe and well-founded civil liberties concerns
- Being so burdensome that it excludes the populations most affected by the issues the protocol is designed to surface

**Candidate approaches:**

*Social graph vouching:* New participants are vouched for by existing verified participants, up to a defined limit per voucher. This is the model used by Keybase and by some Mastodon instances. It scales organically, requires no central database, and creates accountability within communities. Its weakness is that it can bootstrap closed communities if early adopters vouch only within their existing networks.

*Proof of personhood protocols:* Projects including Proof of Humanity, BrightID, and Idena have developed cryptographic approaches to establishing unique human identity without centralised identity data. Each has trade-offs in terms of accessibility and attack surface. These are worth examining as candidate infrastructure rather than reinventing the problem.

*Progressive trust:* Participants begin with limited participation rights and earn fuller participation through demonstrated engagement over time. This raises the cost of Sybil attacks (creating multiple fake identities) without requiring upfront identity verification. Its weakness is that it disadvantages new participants who have the most urgent concerns.

*Device-based verification with privacy preservation:* Using device fingerprinting combined with zero-knowledge proofs to confirm that a participation signal comes from a unique device without revealing what that device is or who owns it. Technically complex but preserves privacy most completely.

The founding principle is that no single approach is sufficient. A layered approach — combining social vouching for early participants, progressive trust accumulation, and cryptographic uniqueness proofs — is likely more robust than any single mechanism. This layering is itself an open design question.

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

**Cooling periods after gaming detection:** If coordinated gaming is confirmed for a specific question, that question is ineligible for re-submission for **180 days**. This removes the incentive to attempt gaming as a delay tactic.

---

## What this document does not resolve

The following questions remain genuinely open and require input from people with relevant technical, legal, and governance expertise:

- **Jurisdiction:** The protocol operates across legal jurisdictions with conflicting laws on speech, privacy, and political organisation. Where is it legally domiciled, if anywhere? What is its legal exposure if a question in the global layer defames a specific entity or government?

- **Infrastructure funding:** Who pays for the computational infrastructure required to run the verification and pattern-detection systems? The founding document establishes that the signal must be unmonetised, but the servers, the developers, and the reviewers cost something. A funding model that does not compromise signal independence is yet to be designed.

- **AI governance:** The framing review and pattern detection both involve AI systems. Those systems have biases, and those biases will shape what reaches the global layer. How are the AI systems governed, audited, and corrected over time?

- **Bootstrap problem:** The social vouching model requires existing verified participants to vouch for new ones. How does the network reach sufficient scale that the vouching graph is meaningfully diverse from the outset, rather than reflecting the demographics of whoever discovers the protocol first?

- **Languages not yet covered:** Automated translation at the quality required for neutral framing review does not yet exist for all of the world's major languages. What is the protocol's responsibility to language communities it cannot yet serve equitably?

---

## Invitation for critique

This sketch is offered to collaborators as a starting point for rigorous challenge. The most useful responses to this document are not endorsements but objections — specific mechanisms that would fail in identified ways, constraints that have been overlooked, prior art in governance design that addresses these problems more elegantly.

The goal is not to defend this design but to arrive, through open critique, at a design robust enough to build.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

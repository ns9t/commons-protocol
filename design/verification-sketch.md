# Commons Protocol — Verification Sketch
### Design document v0.3 / internal / not for publication

---

## Version notes

v0.3 incorporates a second round of feedback from Adam Stallard (BrightID/Updraft founder), adding detail on Aura's layered internal review structure — supervisor roles, peer evaluation within teams, and rapid de-authorisation — distinguishing this from the shallower, necessary-but-insufficient role of community-level oversight.

v0.2 incorporated his first round of substantive critique. Specific changes from v0.1: BrightID Aura referenced as more relevant prior art than original BrightID verification model; behavioural characteristics approach flagged as incompatible with no-central-authority principle and de-emphasised accordingly; participation history as uniqueness signal identified as gameable and removed as a verification criterion; skilled verifier cadre model incorporated as a candidate approach to anomaly detection; social recovery added as key recovery recommendation.

---

## The problem

Every existing verification system solves the uniqueness problem by knowing who you are. Governments issue identity documents. Platforms collect email addresses and phone numbers. Financial institutions require passports and proof of address. All of them trade privacy for certainty — they can confirm you are a unique individual because they know which individual you are.

This protocol cannot follow that model, for a reason that is not merely philosophical but structural: the populations most urgently needing a voice in this system are precisely the people most harmed by identity disclosure requirements. The stateless, the undocumented, dissidents in repressive regimes, indigenous communities without state recognition, people living under governments that would use participation records against them — these are not edge cases. They are a significant portion of the global population, and in many instances they are the people most directly affected by the questions this protocol is designed to surface.

A verification system that excludes them does not merely fail ethically. It fails the protocol's founding principle of equal voice regardless of geography, wealth, or status. It would produce a global signal that systematically underrepresents the most vulnerable and overrepresents the most documented — which is precisely the distortion the protocol exists to correct.

The design challenge is therefore: **certainty without disclosure**. Proof that a participant is a unique human being, without proving which human being they are.

This is a hard problem. It is not, however, an unsolved one.

---

## The constraints any solution must satisfy

Before examining candidate approaches, the constraints are worth stating explicitly, because any solution that violates them — however technically elegant — is not a valid solution for this protocol.

**Must confirm uniqueness.** The system must make it computationally difficult or economically irrational for any participant to register as more than one verified identity. Without this, the one-human-one-voice principle is hollow.

**Must not require government-issued identification.** This immediately excludes the stateless and undocumented, and in repressive regimes it creates a disclosure record that can be subpoenaed or hacked and used against participants.

**Must not create a centralised identity database.** A central store of verified identities is a single point of failure — for hacking, for state subpoena, for commercial acquisition. The protocol's infrastructure principle requires that no single entity can be compelled to produce a list of participants.

**Must not rely on biometric data as a centralised store.** Biometric verification is technically robust for uniqueness but creates the most sensitive possible centralised database. Once compromised, biometric data cannot be changed. The civil liberties exposure is severe and permanent.

**Must be accessible without a smartphone, reliable internet, or financial resources.** Verification systems that require a recent smartphone model, consistent connectivity, or a credit card exclude the populations the protocol most needs to include.

**Must be resistant to state-level interference.** A government that wished to suppress participation from its population should not be able to do so by blocking a single verification server or service.

**Verification must beat inference.** A critical principle learned from eight years of real-world implementation at BrightID: verification by vouching — where a voucher has genuine skin in the game — is more robust than inference from behaviour patterns or participation history. Behavioural analysis can be automated and gamed; an attacker can learn to mimic honest behaviour patterns more effectively than honest participants can maintain them. Reputation-staked vouching creates accountability that automation cannot replicate.

---

## Candidate approaches

No single approach satisfies all constraints. The proposal developed in this document is a layered model — combining multiple mechanisms so that the failure or compromise of any one does not collapse the whole, and so that participants can verify through whichever pathway is accessible to them.

### Approach 1 — Social graph vouching with skin in the game

New participants are vouched for by existing verified participants, up to a defined limit per voucher. Crucially, vouchers must have meaningful skin in the game — their own verified status, their participation reputation, and in the skilled verifier model described below, their livelihood, is staked on the accuracy of their vouching.

**How it works:** A verified participant vouches for a new participant, staking a portion of their participation reputation on the claim that this is a real, unique person they have genuine social knowledge of. Each verified participant can vouch for a limited number of new participants per period, creating accountability. If a vouched participant is later found to be a duplicate or fraudulent identity, the vouching participant's reputation is affected.

**BrightID Aura model:** Adam Stallard, founder of BrightID, notes that BrightID's newer Aura verification system is closer to this model than the original BrightID verification party approach. Aura uses a small cadre of skilled, motivated verifiers — approximately 1% of participants — who have genuine reputational and livelihood stakes in the accuracy of their verifications. A small team of skilled verifiers can verify an entire offline village. They have significant incentive not to inflate numbers or misrepresent participants, because their reputation as verifiers is their primary asset. This model directly addresses the bootstrapping problem, the offline verification problem, and the anomaly detection problem simultaneously. It is the most field-tested approach available and should be treated as the primary model rather than one option among several.

**On the bootstrapping problem:** Aura suffered from the same bootstrapping problem as original BrightID — the network begins with whoever discovers it first, and early demographics shape the vouching graph. Deliberate seeding across culturally and geographically diverse starting communities is required. This is a known challenge, not an unknown one.

**Strengths:** No central database. Scales organically. Works without a smartphone for the vouching act itself. Culturally familiar. Particularly strong for communities where physical co-presence is possible. The skilled verifier model adds robustness without centralisation.

**Weaknesses:** Bootstrap problem. Requires careful seeding. The skilled verifier cadre must itself be verified and incentivised correctly from inception.

---

### Approach 2 — Proof of personhood protocols

Several projects have developed cryptographic approaches to establishing unique human identity without centralised identity data.

**BrightID (original model)** — a social graph-based system in which participants join verification parties (video calls with groups of strangers) and mutually confirm each other's humanness. Identity is a cryptographic keypair; no personal data is stored.

**BrightID Aura** — the newer vouching-based system described above. More relevant to this protocol's needs than the original verification party model.

**Proof of Humanity** — combines a video submission with a social vouching layer and a challenge mechanism. Anyone can challenge a registration they believe to be fraudulent, with a dispute resolution process.

**Idena** — requires participants to pass simultaneous AI-resistance tests at scheduled intervals. Because tests happen simultaneously worldwide, a single human cannot pass the test for multiple identities at once.

**Strengths:** Cryptographically robust. No central database. BrightID Aura in particular is designed for exactly the use case this protocol requires, with eight years of field experience behind it.

**Weaknesses:** All currently require internet connectivity. Idena's simultaneous testing model creates timezone accessibility issues. None has achieved global scale. BrightID verification parties require video calls, which may be dangerous for participants in repressive regimes.

**Role in layered model:** Proof of personhood protocols, particularly BrightID Aura, are the strongest available mechanism for participants with reliable internet access. They should be supported as a primary verification pathway.

---

### Approach 3 — Device-based verification

**Important revision from v0.1:** The original sketch proposed device-based verification using behavioural characteristics. Adam Stallard's critique correctly identifies a structural problem with this approach: behavioural analysis implies a centralised actor capable of adjudicating uniqueness, because only a centralised actor can enforce the security-by-obscurity needed for behavioural analysis. This is directly incompatible with the protocol's no-central-authority principle, and is prone to internal abuse by any centralised actor entrusted with this function.

The revised position is: device-based behavioural analysis is not a valid verification approach for this protocol. It is removed as a primary pathway.

What remains valid from the device-based approach is **cryptographic device commitment without behavioural analysis** — a participant's device generating a cryptographic commitment during registration that is unique to that registration but reveals nothing about behaviour, identity, or device characteristics. This is technically complex, requires further development, and is more appropriately treated as a research direction than a candidate implementation approach.

---

### Approach 4 — Progressive trust with verified onboarding

Rather than requiring full verification before any participation, this approach begins with minimal barriers and increases participation rights as verification is completed.

**Important revision from v0.1:** The original sketch suggested that demonstrated participation history could serve as a signal of uniqueness in the progressive trust model. Adam Stallard's critique identifies this as a significant vulnerability: participation history is exactly the kind of signal that can be automated, giving a systematic advantage to attackers who can learn which behaviours to mimic better than honest participants can maintain them. Verification — vouching by someone with genuine skin in the game — beats inference from activity patterns.

**The revised progressive trust model therefore separates two things that were conflated in v0.1:** access levels (which can increase progressively based on participation) and verification status (which must be established through genuine vouching or proof of personhood, not inferred from behaviour). Participation history may unlock access tiers, but it does not substitute for verification and should not be used as a uniqueness signal.

**Strengths:** Zero barrier to entry for the vast majority of the global population. Reduces the bootstrap problem by allowing engagement to precede full verification.

**Weaknesses:** The transition between lightweight and full verification requires careful calibration.

**Role in layered model:** The progressive trust model is the architecture within which the other approaches operate. It determines when each level of verification is required, not how that verification is performed.

---

## The layered model proposed

Combining the above, the proposed verification architecture is:

**Observer tier:** No verification. Read-only. Zero barrier globally.

**Participant tier (local voting):** Social vouching by an existing verified participant, or completion of a proof-of-personhood verification (BrightID Aura or equivalent). Multiple pathways ensure accessibility. Behavioural inference is not a valid pathway at any tier.

**Proposer tier (raising and nominating questions):** Fuller verification required — BrightID Aura completion, or social vouching by multiple existing verified participants. At least two independent signals required.

**Reviewer and Steward tiers:** Full verification plus demonstrated participation history (for access purposes, not as a uniqueness signal). Selected through community processes; not self-nominated.

---

## Anomaly detection and the skilled verifier model

**Revised from v0.1:** The original sketch proposed that randomly selected verified participants could detect anomalies such as clusters of recently verified identities all vouching for each other. Adam Stallard's critique is direct and experience-based: randomly selected participants are not going to be motivated or skilled enough for this. BrightID learned this from experience, and it was the driving factor in creating the Aura verification method.

The revised approach is a **skilled verifier cadre** — approximately 1% of participants who have demonstrated commitment to the protocol's integrity, have significant reputational stakes in accurate verification, and are specifically equipped and incentivised to detect and flag anomalous patterns. These verifiers may use AI tools to assist with pattern detection. They are not random; they are selected and maintained through a reputation-based process.

This creates a tension with the protocol's anti-capture principle: a standing cadre of skilled verifiers with significant influence over the verification layer is a potential capture point. The resolution is transparency, accountability, and — critically — a layered internal review structure rather than reliance on community oversight alone.

In BrightID Aura, the relevant unit is not the individual verifier but the **Aura team** — a cadre of skilled verifiers operating in a given domain (unique humans, insurance claims, regulatory compliance). Within each team, supervisor roles ("trainer," "manager") evaluate other team members, in the same way that Aura participants evaluate the subjects they verify. These supervisor roles are open to anyone, exactly like the base verifier role, and are governed by the same skin-in-the-game principle: a supervisor who does a poor job, or attempts to exploit their position, can be rapidly de-authorised by other established participants, reversing the evaluations of a compromised verifier quickly.

The community's role is broader but shallower — providing general consent and confidence that a given Aura team is performing well, which is necessary but not sufficient for catching specific failures. The specific, granular evaluation of verifier quality happens inside the team structure, among peers with direct visibility into each other's work. This is expert-evaluating-expert, not crowd-evaluating-expert. Teams have a structural incentive toward accuracy and honesty because their legitimacy — and their members' continued ability to participate — is conferred by the community accepting their evaluations over time.

Adapted to the Commons Protocol, the skilled verifier cadre should be structured the same way: not a flat pool of individually accountable verifiers subject only to outside community review, but teams with internal supervisor roles, peer evaluation, and rapid de-authorisation capability — with community-level transparency and consent operating as the outer layer of accountability, not the only layer. Capture is harder to sustain when there are two independent layers of scrutiny, internal and external, rather than one.

The middle-man problem — corrupt or captured verifiers stealing votes or other benefits — is much easier to detect and block than to bypass. Uncovering such problems is itself aligned with the Commons Protocol's purpose of bringing to light discrepancies between what people want and what actually happens. The protocol's transparency principle applies to its own verification layer as much as to the questions it surfaces.

---

## Key recovery

**Revised from v0.1:** The original sketch flagged key recovery as an open problem without a clear answer. Adam Stallard's suggestion is direct: **social recovery is the best recovery**. The same skilled, motivated verifiers who have a reputation to uphold can re-verify people they know if those people lose access to their cryptographic identity. This is the same community of trust that performs initial verification — extending it to recovery is natural and does not require creating a centralised recovery database.

This approach is consistent with the no-central-authority principle and draws on existing relationships rather than creating new infrastructure.

---

## The Sybil problem

A Sybil attack is the creation of multiple fake identities to manipulate a system that weights participants equally. No verification architecture eliminates it entirely. The goal is making Sybil attacks sufficiently costly, detectable, and low-yield that they are economically and practically irrational.

The layered model addresses this through:

- **Cost:** Each verification pathway requires genuine effort — social relationships, video presence, or cryptographic commitment — that scales linearly with the number of fake identities created.
- **Skin in the game:** Vouchers stake their own reputation on accuracy. Automated farming of fake identities requires corrupting real vouchers, not just generating fake activity.
- **Skilled detection:** The 1% verifier cadre, equipped with AI-assisted pattern detection, can identify anomalous vouching clusters that random participants would miss.
- **Yield limitation:** Even a successful Sybil attack at the local tier has limited consequence — local tier questions affect only the local community. Reaching the global signal layer requires demonstrated cross-cultural resonance that a coordinated inauthentic network cannot manufacture without becoming detectable.

---

## What this document does not resolve

- **Bootstrapping the skilled verifier cadre:** How are the first skilled verifiers identified, incentivised, and held accountable before the community exists to select them? This is the founding verifier problem and is directly related to the founding steward question in the tiered access specification.

- **The simultaneous test problem:** Idena's approach of simultaneous worldwide testing is the most Sybil-resistant mechanism known, but its accessibility constraints make it unsuitable as the sole pathway. A modified version more accessible without sacrificing its core property remains an open research question.

- **Offline verification at scale:** The skilled verifier model handles offline communities well at small scale. At large scale — verifying millions of participants across low-connectivity regions — the model needs further development. Physical community verification events are possible but require trusted local organisers who are themselves part of the verifier cadre.

- **The safety paradox:** Participants most in need of privacy protection — dissidents, activists, people in repressive regimes — are also those for whom video-based verification is most dangerous. The skilled verifier model may actually help here, since verification can happen in person rather than on camera. But the design of safe verification pathways for high-risk participants remains a priority challenge.

- **Legal exposure:** Operating any verification system may trigger regulatory requirements under GDPR, CCPA, or equivalent frameworks depending on jurisdiction. Legal review is required before any implementation.

---

## Invitation for critique

This document has benefited from substantive engagement from Adam Stallard (founder, BrightID) via the Metagovernance Project community. His eight years of field experience with proof-of-personhood systems have materially improved the design.

Further critique is invited, particularly from those with experience in: decentralised identity systems, Sybil-resistance in practice, offline community verification, and the governance of skilled verifier cadres in commons contexts.

The goal remains: arrive, through open critique, at a verification architecture robust enough to build.

---

*Version 0.3 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

# Commons Protocol — Verification Sketch
### Design document v0.1 / internal / not for publication

---

## The problem stated precisely

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

**Must not rely on biometric data as a centralised store.** Biometric verification — fingerprints, iris scans, facial recognition — is technically robust for uniqueness but creates the most sensitive possible centralised database. Once compromised, biometric data cannot be changed. The civil liberties exposure is severe and permanent.

**Must be accessible without a smartphone, reliable internet, or financial resources.** Verification systems that require a recent smartphone model, consistent connectivity, or a credit card exclude the populations the protocol most needs to include.

**Must be resistant to state-level interference.** A government that wished to suppress participation from its population should not be able to do so by blocking a single verification server or service.

---

## Candidate approaches

No single approach satisfies all constraints. The proposal developed in this document is a layered model — combining multiple mechanisms so that the failure or compromise of any one does not collapse the whole, and so that participants can verify through whichever pathway is accessible to them.

### Approach 1 — Social graph vouching

New participants are vouched for by existing verified participants, up to a defined limit per voucher. This model is used by some Mastodon instances, by the PGP web of trust, and in various forms by community-based organisations globally.

**How it works:** A verified participant vouches for a new participant, staking a portion of their participation reputation on the claim that this is a real, unique person they have genuine social knowledge of. Each verified participant can vouch for a limited number of new participants — perhaps five to ten over a defined period — creating accountability. If a vouched participant is later found to be a duplicate or fraudulent identity, the vouching participant's reputation is affected.

**Strengths:** Requires no central database. Scales organically. Works without a smartphone or internet connection for the vouching act itself. Is culturally familiar — humans have always established trust through social networks. Particularly strong in communities where physical co-presence is possible.

**Weaknesses:** The bootstrap problem — the network begins with whoever discovers it first, and their social graphs determine early demographic composition. A network that begins among English-speaking technologists will vouch in English-speaking technologists. Deliberate seeding across diverse starting communities is required to avoid this. Also vulnerable to tight-knit communities vouching for each other's duplicate identities if the reputation stake is insufficient.

**Mitigation:** Initial seeding partnerships with geographically and culturally diverse civil society organisations — literacy programmes, community health networks, indigenous rights organisations — who can establish verified local cohorts from the outset. Reputation stakes calibrated to make coordinated fraud economically irrational.

---

### Approach 2 — Proof of personhood protocols

Several projects have developed cryptographic approaches to establishing unique human identity without centralised identity data. The most relevant are:

**BrightID** — a social graph-based system in which participants join verification parties (video calls with groups of strangers) and mutually confirm each other's humanness. Identity is a cryptographic keypair; no personal data is stored. The system is designed to be Sybil-resistant — creating multiple fake identities requires attending multiple verification parties with different groups of strangers, which is detectable.

**Proof of Humanity** — combines a video submission with a social vouching layer and a challenge mechanism. Anyone can challenge a registration they believe to be fraudulent, with a dispute resolution process that does not require central adjudication.

**Idena** — requires participants to pass simultaneous AI-resistance tests (solving tasks that AI cannot currently solve) at scheduled intervals. Because tests happen simultaneously worldwide, a single human cannot pass the test for multiple identities at once.

**Strengths:** Cryptographically robust. No central database. BrightID and Idena in particular are designed for exactly the use case this protocol requires.

**Weaknesses:** All currently require internet connectivity and a smartphone or computer. Idena's simultaneous testing model creates timezone accessibility issues. None has achieved the scale required for a globally representative signal. BrightID verification parties require participants to interact with strangers in video calls, which may be dangerous for participants in repressive regimes.

**Role in layered model:** Proof of personhood protocols are the strongest available mechanism for participants with reliable internet access and no safety concerns about video presence. They should be supported as a verification pathway but cannot be the only pathway.

---

### Approach 3 — Device-based verification with zero-knowledge proofs

A zero-knowledge proof is a cryptographic method by which one party can prove to another that a statement is true without revealing any information beyond the truth of that statement. Applied to identity verification, a participant can prove "I am a unique human who has not previously registered" without revealing who they are, where they are, or what device they are using.

**How it works in practice:** A participant's device generates a cryptographic commitment during registration — a mathematical fingerprint of certain device and behavioural characteristics that is unique to that registration but reveals nothing about the underlying data. If the same participant attempts to register again from a different device, the system can detect the duplicate without knowing which human is involved.

**Strengths:** Maximum privacy preservation. No personal data transmitted or stored. Resistant to state-level surveillance. Compatible with the protocol's decentralised architecture.

**Weaknesses:** Technically complex to implement accessibly. Vulnerable to participants using genuinely different devices — a person with two phones could potentially register twice if device characteristics are the only signal. Requires active development work; no off-the-shelf implementation currently fits this use case precisely.

**Role in layered model:** The most appropriate mechanism for participants in high-risk environments where video presence or social graph exposure is dangerous. Should be developed as a priority pathway for this reason, even though it is technically the most demanding.

---

### Approach 4 — Progressive trust accumulation

Rather than requiring full verification before any participation, this approach begins with minimal barriers and increases participation rights as a participant demonstrates consistent, non-duplicative engagement over time.

**How it works:** A new participant begins at Observer tier — read-only, no verification required. To move to Participant tier and cast votes at the local level, they complete a lightweight registration that records a pseudonymous identifier and a small number of non-identifying behavioural signals. Full verification — through social vouching, proof of personhood, or device-based proof — is required only to move to Proposer tier and above.

**Strengths:** Zero barrier to entry for the vast majority of the global population. Dramatically reduces the bootstrap problem by allowing engagement to precede full verification. Makes the cost of Sybil attacks at the local tier low-consequence — a duplicate identity at the Observer tier changes nothing.

**Weaknesses:** Local tier votes cast before full verification are less trustworthy than fully verified votes. The transition point between lightweight and full verification requires careful calibration — too early and it becomes a barrier; too late and early-tier signal is unreliable.

**Role in layered model:** The progressive trust model is the architecture within which the other three approaches operate. It determines when each level of verification is required, not how that verification is performed.

---

## The layered model proposed

Combining the above, the proposed verification architecture is:

**Observer tier:** No verification. Read-only. Zero barrier globally.

**Participant tier (local voting):** Pseudonymous registration plus one of: social vouching by an existing verified participant, or lightweight behavioural device signal, or completion of a proof-of-personhood verification. Multiple pathways ensure accessibility across different contexts and risk levels.

**Proposer tier (raising and nominating questions):** Full verification required — either proof-of-personhood protocol completion, or social vouching by multiple existing verified participants, or device-based zero-knowledge proof. At least two independent signals required.

**Reviewer and Steward tiers:** Full verification plus demonstrated participation history. Selected randomly from the verified pool; cannot be self-nominated.

The layered approach means that no single verification mechanism is a single point of failure. Compromise of one pathway does not compromise the others. Participants in different circumstances — high-risk environments, low connectivity, distrust of video-based systems — can choose the pathway appropriate to them.

---

## The Sybil problem stated honestly

A Sybil attack is the creation of multiple fake identities to manipulate a system that weights participants equally. It is the primary attack vector against any one-human-one-voice system, and no verification architecture eliminates it entirely. The goal is not elimination but making Sybil attacks sufficiently costly, detectable, and low-yield that they are economically and practically irrational.

The layered model addresses this through:

- **Cost:** Each verification pathway requires genuine effort — social relationships, video presence, or cryptographic commitment — that scales linearly with the number of fake identities created.
- **Detection:** The temporal independence criterion in the governance sketch (genuine engagement spreads with natural time lags; coordinated manipulation shows synchronised patterns) applies to identity networks as well as question engagement. A cluster of recently verified identities all vouching for each other and immediately engaging with the same questions is a detectable anomaly.
- **Consequence:** Verified participants who vouch for fraudulent identities lose participation reputation. The social graph cost of systematic fraud is therefore borne by real participants, not just the fraudulent identities themselves.
- **Yield limitation:** Even a successful Sybil attack at the local tier has limited consequence — local tier questions affect only the local community. Reaching the global signal layer requires demonstrated cross-cultural resonance that a coordinated inauthentic network cannot manufacture without becoming detectable.

---

## What this document does not resolve

The following questions remain genuinely open:

- **The simultaneous test problem:** Idena's approach of simultaneous worldwide testing is the most Sybil-resistant mechanism known, but its accessibility constraints and timezone issues make it unsuitable as the sole pathway. Can a modified version of simultaneous testing be designed that is more accessible without sacrificing its core property?

- **Offline verification:** Large populations in sub-Saharan Africa, South and Southeast Asia, and rural communities globally have intermittent or no internet connectivity. What verification pathway is available to them? SMS-based systems exist but are vulnerable to state interception. Physical community verification events are possible but require trusted local organisers.

- **The safety paradox:** The participants most in need of privacy protection — dissidents, activists, people in repressive regimes — are also the participants most important to the protocol's claim to global representation. Video-based verification is inaccessible to them. Device-based zero-knowledge proofs are the best current answer but require significant development. This should be treated as a priority, not a deferred problem.

- **Key recovery:** If a participant's cryptographic identity is a keypair they generate and hold, losing access to that keypair means losing their verified identity. What recovery mechanism exists that does not recreate the centralised database problem?

- **Legal exposure:** Depending on jurisdiction, operating a verification system — even one that holds no personal data — may trigger regulatory requirements under GDPR, CCPA, or equivalent frameworks. Legal review is required before any implementation.

---

## Invitation for critique

As with the governance sketch, this document is offered to collaborators as a starting point for rigorous challenge. The most useful responses are specific objections: verification pathways that would fail in identified ways, attack vectors not addressed, prior art in identity systems that addresses these constraints more elegantly.

The goal is not to defend this design but to arrive, through open critique, at a verification architecture robust enough to build.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

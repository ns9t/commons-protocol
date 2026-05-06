# Commons Protocol — Evidence Record Design
### Design document v0.1 / internal / not for publication

---

## Purpose of this document

Every question in the Commons Protocol carries an attached evidence record — a structured collection of sources that participants can consult when forming their response. The founding document establishes that the protocol does not take positions; it ensures participants have access to the information needed to form their own. The evidence record is the mechanism through which that principle is operationalised.

This document examines what that mechanism must achieve, the constraints it must satisfy, the two primary design approaches and their trade-offs, and the central unresolved question that requires specialist input before any implementation decision can be made.

---

## Why the evidence record exists

The protocol's filter pyramid ensures that only questions with demonstrated cross-cultural resonance reach the global layer. But cross-cultural resonance is not the same as informed resonance. A question can spread widely through communities whose shared concern is genuine but whose access to relevant information is limited, distorted, or absent.

Without an evidence record, the global signal reflects what participants have been told by whatever information environment they happen to inhabit — which is, as the founding document notes, itself a product of structural amplification, commercial interest, and in some cases deliberate distortion. A signal produced under those conditions is not a measure of informed global conscience. It is a measure of existing information asymmetry.

The evidence record exists to partially correct that asymmetry — not by telling participants what to think, but by ensuring that verifiable, relevant information is accessible to anyone who wants it before they respond.

---

## The constraints any solution must satisfy

**Must not compromise the protocol's neutrality.**
The evidence record cannot become a mechanism through which the protocol takes a substantive position on the question it is attached to. Selecting sources is inevitably a curatorial act, and curation carries implicit endorsement. The design must minimise this risk while acknowledging it cannot be eliminated.

**Must be resistant to capture by well-resourced interests.**
Commercial and state actors with strong interests in particular question outcomes have both the motivation and the resources to attempt to shape evidence records in their favour — by submitting favourable sources, funding nominally independent research that meets formal credibility criteria, or challenging credible sources through procedural mechanisms. The design must make capture economically irrational and procedurally detectable.

**Must be accessible to participants with limited scientific or media literacy.**
A global protocol cannot assume that participants have the background to evaluate primary scientific literature, assess journalistic methodology, or navigate contested expert disagreement. The evidence record must be navigable by someone encountering a topic for the first time, without being so simplified that it misrepresents genuine complexity.

**Must be honest about the limits of established knowledge.**
In some domains — certain areas of medical research, environmental science, and economics among them — the formally established consensus has been shaped by commercial interests in ways that are themselves documented and contested. A credibility standard that defers entirely to formal peer review in these domains would reproduce rather than correct existing distortions. The design must acknowledge this without becoming a vehicle for unfounded contrarianism.

**Must be scalable.**
The protocol is designed for global adoption across thousands of questions in multiple languages. Any evidence record design that requires intensive human curation for every source submitted to every question will not scale. Automation and community participation must carry most of the load, with human expert review reserved for contested decisions.

---

## The central design question

Two primary approaches are possible, each with distinct trade-offs. This is the central unresolved question of this document, and it is named here explicitly as requiring specialist input from information scientists, librarians, epistemologists, and practitioners in the fact-checking and open knowledge communities before any implementation decision is made.

---

### Approach A — Protocol-defined credibility standards

The protocol establishes a set of credibility criteria. Sources that meet the criteria are included in the evidence record. Sources that do not are excluded. The determination is made by a governed review process operating against the published criteria.

**What the criteria might include:**
- Disclosed authorship with verifiable identity
- Disclosed methodology, open to independent replication
- No undisclosed commercial or political interest in the question outcome
- Published in a venue with independent editorial oversight
- Primary data or peer-reviewed analysis, not aggregation or commentary

**What an evidence record looks like under Approach A:**

Using the Amazon deforestation example from the founding document:

*Sources meeting the credibility threshold:*
- NASA satellite deforestation data, 2024 — primary scientific data, government agency, methodology published
- IPCC Sixth Assessment Report, forest carbon chapter — intergovernmental scientific body, peer-reviewed
- Brazilian National Institute for Space Research annual figures — government scientific agency
- Global Forest Watch annual report — independent non-profit, methodology published
- Financial Times investigative report on agricultural lobby influence on Brazilian forest policy — established international publication, named journalists, editorial oversight on record

*Sources submitted but not meeting threshold:*
- Agricultural industry association position paper — undisclosed commercial interest, no independent methodology
- Anonymous blog post — unverifiable authorship

**Strengths:**
Clean and navigable for participants. Reduces cognitive load. Makes the evidence record usable for participants with limited background. Creates a clear standard that bad-faith submissions can be measured against.

**Weaknesses:**
The credibility determination is made by someone, and that someone is capturable. Peer review has been demonstrably compromised in specific domains — pharmaceutical research, tobacco science, and agrochemical safety studies being documented cases where formally credentialed research served commercial rather than scientific interests. A standard that defers to peer review without qualification reproduces those distortions. The exclusion decisions are invisible to participants — they see only what passed, not what was considered and rejected, which limits their ability to contest the curation.

---

### Approach B — Community classification with open contestation

The protocol establishes a submission process but not a credibility standard. All submitted sources are visible to participants, classified by the submitting community according to a published taxonomy, and subject to open contestation. Participants see the sources, their classifications, and the degree of community agreement or disagreement about those classifications.

**What the taxonomy might include:**
- Source type (primary data / peer-reviewed analysis / investigative journalism / institutional position / advocacy / commercial / unclassified)
- Interest disclosure (no declared interest / declared interest / undisclosed interest suspected — with evidence)
- Methodology status (published and replicable / published not replicable / not published / not applicable)
- Community confidence rating (derived from participant classification responses)

**What an evidence record looks like under Approach B:**

*All submitted sources, with community classifications:*
- NASA satellite deforestation data — Type: Primary scientific data. Interest: No declared interest. Methodology: Published. Community confidence: 94% [based on 3,847 participant classifications, 12 contested]
- Brazilian Agricultural Confederation position paper — Type: Institutional/advocacy. Interest: Declared commercial interest. Methodology: Not published. Community confidence: 23% [2,103 classifications, 891 contested]
- IPCC Sixth Assessment Report — Type: Peer-reviewed analysis. Interest: No declared interest. Methodology: Published. Community confidence: 97% [4,102 classifications, 8 contested]
- Independent analysis challenging INPE methodology — Type: Peer-reviewed analysis. Interest: No declared interest declared. Methodology: Published. Community confidence: 61% [1,205 classifications, 340 contested — active dispute]

**Strengths:**
More consistent with the protocol's founding principles — no central authority determines what participants see. Contested science is visible as contested rather than silently excluded or included. Bad-faith sources are classifiable and contestable rather than simply excluded by an opaque process. The community confidence rating is itself a meaningful signal.

**Weaknesses:**
Significantly higher cognitive load for participants, particularly those without background in evaluating source types. Vulnerable to flooding — a well-resourced actor can submit large numbers of sources that technically meet submission criteria, diluting the record. The community classification process requires participant engagement that may be unrealistic at scale for every question. Contested classifications may never resolve, leaving participants with genuine uncertainty about which sources to trust.

---

## The hybrid model as working hypothesis

Given the trade-offs above, the working hypothesis for this protocol is a hybrid approach — combining a minimal baseline exclusion standard with an open classification and contestation process for everything above that baseline.

**The baseline standard** excludes only sources that are clearly and verifiably bad-faith by formal criteria:
- Anonymous authorship with no verifiable identity
- Undisclosed commercial or political interest where the interest is demonstrably material to the question outcome
- No methodology stated and none inferable from the source type
- Demonstrated fabrication (retracted papers, confirmed misinformation)

This baseline is deliberately narrow — it does not attempt to adjudicate contested science or exclude sources merely because they challenge established consensus. Its purpose is to remove obviously fraudulent material without prejudging genuinely disputed evidence.

**Above the baseline**, all submitted sources are visible with community classifications and confidence ratings, as in Approach B. Participants see the full record, the taxonomy, and the degree of community agreement. They make their own credibility judgements informed by that metadata.

**The baseline determination** is made by a governed review process — as in Approach A — but against criteria narrow enough that the decision space is minimised. The fewer decisions the governed process makes, the smaller the capture surface.

**Contested baseline decisions** — cases where a source's exclusion or inclusion under the baseline criteria is disputed — follow the same random panel review process described in the governance sketch: randomly selected reviewers, published deliberation, contestable outcome.

---

## The epistemic bias problem stated honestly

The hybrid model reduces but does not eliminate the most serious underlying problem: in certain domains, the formally credible information environment has itself been compromised by the interests the protocol is designed to hold accountable.

Documented cases include:
- Pharmaceutical industry funding of clinical trials, with selective publication of favourable results and suppression of unfavourable ones — documented extensively in Ben Goldacre's *Bad Pharma* (2012) and in the AllTrials campaign's findings
- Agrochemical industry funding of safety studies for products subsequently found to cause harm — Monsanto's suppression of glyphosate safety research being among the most extensively documented cases
- Tobacco industry funding of research designed to create the appearance of scientific uncertainty about established findings — documented in Naomi Oreskes and Erik Conway's *Merchants of Doubt* (2010)

In each of these cases, formally peer-reviewed research published in credentialed journals served commercial rather than scientific interests. A credibility standard that defers to peer review without qualification would include this research and exclude challenges to it that, while less formally credentialed, may be more accurate.

The protocol's first iteration operates within the limits of what it can verify, and those limits are explicitly acknowledged as a known limitation rather than a permanent position. The epistemic bias problem is named here as a major future design challenge — one that requires input from specialists in the sociology of science, evidence-based medicine, and the history of commercial influence on research — before it can be addressed in a subsequent version of this document.

For the first iteration, the hybrid model's narrow baseline standard provides partial protection: sources with documented commercial interest and no independent methodology will not pass the baseline regardless of their formal credentials. This does not solve the problem but it addresses its most egregious manifestations.

---

## Relationship to the question framing process

The evidence record does not exist in isolation. It is assembled in parallel with the question framing review described in the governance sketch — the process by which a question's language is assessed for neutrality before it enters the global tier.

The framing review and the evidence record assembly should be coordinated: sources submitted during the framing review process inform the initial evidence record, and the evidence record's composition may in turn reveal framing issues not caught in the initial review. A question whose submitted evidence record consists overwhelmingly of sources from one interest group is itself a signal that the question framing may require closer examination.

---

## What this document does not resolve

**The central unresolved question:** Should the protocol define credibility standards itself (Approach A), rely on community classification with open contestation (Approach B), or implement the hybrid model described above? This decision requires specialist input from:
- Information scientists and librarians with expertise in source classification systems
- Practitioners in the fact-checking community (IFCN-accredited organisations and their methodologists)
- Epistemologists with expertise in the sociology of scientific knowledge
- Practitioners in open knowledge communities (Wikipedia's editorial governance being the most relevant existing model, notwithstanding its known limitations in contested domains)

**Scalability of community classification:** The Approach B and hybrid models require participant engagement in source classification at a scale that has not been demonstrated in any existing platform. What incentive structures make this engagement sustainable? What does the classification process look like in practice for a participant encountering it for the first time?

**Language and cultural equivalence in source classification:** A source classified as "peer-reviewed" in one knowledge tradition may not map cleanly onto the same category in another. Indigenous knowledge systems, oral traditions, and community-held evidence do not fit the taxonomy described above. How are these accommodated without either excluding them or misrepresenting their epistemological status?

**The retraction and correction problem:** Scientific consensus changes. Investigative reporting is sometimes wrong and sometimes corrected. How does the evidence record update when a previously included source is retracted, corrected, or superseded? Who is responsible for monitoring source status over time?

**The first-mover problem:** Whoever submits sources to an evidence record first shapes its initial composition. Early submissions from well-resourced actors may establish a baseline that is difficult to contest even with the classification process in place. How is the first-mover advantage neutralised?

---

## Invitation for critique

This document is offered to collaborators — particularly those with expertise in information science, evidence evaluation, and the governance of open knowledge systems — as a starting point for rigorous challenge. The central design question is explicitly unresolved and requires exactly the kind of specialist input this document cannot provide.

The most useful responses are: specific mechanisms that would fail in identified ways, domains where the hybrid model's baseline standard would produce known distortions, existing classification systems in open knowledge communities that address these constraints more elegantly, and precedents — successful or failed — in evidence governance that bear on this design.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

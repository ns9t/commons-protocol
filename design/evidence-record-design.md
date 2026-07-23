# Commons Protocol — Evidence Record Design
### Design document v0.2 / internal / not for publication

---

## Version notes

v0.2 incorporates three rounds of specialist input not available at v0.1: Adam Stallard's (BrightID/Updraft founder) architecture for decentralised expert evaluation combined with crowd wisdom accountability; Anton Parf's (Anthosphere) observation that reputation systems without an ontological grounding cannot guarantee ethical outcomes; and the Anthosphere audit series finding that the expert panel problem as framed in v0.1 may be unsolvable within a centralised architecture. The response to these inputs is a third design approach — the distributed evaluation model — which supersedes the hybrid model as the primary working hypothesis, while retaining the hybrid model as a fallback for contexts where the distributed infrastructure is not yet available.

---

## Purpose of this document

Every question in the Commons Protocol carries an attached evidence record — a structured collection of sources that participants can consult when forming their response. The founding document establishes that the protocol does not take positions; it ensures participants have access to the information needed to form their own. The evidence record is the mechanism through which that principle is operationalised.

The protocol does not claim that its evidence records contain objective truth. They contain the best available verified information at a given moment, assembled through a process designed to resist capture and open to ongoing contestation. That is a more honest and more defensible claim.

---

## Why the evidence record exists

The protocol's filter pyramid ensures that only questions with demonstrated cross-cultural resonance reach the global layer. But cross-cultural resonance is not the same as informed resonance. A question can spread widely through communities whose shared concern is genuine but whose access to relevant information is limited, distorted, or absent.

Without an evidence record, the global signal reflects what participants have been told by whatever information environment they happen to inhabit — which is itself a product of structural amplification, commercial interest, and in some cases deliberate distortion. A signal produced under those conditions is not a measure of informed global conscience. It is a measure of existing information asymmetry.

The evidence record exists to partially correct that asymmetry — not by telling participants what to think, but by ensuring that verifiable, relevant information is accessible to anyone who wants it before they respond.

---

## The constraints any solution must satisfy

**Must not compromise the protocol's neutrality.**
The evidence record cannot become a mechanism through which the protocol takes a substantive position on the question it is attached to. Selecting sources is inevitably a curatorial act, and curation carries implicit endorsement. The design must minimise this risk while acknowledging it cannot be eliminated.

**Must be resistant to capture by well-resourced interests.**
Commercial and state actors with strong interests in particular question outcomes have both the motivation and the resources to attempt to shape evidence records in their favour. The design must make capture economically irrational and procedurally detectable.

**Must be resistant to capture at the evaluator level.**
Any system that relies on expert evaluators must address the possibility that the evaluators themselves are captured — either by direct interest or by institutional affiliation with interests that shape their judgement. This is the problem the Anthosphere audit identified as potentially unsolvable within a centralised architecture. The distributed evaluation model addresses it by ensuring no single evaluator or team controls the outcome.

**Must carry an ontological grounding.**
As Anton Parf observed: reputation systems without an ontological grounding cannot guarantee ethical outcomes. An expert evaluator with high reputation scores who evaluates evidence in service of anti-life policies is not a trustworthy evaluator for this protocol. The evidence record framework must specify not just formal credibility criteria but the values against which evidence is assessed — the Commons Protocol's founding principles serve as this grounding.

**Must be accessible to participants with limited scientific or media literacy.**
A global protocol cannot assume that participants have the background to evaluate primary scientific literature, assess journalistic methodology, or navigate contested expert disagreement. The evidence record must be navigable by someone encountering a topic for the first time.

**Must be honest about the limits of established knowledge.**
In some domains, the formally established consensus has been shaped by commercial interests in ways that are themselves documented and contested. The design must acknowledge this without becoming a vehicle for unfounded contrarianism.

**Must be scalable.**
Any evidence record design that requires intensive human curation for every source will not scale. Automation and community participation must carry most of the load, with human expert review reserved for contested decisions.

---

## Three approaches

### Approach A — Protocol-defined credibility standards

The protocol establishes credibility criteria. Sources that meet them are included; sources that do not are excluded. The determination is made by a governed review process.

**Strengths:** Clean and navigable. Reduces cognitive load. Creates a clear standard.

**Weaknesses:** The credibility determination is made by someone, and that someone is capturable. Peer review has been demonstrably compromised in specific domains. The exclusion decisions are invisible to participants.

*Role in current design:* Approach A criteria inform the baseline exclusion standard in the distributed model below. They are not sufficient on their own.

---

### Approach B — Community classification with open contestation

Sources are submitted openly and classified by community participants according to a published taxonomy. All sources are visible with their classifications and community confidence ratings.

**Strengths:** No central authority determines what participants see. Contested science is visible as contested. Bad-faith sources are classifiable and contestable.

**Weaknesses:** High cognitive load. Vulnerable to flooding. May not scale. Contested classifications may never resolve.

*Role in current design:* The community layer of the distributed model below incorporates Approach B's contestation mechanism, but adds expert evaluation and crowd wisdom accountability as additional layers.

---

### Approach C — Distributed evaluation model (primary working hypothesis)

This approach incorporates the architecture described by Adam Stallard (BrightID/Updraft) and addresses the evaluator capture problem identified by the Anthosphere audit. It operates across three layers:

**Layer 1 — Expert evaluation teams (Aura)**
Multiple independent teams of skilled evaluators assess evidence sources against the Commons Protocol evaluation rubric (see below). Teams operate within the Aura protocol — a decentralised system in which evaluators within each team assess each other's work, with supervisor roles able to rapidly de-authorise compromised evaluators. Multiple competing teams provide resilience: if one team is captured, others continue operating.

Teams are not assigned to fixed domains. Evaluators develop specialisation organically — the system learns what each evaluator is good at and routes relevant cases to them. This means "ecological evidence records" and "humanitarian evidence records" are not separate siloed domains but natural specialisations that emerge from evaluator behaviour.

Each team operates under a publicly acknowledged guiding document — the Commons Protocol evidence record framework (this document) — which specifies what trustworthy evidence means in this context. Teams cannot set rules that contradict this framework. The framework is the ontological grounding that prevents high-reputation evaluators from serving anti-protocol interests.

**Layer 2 — Crowd wisdom accountability (Updraft)**
The public votes on which Aura teams are trustworthy, using Updraft's crowd wisdom mechanism. Early, accurate assessments of team trustworthiness are financially rewarded; attempts to distort the public assessment lose money to honest assessors. This layer holds the expert teams publicly accountable without requiring every member of the public to have expert knowledge.

Teams with the highest public confidence are ranked at the top of the Updraft campaign for each domain. The Commons Protocol's evidence layer uses this ranking to weight team assessments.

**Layer 3 — AI-assisted evaluation support**
An AI-assisted tool helps evaluators apply the rubric consistently — flagging potential conflicts of interest, identifying methodological patterns, cross-referencing funding sources against known commercial interest databases, and surfacing prior contestations of the same source. The AI layer supports human evaluator judgement; it does not replace it. All AI-assisted assessments are visible and contestable.

This layer is where Anton Parf's Anthosphere evaluation experience is directly applicable — his audit tool demonstrates the cognitive task that AI-assisted evidence evaluation would perform.

---

## The evaluation rubric

The following rubric provides the operational framework that expert teams use to evaluate evidence sources. It is published openly so that participants, teams, and the public can all assess whether evaluations are being applied consistently.

### Formal credibility criteria (baseline)

All sources are assessed against these criteria. Sources failing the baseline are excluded regardless of other factors.

| Criterion | Passing | Failing |
|-----------|---------|---------|
| Authorship | Disclosed, verifiable identity | Anonymous or unverifiable |
| Methodology | Stated and independently assessable | Absent and not inferable |
| Interest disclosure | Funding sources and affiliations disclosed | Material interests undisclosed |
| Fabrication status | No documented fabrication | Retracted, corrected for fabrication, or confirmed misinformation |

### Credibility assessment dimensions (above baseline)

Sources passing the baseline are assessed across five dimensions. Each dimension is rated 1–4 by the evaluating team, with reasoning published.

**1. Independence**
Does the source's funding, institutional affiliation, or authorial interest create a material risk of bias toward a particular outcome on this question?

- 4: Fully independent — no material interest in the question outcome
- 3: Minor interest disclosed and managed — methodology provides adequate protection
- 2: Significant interest disclosed — findings should be weighted accordingly
- 1: Significant interest and methodology does not adequately protect against bias

**2. Methodology**
Is the source's methodology transparent, replicable, and appropriate to the claim being made?

- 4: Methodology fully published, independently replicated or replicable, appropriate to the claim
- 3: Methodology published and appropriate, not yet independently replicated
- 2: Methodology partially published or partially appropriate
- 1: Methodology not published or systematically inappropriate

**3. Primary vs derived**
Is the source based on primary data or primary research, or does it aggregate, interpret, or comment on other sources?

- 4: Primary data or primary peer-reviewed research
- 3: Secondary analysis of primary data with published methodology
- 2: Synthesis or review of secondary sources
- 1: Commentary, opinion, or aggregation without independent analysis

**4. Currency**
Is the source current relative to the state of knowledge in this domain?

- 4: Published within a timeframe appropriate to the domain's rate of change, or explicitly validated as current
- 3: Slightly dated but not superseded by contradicting evidence
- 2: Dated and potentially superseded — should be supplemented by more recent sources
- 1: Significantly outdated — findings are likely superseded

**5. Cross-cultural accessibility**
Can the source be understood and evaluated by participants from diverse cultural and linguistic backgrounds? Does it assume knowledge frameworks that are not universally shared?

- 4: Accessible across cultural contexts, methodology and findings translatable
- 3: Primarily accessible in one cultural context but translatable with effort
- 2: Significantly culturally embedded — requires contextualisation for other audiences
- 1: Inaccessible outside its originating cultural context without substantial mediation

### Domain-specific considerations

The rubric above applies across all question domains. The following domain-specific notes address known distortion patterns in specific areas.

**Environmental and ecological evidence**
Particular attention to: satellite and remote sensing data provenance; government agency methodology independence from extractive industry influence; the peer review record of agrochemical and fossil fuel safety research; indigenous and community ecological knowledge as valid primary evidence even where it does not fit the formal peer review category.

**Humanitarian and conflict evidence**
Particular attention to: government and military sources on their own conduct; casualty figures methodology and independence; the political affiliation of human rights monitoring organisations; the time lag between events and documentation.

**Public health and medical evidence**
Particular attention to: pharmaceutical industry funding of clinical trials and selective publication patterns; the AllTrials framework for registered trial disclosure; the distinction between regulatory approval and independent efficacy evidence; the documented commercial distortion of nutritional research.

**Economic and resource evidence**
Particular attention to: the institutional affiliation of economic modelling; the assumptions embedded in cost-benefit analyses; the distinction between GDP-based and commons-based measures of value.

**Indigenous and community knowledge**
Indigenous knowledge systems, oral traditions, and community-held evidence do not fit the formal peer review taxonomy and must not be excluded on those grounds. They are assessed under adapted criteria: community validation (the equivalent of peer review within the knowledge tradition), transmission integrity (the equivalent of methodology), and relevance to the question domain. Evaluators assessing evidence in domains where indigenous knowledge is material must include evaluators with relevant cultural competence.

---

## The contestation process

Any verified participant may contest any evaluation decision. A valid contestation must:

1. Identify the specific criterion or dimension on which the evaluation is contested
2. Provide a counter-assessment with reasoning
3. Reference at least one source supporting the counter-assessment

Contestations are reviewed by a secondary evaluation team selected randomly from teams not involved in the original evaluation. The secondary team's assessment is published alongside the original. Where the two teams disagree, both assessments remain visible to participants with equal prominence — contested evidence is displayed as contested, not silently resolved.

Persistent contested assessments — where two or more teams reach opposite conclusions after review — are escalated to the crowd wisdom layer (Updraft) for public resolution. The public assessment does not override the expert teams; it is displayed alongside them as an additional signal.

---

## The AI-assisted evaluation layer

An AI tool assists human evaluators in applying the rubric by:

- Cross-referencing disclosed funding sources against known commercial interest databases
- Flagging methodology patterns associated with known distortion (selective outcome reporting, small sample sizes in sponsored research, etc.)
- Identifying prior contestations of the same source in the Commons Protocol system
- Translating and summarising sources for evaluators operating across language barriers
- Flagging potential conflicts between a source's findings and its methodology

The AI layer produces a preliminary assessment for each source that human evaluators review, modify, and finalise. AI assessments are visible to participants alongside human assessments. All AI methodology is published and open to challenge.

---

## The epistemic bias problem

The hybrid and distributed models reduce but do not eliminate the most serious underlying problem: in certain domains, the formally credible information environment has itself been compromised by the interests the protocol is designed to hold accountable.

Documented cases include pharmaceutical industry selective publication, agrochemical safety research distortion, and tobacco industry manufacture of scientific uncertainty. The domain-specific rubric notes above address these cases directly, but they cannot fully neutralise the problem in first iteration.

The honest position for first iteration: the distributed model's multiple independent teams, crowd wisdom accountability, and published ontological grounding provide substantially better protection against epistemic capture than any centralised expert panel or community classification system alone. But they do not guarantee it. The protocol operates within known limitations and names them rather than concealing them.

---

## What this document does not resolve

**Bootstrapping the first evaluator teams:** How are the first Aura teams for Commons Protocol evidence evaluation recruited, verified, and established before the participant community exists to hold them accountable? This is the founding evaluator problem — the same bootstrapping challenge as the founding custodian problem in the governance sketch.

**Scalability of the crowd wisdom layer:** Updraft's crowd wisdom mechanism requires sufficient public participation to produce reliable signals. In the early protocol, before a large verified participant community exists, this layer will be thin. The design must be honest about what the crowd wisdom layer can and cannot provide at different stages of protocol maturity.

**The first-mover problem:** Whoever submits sources to an evidence record first shapes its initial composition. Well-resourced actors may establish a baseline that is difficult to contest even with the distributed evaluation process in place.

**Retraction and correction:** Scientific consensus changes. Investigative reporting is sometimes wrong and sometimes corrected. How does the evidence record update when a previously included source is retracted or superseded? Who monitors source status over time?

**Language and cultural equivalence:** The rubric above addresses indigenous knowledge but the broader problem of cross-cultural source assessment — what counts as credible evidence in different epistemological traditions — remains only partially addressed.

---

## Plugging into existing infrastructure

Adam Stallard (BrightID/Updraft) has confirmed that the Commons Protocol evidence record framework document can serve as the publicly acknowledged guiding document for an Aura evaluation domain without requiring changes to the Aura or Updraft infrastructure. The practical steps for plugging in are:

1. Finalise this framework document to the point where it is specific enough for evaluator teams to apply consistently
2. Establish the first evidence evaluation team(s) within the Aura system, publicly acknowledging this document as their guiding framework
3. Create an Updraft campaign for the Commons Protocol evidence evaluation domain, allowing the public to vote on which teams are trustworthy
4. Integrate the Updraft and Aura outputs into the Commons Protocol's evidence display layer

Steps 1 and 2 are the immediate next actions. Steps 3 and 4 require the Commons Protocol to have sufficient participant community to make the crowd wisdom layer meaningful.

---

## Invitation for critique

This document has benefited from input from Adam Stallard (BrightID/Updraft), Anton Parf (Anthosphere), and the Anthosphere audit series. Further critique is invited, particularly from those with expertise in: information science and source classification, the sociology of scientific knowledge, AI-assisted evaluation systems, and the governance of open knowledge communities.

The most useful responses are: specific ways the rubric would fail in identified domains, existing classification systems that address these constraints more elegantly, and precedents in evidence governance that bear on the distributed evaluation model.

---

*Version 0.2 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

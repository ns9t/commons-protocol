# Evidence Record Evaluation Tool — Test Brief
### For Anton Parf / Anthosphere — Issue #4 prototype development

---

## The question

*"Since October 2023, multiple independent monitoring organisations have documented civilian casualties in Gaza. Reported figures vary significantly between sources. Do you consider the documented rate of civilian harm acceptable under international humanitarian law standards, and does the variation between source figures affect your assessment of the available evidence?"*

This question is chosen as a test case because:
- Existence evidence is uncontested and extensively documented
- Sources score very differently against the evaluation rubric's independence and conflict of interest dimensions
- The variation between source figures is itself meaningful signal about evidence integrity
- It is live, globally relevant, and tests the tool against a high-stakes contested domain

---

## Test evidence sources

The following four sources are chosen to represent genuinely different profiles against the evaluation rubric. The tool should produce meaningfully different scores for each.

**Source 1 — UN OCHA (Office for the Coordination of Humanitarian Affairs)**
- URL: ochaopt.org
- Type: Intergovernmental humanitarian monitoring organisation
- Expected profile: High methodology transparency, moderate independence (UN member states include parties to the conflict), high currency, high cross-cultural accessibility
- Key tension to flag: UN funding relationships and Security Council dynamics create indirect pressure on reporting

**Source 2 — Médecins Sans Frontières / Doctors Without Borders**
- URL: msf.org — Gaza situation reports
- Type: Independent medical humanitarian organisation with field presence
- Expected profile: High independence (explicitly non-governmental, non-partisan), high methodology (direct field observation), high currency, high cross-cultural accessibility
- Key tension to flag: Field presence means direct observation but also exposure to information control by parties controlling access

**Source 3 — Israeli Defense Forces official statements**
- URL: idf.il
- Type: Official military communication from a party to the conflict
- Expected profile: Low independence (direct conflict of interest), low methodology transparency (operational security constraints on disclosure), high currency
- Key tension to flag: Primary source for some facts not available elsewhere, but maximum conflict of interest on casualty figures

**Source 4 — Gaza Ministry of Health figures**
- URL: moh.gov.ps
- Type: Government body of the governing authority in Gaza
- Expected profile: Moderate methodology (systematic record-keeping but resource-constrained), low independence (party to the conflict on the other side), high currency
- Key tension to flag: Historically cited by UN and independent organisations as reliable for raw casualty counts despite political affiliation; methodology has been independently validated in peer-reviewed literature

---

## The evaluation rubric

Apply the five dimensions from the evidence record design document to each source. Rate each dimension 1–4 with reasoning.

**1. Independence**
Does the source's funding, institutional affiliation, or direct interest create a material risk of bias toward a particular outcome on this question?
- 4: No material interest in the question outcome
- 3: Minor interest disclosed and managed
- 2: Significant interest disclosed
- 1: Significant interest, methodology does not adequately protect against bias

**2. Methodology**
Is the source's methodology transparent, replicable, and appropriate to the claim being made?
- 4: Methodology fully published, independently replicable, appropriate to the claim
- 3: Methodology published and appropriate, not yet independently replicated
- 2: Methodology partially published or partially appropriate
- 1: Methodology not published or systematically inappropriate

**3. Primary vs derived**
Is the source based on primary data or primary research?
- 4: Primary data or primary peer-reviewed research
- 3: Secondary analysis of primary data with published methodology
- 2: Synthesis or review of secondary sources
- 1: Commentary, opinion, or aggregation without independent analysis

**4. Currency**
Is the source current relative to the state of knowledge in this domain?
- 4: Current and explicitly validated
- 3: Slightly dated but not superseded
- 2: Potentially superseded
- 1: Significantly outdated

**5. Cross-cultural accessibility**
Can the source be understood and evaluated by participants from diverse cultural and linguistic backgrounds?
- 4: Accessible across cultural contexts
- 3: Primarily accessible in one cultural context but translatable
- 2: Significantly culturally embedded
- 1: Inaccessible outside its originating context

---

## Expected output format

For each source, the tool should produce:

```
Source: [name]
URL: [url]

Baseline criteria:
- Authorship: [disclosed / not disclosed]
- Methodology: [stated / not stated]
- Interest disclosure: [disclosed / not disclosed]
- Fabrication status: [none documented / flagged]
- Baseline result: [PASS / FAIL]

Assessment dimensions (if baseline passed):
- Independence: [1-4] — [reasoning]
- Methodology: [1-4] — [reasoning]
- Primary vs derived: [1-4] — [reasoning]
- Currency: [1-4] — [reasoning]
- Cross-cultural accessibility: [1-4] — [reasoning]

Overall credibility score: [average]
Key flags: [conflict of interest notes, methodology concerns]
Recommended weighting: [include as primary / include with caveats / include as supporting only / exclude]
```

---

## What a useful first output looks like

The tool does not need to be perfect for the first iteration. A useful first output:
- Produces meaningfully different scores for the four sources
- Flags the conflict of interest tension in Sources 3 and 4 explicitly
- Notes the independent validation of Gaza Ministry of Health methodology as a complicating factor for simple independence scoring
- Produces reasoning that a human evaluator could review, modify, and publish

The variation between sources is the most important thing to capture — a tool that scores all four sources similarly has not understood the rubric.

---

## Design document reference

Full evaluation rubric and rationale: 
https://github.com/ns9t/commons-protocol/blob/main/design/evidence-record-design.md

GitHub issue: 
https://github.com/ns9t/commons-protocol/issues/4

---

*Commons Protocol Stewardship — commonsprotocol@proton.me*

# Working Notes — Commons Protocol
### Internal only — not for publication
### Updated session 9 — major development sprint

---

## Status summary

Repository public at github.com/ns9t/commons-protocol. Founding document at v1.0. Verification sketch at v0.4. Governance sketch at v0.3. Evidence record design at v0.2. Interconnection map at v0.2. Adoption and seeding guide at v0.1 (public facing — internal designation removed). CONTRIBUTING.md added. Six GitHub issues open for minimal proof of concept. Adam Stallard self-assigned Issue #2. Anton Parf working on Issue #4 prototype with Gaza test brief. Essays published: Wiring the Organism, The God in the River. Stewardship email: commonsprotocol@proton.me.

---

## Active flags — founding document

**Flag 1 — Section title "One Movement"**
Hold for now.

**Flag 2 — Hawken placement**
Hold.

**Flag 4 — Naming / working title**
"Global Commons Consensus Protocol" as full name, "Commons Protocol" as short form. Consistent throughout from v0.8. Deferred.

**Flag 5 — Publication timing**
Founding document v1.0 complete and published. All revision items from Flag 50 incorporated. Closed.

**Flag 50 — Founding document v1.0 revision items**
All items incorporated in v1.0. Additional items identified from Francesco Bonetti's design critique:

- **7.6 descriptive vs prescriptive clauses** — Francesco's framework distinguishes clauses that describe mechanisms (must follow the machine) from clauses that constrain it (machine must follow these). The Commons Protocol founding document conflates these in places — some clauses describe aspirations that don't yet technically exist, which makes them false statements with a seal. Worth addressing in next revision pass.
- **Simulation testing equivalent** — Francesco's sim-before-live model suggests the Commons Protocol's filter pyramid needs a buffer between elevation and permanent record. A phase where an elevated question is visible but responses not yet counted would allow framing and evidence record refinement. Not yet in any design document.

---

## Active flags — governance design

**Flag 10 — Governance sketch status**
v0.3 complete. Custodian accountability section added. Sent to Anton Parf for audit.

**Flag 11 — Temporal independence criterion**
Open.

**Flag 12 — Bootstrap problem**
Open.

---

## Active flags — verification design

**Flag 13 — Verification sketch status**
v0.4 complete. Adam Stallard self-assigned Issue #2 (BrightID/Aura verification integration) on GitHub — first formal code commitment from any collaborator.

**Flag 14 — The safety paradox**
Partially addressed. Zoom concern resolved — any trusted channel works. Aura Add Device failure still unresolved — Adam posted engineer query, no response yet.

**Flag 15 — Offline verification**
Open.

---

## Active flags — evidence record design

**Flag 17 — Evidence record design status**
v0.2 complete. Approach C (distributed evaluation model) as primary working hypothesis. Full operational rubric with five dimensions. Domain-specific guidance. AI-assisted evaluation layer. Plugging into Aura/Updraft described.

New addition from Anton Parf observation: existence vs causality evidence distinction. Existence evidence (visually verifiable, low burden — don't make it a bureaucratic escape route). Causality and accountability evidence (contested, full Approach C process warranted). Added to v0.2.

**Flag 18 — Approach A vs B**
Resolved in favour of Approach C. Closed as design question.

**Flag 19 — The epistemic bias problem**
Named cases documented. Political problem, not technical.

**Flag 20 — First-mover problem**
Open.

**Flag 21 — Language and cultural equivalence**
Open.

**Flag 22 — Retraction and correction problem**
Open.

**Flag 23 — Scalability of community classification**
Open.

---

## Active flags — token and funding layer

**Flag 24 — Token layer status**
v0.2 complete.

**Flag 27 — Soul-bound token implementation**
Open.

**Flag 28 — Contributor compensation equity**
Open.

**Flag 29 — Grant governance**
Open.

---

## Active flags — tiered access

**Flag 30 — Tiered access specification status**
v0.1 complete. Needs v0.2 for Flag 32.

**Flag 31 — The participation-quality tradeoff**
Named in spec.

**Flag 32 — Quality metric for Tier 3 to Tier 4 transition**
Open.

**Flag 33 — Quorum question**
Open.

**Flag 34 — Founding steward question**
Open.

---

## Active flags — interconnection map

**Flag 35 — Interconnection map design status**
v0.2 complete. MLF experiential design principles added.

**Flag 36 — Project Drawdown relationship**
Deferred. Paul Hawken responded via mutual contact (Rebecca) — capacity constraints, not available. Drawdown team approach (not Paul directly) remains a future target once proof of concept exists.

**Flag 37 — Algorithmic inference question**
Open.

**Flag 38 — Low-bandwidth accessibility**
Open.

**Flag 39 — Map as political object**
Open.

---

## Active flags — influences document

**Flag 40 — Influences document status**
v0.1 complete. Add contributors section for Adam Stallard. Pending.

**Flag 41 — 2019 antecedent article**
Pending.

---

## Active flags — outreach and circulation

**Flag 42 — Metagovernance Project contact**
Active. Multiple substantive engagements. See institutional relationships below.

**Flag 43 — Mastodon / social media**
No meaningful responses. Deprioritise.

**Flag 44 — Trusted circle and direct outreach**
Randolph Kent — no further response. Treated as dormant for now. David Bollier — no response. Laura Sandys — no response. Marzia Briel — no response.

**Flag 45 — AI acknowledgment**
Complete.

**Flag 49 — Adam Stallard / BrightID relationship**
Self-assigned Issue #2 on GitHub — first formal code commitment. Has forked Plurality (Weyl/Tang) — confirms engagement with adjacent intellectual territory. Active collaborator status confirmed.

---

## Active flags — accessible summary document and contacts

**Flag 47 — Accessible summary document**
Hold until proof of concept exists. Essay is the front door.

**Flag 48 — Randolph Kent engagement**
Dormant. No further response to governance sketch invitation or Sense-Making Project introduction request. Do not pursue further for now.

**Flag 51 — Sense-Making Project**
Dormant pending Randolph introduction which has not arrived.

**Flag 52 — Global Regeneration CoLab**
Deferred — premature until proof of concept exists.

**Flag 53 — Strategic orientation**
Updated. Three active technical relationships now in play:
1. Adam Stallard — identity and funding infrastructure layer. Self-assigned Issue #2. Active.
2. Anton Parf — AI-assisted evaluation layer. Working on Issue #4 prototype with Gaza test brief. Active.
3. Francesco Bonetti (Pangea) — governance and cryptographic architecture. Homomorphic ballot encryption and OpenTimestamps directly relevant to Issues #5 and #6. Relationship developing.

Harley Goodwin (The People's Branch) — warm relationship, US-civic orientation, builds within existing constitutional framework. Philosophically sympathetic but operates on a different premise from the Commons Protocol. Maintain warm contact, low energy investment.

---

## Active flags — proof of concept

**Flag 72 — Minimal proof of concept — six GitHub issues (new)**
CONTRIBUTING.md added to repository root. Six GitHub issues created:

- Issue #1 — Question registry (Python/TypeScript, PostgreSQL, React)
- Issue #2 — Participant verification (BrightID API) — self-assigned by Adam Stallard
- Issue #3 — Elevation panel mechanism
- Issue #4 — Evidence record evaluation tool (AI-assisted) — Anton Parf working on prototype
- Issue #5 — Response collection interface
- Issue #6 — Cryptographic output record (OpenTimestamps, IPFS/Arweave)

Gaza test brief produced for Issue #4 — four sources (UN OCHA, MSF, IDF, Gaza Ministry of Health) chosen to test the independence and conflict of interest dimensions of the evaluation rubric. Uploaded to repository as design/test-brief-issue4.md.

Anton asked two questions: why Gaza, and what are next steps after evaluation. Answered: Gaza chosen because sources score very differently against the rubric; next steps require all six issues connected on distributed infrastructure before cryptographic output record is produced — Anton's prototype is one of six components.

**Flag 73 — Francesco Bonetti / Pangea (new)**
Solo builder, physiotherapist by day, Verona Italy. Built Pangea — self-modifying constitutional governance system. Features directly relevant to Commons Protocol:
- Homomorphic ballot tallying — votes counted without being decrypted (relevant to Issue #5 and #6)
- Tamper-evident history via OpenTimestamps — permanent independent timestamp (relevant to Issue #6)
- Simulation-before-live — constitutional changes tested in sandbox before binding (no equivalent in Commons Protocol — worth adding)
- No reshare button by constitutional design — anti-virality by architecture
- Recursive federation — groups nest as constitutional tree, forking is citizen right
- No chain, no token (¬9.1) — same reasoning as Commons Protocol: receipt-freeness, personhood, cost

Key refusals worth noting for Commons Protocol design:
- ¬9.1: receipt-freeness argument directly relevant — Commons Protocol's output record needs to specify whether individual votes are permanently public or only aggregate signal is
- 7.6: descriptive vs prescriptive clause distinction — reveals a gap in Commons Protocol founding document
- 7.9: the interpreter that does not exist — honest acknowledgement that some questions cannot be settled by running a rule. Commons Protocol should make the same acknowledgement for contested evidence

Relationship developing. Three exchanges so far. Critical feedback given on: 7.9 (interpreter problem), simulation bootstrapping problem (Aura as potential solution), fork fragility. Francesco engaged, response substantive though AI-mediated.

**Flag 74 — Harley Goodwin / The People's Branch (new)**
82-year-old solo builder, Putnam CT, building The People's Branch (4tpb.org) — US civic signal platform with AI-paired citizens, representative accountability layer, geographic signal interface, 28th Amendment constitutional route as long-term goal. 1,249 registered voices, polls largely unpopulated.

Key observation: "TPB carries conscience into consequence inside one country's process, the Commons Protocol makes it permanently legible beyond any." — clearest description of the seam between the two projects. Cleared to go into adoption guide.

Three-step arc: aggregate signal → shared mandate → constitutional route. Commons Protocol lives at step one permanently. TPB is building toward step three inside a specific jurisdiction.

AI-for-every-citizen model (not just stewards) is more biomimetically consistent than Commons Protocol's current design — worth considering for future revision.

Open room created on TPB for Commons Protocol exchange. All letters in the room. Nik is co-facilitator.

Calibration: warm relationship, low energy investment. Harley builds within existing constitutional framework which is a different premise from the Commons Protocol. Not a primary integration partner for proof of concept.

**Flag 75 — Essay: The God in the River (new)**
Second published essay drafted. Title: "The God in the River Needs More Than a Lawyer — and so do we." Draws on Robert Macfarlane, Ted Hughes, Nan Shepherd, Kathleen Raine, Māori proverb (Ko au te awa), Rights of Nature / Mar Menor, Municipal England / northern towns. Biomimicry thread throughout. Commons Protocol introduced as the infrastructure for making expressed conscience permanently legible.

Status: editing complete, ready to publish. Tags and subtitle finalised. Subtitle: "On the law, rivers, northern towns, and the infrastructure in the wings."

**Flag 76 — Metagov community call on protocols (new)**
Brandon Nørgaard proposed community call: "Scoping a Protocols space — and the tools we already have for evaluating decentralised protocols." References OpenHaven's protocol comparison matrix and Nathan Schneider's Protocol Bicorder. Angel Marino, Liz Barry among approvals. Commons Protocol should engage with this call — it's the community-level conversation about fragmentation that has been needed. Vote to approve and participate.

---

## Repository structure (current)

```
commons-protocol/
├── founding-document.md (v1.0)
├── working-notes.md
├── README.md
├── CONTRIBUTING.md (new)
├── LICENCE
└── design/
    ├── governance-sketch.md (v0.3)
    ├── verification-sketch.md (v0.4)
    ├── evidence-record-design.md (v0.2)
    ├── token-funding-layer.md (v0.2)
    ├── tiered-access-specification.md (v0.1 — v0.2 needed)
    ├── interconnection-map-design.md (v0.2)
    ├── influences-prior-art.md (v0.1)
    ├── adoption-and-seeding-guide.md (v0.1 — public facing)
    └── test-brief-issue4.md (new — Gaza evidence evaluation test)
```

---

## Next phase priorities

1. Anton — await Issue #4 prototype output, refine based on results
2. Adam — Issue #2 in progress, monitor
3. Francesco — await response to critical feedback, explore OpenTimestamps/homomorphic encryption components for Issues #5 and #6
4. Metagov protocols community call — participate
5. Tiered access specification v0.2 — Flag 32 clarification
6. Influences document — add contributors section (Adam Stallard)
7. The God in the River essay — publish
8. Simulation testing equivalent — consider adding to governance sketch or filter pyramid design
9. 7.6 descriptive vs prescriptive clause fix — next founding document revision
10. Drawdown team approach — after proof of concept exists

---

## Institutional relationships

- **Adam Stallard / BrightID** — first specialist contributor, self-assigned Issue #2, active collaborator
- **Anton Parf / Anthosphere** — AI evaluation prototype (Issue #4), active, enthusiastic
- **Francesco Bonetti / Pangea** — governance and cryptographic architecture overlap, relationship developing
- **Harley Goodwin / The People's Branch** — warm contact, low energy investment, open room established
- **Angel Marino** — non-responsive after initial exchange, moved on
- **Metagovernance Project** — active Slack community, multiple contacts
- **Randolph Kent** — dormant
- **David Bollier** — no response
- **Laura Sandys** — no response
- **Marzia Briel / Reading University** — no response
- **Protocol Institute / Protocolized** — essay pitched, no response
- **Project Drawdown** — deferred, approach team not Paul directly after proof of concept
- **Global Regeneration CoLab** — deferred
- **Sense-Making Project** — dormant
- **Rights of Nature / Repatterning Collective** — deferred
- **RadicalxChange** — deferred
- **Dark Matter Labs** — deferred
- **Open Society / Ford / Shuttleworth / Omidyar** — grant targets, deferred

---

## Design tensions (standing flags)

**Flag 54 — Updraft as infrastructure funding**
Working position: provisional bridge while CEU model develops. Not permanent adoption.

**Flag 55 — Wikipedia governance / output tension**
Use as cautionary model as much as exemplary one.

**Flag 56 — Boundary enforcement: stated vs structural**
Every pragmatic compromise must be tested: is the boundary structural or merely stated?

**Flag 57 — Rights of Nature / Mar Menor precedent**
Added to founding document v1.0. Emergent Commons Guardianship framing.

**Flag 58 — Who this is for**
Addressed in adoption and seeding guide opening.

**Flag 64 — Citizen Infrastructure ecosystem**
Priority contacts extracted. Sequencing: technical builder first, institutional credibility second, community participants third.

**Flag 65 — GitBook/Starlight documentation format**
Deferred until content stable.

**Flag 66 — Anthosphere audit series**
Five audits complete. Scores 72-82. Persistent gap: resources/self-sufficiency. Key insight: recursive self-application — use protocol to govern own resource allocation.

**Flag 68 — Marshmallow Laser Feast / Emergence Magazine**
MLF experiential design principles incorporated into interconnection map v0.2. Deferred as contact.

---

## Closed flags

**Flag 3** (closed v0.5) **Flag 6** (closed session 5) **Flag 7** (closed session 2) **Flag 8** (closed v0.6) **Flag 16** (closed v0.2 verification sketch) **Flag 18** (closed — Approach C adopted) **Flag 25** (closed session 4) **Flag 26** (closed session 4) **Flag 46** (closed session 6)

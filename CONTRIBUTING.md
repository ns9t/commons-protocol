# Contributing to the Commons Protocol

The Commons Protocol is an open, decentralised protocol designed to surface verifiable global human conscience — without central authority, commercial incentive, or political affiliation. It belongs to no one. It is offered to everyone.

This file explains what the project needs, how to get involved, and where your skills might fit.

---

## What we are building right now

The design documents are complete enough to build from. The immediate goal is a **minimal proof of concept** — one question, elevated through the filter pyramid, producing a cryptographically signed output record, visible to the world.

This demonstration does not need to be production-ready. It needs to be real. A working signal, however small, transforms the project from a design suite into something builders can connect to.

The proof of concept has six components. Each is tracked as an open GitHub issue. You do not need to build all of them — one component built well is a contribution.

---

## The six components

| Component | What it does | Skills needed | Issue |
|-----------|-------------|---------------|-------|
| Question registry | Stores and displays questions at local/regional/global tier | Python or TypeScript, PostgreSQL, React | #1 |
| Participant verification | BrightID API integration for verified unique participants | API integration, cryptographic identity | #2 |
| Elevation panel mechanism | Panel review, determination, published reasoning | Web development, simple workflow | #3 |
| Evidence record evaluation | AI-assisted assessment of source credibility | AI/ML, Python, structured evaluation | #4 |
| Response collection | Verified participant voting interface | Frontend, verification gate | #5 |
| Cryptographic output record | OpenTimestamps signing and permanent archiving | Cryptography, Python | #6 |

---

## How to contribute

**If you want to build a component:** Open the relevant issue, comment that you are interested, and describe your proposed approach. We will respond and coordinate from there.

**If you want to propose a different technical approach:** Open a new issue describing the alternative. All design decisions are open to challenge — the methodology transparency principle applies to the technical layer as much as to the governance layer.

**If you want to critique the design:** Open an issue or propose a revision to the relevant design document. The design documents are in the `/design` folder. The most useful critiques name a specific problem and propose an alternative.

**If you want to translate the founding document:** Open an issue. Multilingual accessibility is a founding principle.

**If you have a different skill:** Open an issue describing what you can offer. The project needs domain expertise in humanitarian systems, commons governance, environmental science, and legal frameworks as much as it needs code.

---

## The design documents

All design decisions are documented in the `/design` folder. Read the relevant document before building — the design constraints matter and the reasoning behind them is documented.

| Document | What it covers |
|----------|----------------|
| `governance-sketch.md` | Question elevation, custodian accountability, gaming detection |
| `verification-sketch.md` | Participant verification, BrightID Aura, the identity trilemma |
| `evidence-record-design.md` | Evidence record design, the evaluation rubric, Approach C distributed model |
| `token-funding-layer.md` | Infrastructure funding, CEU model, ATP principle |
| `tiered-access-specification.md` | Participation tiers, access criteria |
| `interconnection-map-design.md` | The planetary map interface, experiential design principles |
| `adoption-and-seeding-guide.md` | How the protocol connects to existing platforms and communities |

---

## The founding principles

Any contribution must be consistent with the seven founding principles in the founding document. The most relevant for technical contributors:

- The signal is unmonetised and unmonetisable — no token attached to the vote itself
- No central authority — no single server, organisation, or actor can control or suppress the protocol
- Transparent methodology, open to challenge — no black boxes, no proprietary algorithms
- Structurally neutral — the protocol does not take positions, it records them

---

## Current active collaborators

- **Adam Stallard** (BrightID/Updraft) — identity verification infrastructure, crowd wisdom accountability layer
- **Anton Parf** (Anthosphere) — AI-assisted evaluation, civilisational coordination layer
- **Nik Spitz** — founding steward, design documents

Correspondence: commonsprotocol@proton.me

---

## A note on the project's stage

The Commons Protocol is not a finished thing. The design documents describe what needs to be built; most of it has not been built yet. The proof of concept described above is the first working implementation goal.

If you are looking for a mature codebase to contribute to, this is not it yet. If you are looking for a project at the stage where the earliest contributors shape it most — this is exactly that.

*No author. No organisation. Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

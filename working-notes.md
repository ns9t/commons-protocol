# Working Notes — Commons Protocol
### Internal only — not for publication
### Updated after session 2 design review

---

## Open flags — founding document

**Flag 1 — Section title "One Movement"**
Currently used. Alternative "The Movement" considered and set aside as potentially too generic or politically coded. Review on next pass.

**Flag 2 — Hawken placement**
Moved from introduction to "One Movement" section body and footnote. Introduction now opens with the document's own argument. Currently feels appropriately weighted. Hold.

**Flag 3 — Multilingual consistency**
Founding document states multilingual as a universal founding principle but singles it out specifically at the global tier, implying it doesn't apply below. Clarification needed: translation is default at all tiers; quality and coverage scales with tier. Local tier functions in community language with machine translation available. Global tier requires human-reviewed translation to preserve neutral framing across languages. Principle is universal; implementation varies. Amend in v0.5.

**Flag 4 — Naming**
Unresolved. Full candidate list: Earth Commons Grid, Earth Resonance Grid, Earth Resonance Project, Conscience Earth Grid, Global Conscience Grid, Common Ground Protocol, Commons Signal Grid, Commons Layer, Earth Grid, Earthsignal. Strongest current candidates: Common Ground Protocol, Earth Commons Grid. Decision deferred until document is stable.

**Flag 5 — Publication timing**
Internal development only until verification, governance, and interconnection map have provisional design answers.

**Flag 6 — Stewardship identity**
Decision pending: pseudonymous steward from outset (better for institutional relationships) vs. anonymous circulation until organic stewardship group forms (more consistent with philosophy). No institutional approaches until document is ready.

**Flag 7 — Forking clarification**
Explicit in stewardship section. Founding document is not forkable — it is the constitution. Implementations branch from it. Invitation section now calls for collaboration on a single first build.

---

## Open flags — governance design

**Flag 8 — Question curation governance**
Governance sketch v0.1 drafted. Three-stage elevation with cryptographic verification, temporal independence criterion, and random panel review. Addresses three failure modes: gaming by coordination, ideological capture, bureaucratic stagnation. Needs critique from people with technical and governance expertise. Upload to /design folder in repository.

**Flag 9 — Temporal independence criterion**
Primary anti-astroturfing mechanism. Genuine cross-cultural resonance spreads with natural time lags; coordinated gaming shows synchronised spikes. Observable in data without revealing identity. Publish methodology openly for external audit. Strong candidate for peer review before implementation.

**Flag 10 — Bootstrap problem**
Social vouching requires existing verified participants. How does the network reach sufficient diversity at outset rather than reflecting demographics of earliest adopters? Partially addressed by tiered access model (see Flag 14) — observers require nothing, path from observer to participant is designed to be accessible. Remains an open design challenge.

**Flag 11 — Jurisdiction**
Protocol operates across conflicting legal jurisdictions. Legal domicile question unresolved. Exposure if global layer question defames specific entity or government is unassessed. Requires legal input before any public launch.

---

## Open flags — epistemic integrity

**Flag 12 — The evidential bias problem**
Critical design challenge. The protocol's evidence record, if it defers to established sources, inherits the institutional and commercial biases embedded in those sources. Wikipedia is a known example — its entries on contested medical and environmental topics demonstrably reflect mainstream institutional positions rather than neutral evidence assessment. The black salve / Greg Caton case is a concrete instance: a plant compound with documented medicinal properties, suppressed through regulatory and media capture, misrepresented in ostensibly neutral sources.

Resolution for first iteration: the protocol operates within the limits of what it can verify through established methodological standards, and those limits are explicitly acknowledged as a known limitation and future design challenge — not a permanent position. This is not a dismissal of contested evidence; it is an honest statement of what the first implementation can and cannot do.

The epistemic bias problem — the systematic suppression or distortion of evidence by institutional and commercial interests — is flagged as a major future design challenge the project must eventually confront directly. Should appear in the founding document's "next questions" section as a named limitation.

**Flag 13 — Scope discipline for first iteration**
First iteration should focus on questions with navigable evidential situations: geopolitical abuses (Palestine, Amazon deforestation, sand extraction) where the factual basis, while contested, is not comprehensively suppressed. Questions involving medical suppression, alternative science, and regulatory capture are within the project's long-term scope but will consume credibility before it is established if attempted prematurely. Organic evolution of scope as the project demonstrates credibility is the correct sequencing.

---

## Open flags — architecture

**Flag 14 — Tiered access model**
Five proposed tiers:
- **Observer** — zero barrier, no verification. Read-only access to all questions, results, evidence records. No signup, no data. Entry point for global majority.
- **Participant** — light verification via social vouching or equivalent. Can engage and vote at local tier. Contribute to evidence records.
- **Proposer** — demonstrated participation history, fuller verification. Can raise questions, nominate for regional consideration, contribute to framing review.
- **Reviewer** — earned through contribution quality, subject to random selection for panel review. Cannot self-nominate.
- **Steward** — custodial role for canonical documents. Subject to community accountability. No authority over signal, only over protocol integrity.

Each tier has verification requirement proportionate to consequence of participation. Needs formal specification in separate design document.

**Flag 15 — Token / funding layer**
Architecturally and documentarily separate from signal layer. Token has utility value only — not speculative. Mechanism:
- Infrastructure costs denominated in token
- Contributors earn tokens through verified labour (translation, framing review, panel participation, code contribution)
- Tokens used to vote on infrastructure budget allocations
- External donors and grant-making foundations can purchase tokens at defined rate, distributed to contributors
- Non-accumulative: tokens not spent within defined period are redistributed, not held (ATP principle applied)
- Token cannot be exchanged for anything outside the ecosystem
- Closest existing model: Gitcoin for open source funding, with ATP non-accumulation constraint added

Will not make anyone wealthy. Will fund the work. Needs its own design document. Should not appear in founding document — lives in a separate token design paper that references the founding document, not vice versa.

**Flag 16 — Evidence record design**
Each question at every tier carries an open, citable evidence record — a structured bibliography of verifiable sources participants can consult. Governed process for source submission and classification. Sources classified by methodological standard (peer review, IFCN accreditation, investigative journalism standards) not excluded by gatekeepers. Classification methodology published and contestable. Protocol does not take positions; it ensures participants have access to information to form their own. Who assesses source credibility and by what standard is an open design question. Needs its own design sketch.

---

## Prior art and influences

**Flag 17 — 2019 ATP / Human Coin article**
Published at intothedialectic.com and Medium. Authored piece anticipating core concepts of this project — ATP biomimetic model, participatory economics, P2P infrastructure for commons governance. Cannot be made unauthored without misrepresenting publication history.

Recommended approach A: add a postscript or companion piece to the original article acknowledging that its ideas contributed to a subsequent initiative, linking to the GitHub repository without naming the repository's steward.

Recommended approach B: repository includes an `influences.md` file acknowledging ATP / Human Coin concept as antecedent alongside Hawken, Sahtouris, and Dunbar — without naming its author.

Both approaches can coexist. Decision pending.

---

## Next design documents needed (priority order)

1. **Verification sketch** — human identity without centralised database. Constraints, candidate approaches, trade-offs.
2. **Evidence record design** — source classification, governance, relationship to epistemic bias problem.
3. **Interconnection map** — data sources, editorial governance, technical architecture.
4. **Token / funding layer** — separate document, ATP non-accumulation model, Gitcoin reference.
5. **Tiered access specification** — formal definition of five tiers, verification requirements per tier.

---

## Institutional relationships (when ready)

Natural first contacts once document is stable and governance sketch is complete:
- Project Drawdown — environmental interconnection methodology
- Metagovernance Project (metagov.org) — digital governance research
- Consul Project — participatory democracy prior art
- Fediverse / ActivityPub developer community — federated infrastructure
- Nostr developer community — decentralised identity

Warm introduction preferred in all cases. No cold approaches until project can stand independently.

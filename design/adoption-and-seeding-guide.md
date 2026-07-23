# Commons Protocol — Adoption and Seeding Guide
### Design document v0.1 / internal / not for publication

---

## Purpose of this document

The founding document describes the Commons Protocol as designed to be seeded into existing networks rather than requiring communities to find and join a new platform. This document explains what that means in practice — how the protocol reaches communities, what adoption looks like for different kinds of organisations and platforms, and how the question elevation process connects to people who may never know they are participating in a global consensus mechanism.

This document is written for three audiences: civil society organisations and NGOs considering whether and how to engage with the protocol; builders of existing civic and governance platforms considering integration; and community organisers who want to raise questions at the global level but do not have technical capacity to build infrastructure themselves.

---

## The cold start problem — and why the Commons Protocol doesn't have one in the conventional sense

Every participatory platform faces the same fundamental challenge: the signal only has meaning when enough people are producing it, but enough people won't produce it until they believe the signal has meaning. Most platforms attempt to solve this by building a compelling interface and waiting for users to arrive. This is the cold start problem.

The Commons Protocol does not claim to have solved it. What it claims is something more useful: it doesn't have the cold start problem in the same form, because it is not trying to attract users to a new interface.

The Commons Protocol is a layer, not a destination. Its participants are the people already using The People's Branch, Pangea, Polis, Consul, and every other civic platform. Its communities are the members of every humanitarian NGO, environmental cooperative, and neighbourhood association that chooses to connect. It does not need those people to leave the platforms they trust and navigate something new. It needs their platforms to connect to the global elevation layer.

This means the relationship between the Commons Protocol and existing civic platforms is not competitive. It is complementary in both directions.

**What the Commons Protocol gives existing platforms:** A global signal layer they could not build alone. A permanent, cryptographically signed record of cross-cultural consensus that gives their community's questions reach and consequence beyond their own user base. The ability to say: this question mattered not just to our users, but to verified participants across 94 countries and 47 language groups.

**What existing platforms give the Commons Protocol:** The communities it needs to produce a meaningful signal. The verified participants, the local questions, the cultural diversity, the geographic spread. Without them, the protocol has architecture but no signal.

Neither makes the other redundant. Each makes the other more valuable. A civic platform without a global signal layer produces local consensus with no mechanism for global consequence. A global signal layer without existing communities to draw from has no participants and no questions.

The complementarity runs in three directions, not two:

**What the Commons Protocol gives existing platforms:** A global signal layer they could not build alone. A permanent, cryptographically signed record of cross-cultural consensus that gives their community's questions reach and consequence beyond their own user base.

**What existing platforms give the Commons Protocol:** The communities it needs to produce a meaningful signal — verified participants, local questions, cultural diversity, geographic spread.

**What the Commons Protocol gives existing platforms' potential users:** Discovery. A participant engaging with a question about civic representation may be directed toward The People's Branch, where that question is being actively deliberated. A participant interested in participatory constitutional design may be directed toward Pangea. The signal layer creates discovery pathways into deliberation platforms — not just the reverse. For platform builders with small user bases, this is a meaningful incentive: connection to the Commons Protocol is also a channel through which new participants find their way to the platform.

---

## Three adoption pathways

### Pathway 1 — The local tier node

The most direct form of adoption. An organisation, community group, or network establishes a local tier node — a defined community of up to approximately 150 verified participants who can raise questions, discuss them, and nominate them for elevation to the regional tier.

**Who can establish a local tier node:**
Any organisation or group that can verify the identity and uniqueness of its members, commit to the protocol's founding principles, and maintain the node according to the governance sketch's requirements. This includes:

- Civil society organisations with existing membership structures
- Community cooperatives, neighbourhood associations, and local governance bodies
- NGO field teams with established relationships with the communities they serve
- Academic research groups with defined participant communities
- Existing civic platforms that want to connect their users to the global elevation process

**What establishing a local tier node requires:**
A local tier node needs: a verified participant community of at least 10 members to begin (with a path to 150); a designated steward who understands and can explain the founding principles; a method for verifying participant uniqueness (integration with BrightID Aura or equivalent); and a commitment to the protocol's transparency requirements — all elevation nominations published with reasoning, all decisions open to challenge.

**What a local tier node does not require:**
Technical infrastructure. The protocol is designed so that local tier participation can occur through existing communication channels — a WhatsApp group, a community forum, a Slack channel, an in-person meeting — with the steward responsible for translating the community's expressed concerns into the protocol's question format and submitting them to the elevation process. The barrier to establishing a local tier node is organisational, not technical.

**A concrete example — the fishing cooperative:**
A fishing cooperative in Senegal whose members have observed the depletion of their traditional fishing grounds by industrial trawlers does not need to know about the Commons Protocol. The cooperative's representative — perhaps connected to the protocol through an NGO partner — establishes a local tier node for the cooperative. The representative works with members to articulate their concern as a protocol-standard question: not "foreign trawlers are stealing our fish" (evaluative, unelevatable) but a factual framing with documented evidence of catch decline, vessel registration data, and the economic impact on cooperative members. That question enters the elevation process. If it demonstrates cross-cultural resonance — if fishing communities in Vietnam, Peru, and Norway recognise the same dynamic — it rises to the regional tier. The Senegalese cooperative members have contributed to a global signal without ever using a new platform.

---

### Pathway 2 — Platform integration

The second adoption pathway is for builders of existing civic and governance platforms who want to connect their users to the Commons Protocol's elevation process without replacing their own interface.

**The integration model:**
Rather than asking a platform's users to leave and participate in the Commons Protocol directly, integration means the platform's own participation layer connects to the protocol's elevation mechanism. A question that reaches resonance threshold within the platform's community can be nominated for elevation into the Commons Protocol regional tier. The platform's users participate through the interface they already use; the Commons Protocol receives the elevated question and processes it through the global tier.

**What this looks like in practice:**

*For a platform like The People's Branch (4tpb.org):* Questions that achieve high civic consensus within the platform's US user base could be nominated for elevation to the Commons Protocol's regional tier — connecting US civic signal to the global layer without requiring US users to leave the platform or understand the broader protocol architecture. The People's Branch handles the civic interface; the Commons Protocol handles the global signal layer.

*For a platform like Pangea:* A constitutional group within Pangea that passes a resolution on a matter of global commons significance could nominate that resolution for elevation through the Commons Protocol's question process. Pangea's homomorphic ballot encryption and tamper-evident history could potentially serve as evidence of the resolution's legitimacy within the local tier. The two systems complement rather than compete.

*For a platform like Polis or the Computational Democracy Project's tools:* Opinion clustering outputs that identify cross-cultural consensus could be translated into protocol-standard questions and elevated. The deliberation happens on the existing platform; the permanent global record is produced by the Commons Protocol.

**What integration requires from platform builders:**
An API connection to the protocol's question submission layer, a commitment to the protocol's question framing standards (neutral framing, evidence record requirement), and an identity bridge — a way for the platform's verified users to be counted as verified participants in the Commons Protocol without double-counting. This is where BrightID Aura's domain architecture becomes relevant: a platform that uses BrightID for identity verification can connect directly to the Commons Protocol's verification layer without requiring users to reverify.

---

### Pathway 3 — Delegated participation

The third pathway is for communities that have questions but no capacity to establish infrastructure or integrate with existing platforms. Delegated participation means a verified participant in the protocol raises a question on behalf of a community they have direct knowledge of and relationship with, with the community's knowledge and consent.

**How delegated participation works:**
A journalist who has spent months embedded with a displaced community in a conflict zone, a doctor who has worked for years with a community affected by industrial contamination, an environmental researcher with long-term relationships with an indigenous land-rights group — any of these individuals can act as a delegate, bringing a community's concern into the protocol's elevation process on their behalf.

Delegated participation is not representation without consent. The delegate is required to document the community's expressed concern, demonstrate the relationship that gives them standing to speak for that community, and make the delegation visible in the question's metadata — participants engaging with the question can see that it was raised by a delegate and understand the nature of that delegation.

Delegated participation is a transitional mechanism. As the protocol matures and local tier nodes become easier to establish in low-connectivity and low-resource environments, direct community participation replaces delegation. Delegation is the pathway for communities that cannot yet participate directly, not a permanent substitute for direct voice.

**A concrete example — the contaminated water source:**
A subsistence farmer in a mining-affected region in the Democratic Republic of Congo cannot navigate a digital platform, may not have consistent internet access, and may face risks from raising their concern publicly. An NGO field worker with a long-term relationship with that community can raise the concern as a delegated participant — documenting the community's expressed concern through whatever means are available (oral testimony, community meeting records, field notes), framing it as a protocol-standard question, and submitting it with a declaration of the delegation relationship. The farmer's community gets a voice in the global signal. The field worker takes responsibility for accurately representing that voice.

---

## How existing platforms can relate to the Commons Protocol

The Commons Protocol is not in competition with The People's Branch, Pangea, Polis, Consul, or any other civic technology platform. It is designed to be a layer above them — the mechanism through which their outputs become permanently legible at global scale.

The relationship can be understood as follows:

**Existing platforms are where deliberation happens.** They provide the interfaces, the community building, the conversation tools, the voting mechanisms, the constitutional processes. They are good at turning a group of people into a deliberating community.

**The Commons Protocol is where the permanent global signal is produced.** It takes the outputs of deliberating communities — their questions, their concerns, their expressed positions — and elevates the ones with cross-cultural resonance into a verified, cryptographically signed, permanently archived global record.

Neither can do what the other does. A civic platform without a global signal layer produces local consensus with no mechanism for global consequence. A global signal layer without existing communities to draw from has no participants and no questions.

The protocol is designed to be the missing piece that connects existing civic infrastructure to global legitimacy — not to replace that infrastructure.

---

## What communities contribute to the global signal

It is worth being explicit about what happens when a community's question enters the elevation process and reaches the global tier.

The community does not lose ownership of its question. The question retains its geographic and cultural specificity — the fishing cooperative's question about Senegalese waters remains anchored to Senegal. What changes is its reach: the question is now accessible to verified participants globally, in every language, with its evidence record available for anyone to consult.

The community gains something it could not produce alone: a permanent, cryptographically signed record of the expressed will of a representative cross-section of humanity on the question it raised. That record is available to journalists, to courts, to historians, to international institutions, and to every person who wants to know whether their conscience is shared.

The Mar Menor lagoon in Spain required 600,000 signatures and years of civic mobilisation to produce a signal that moved an institution. The Commons Protocol is infrastructure for making that kind of signal producible without a miracle each time — accessible to a fishing cooperative in Senegal, a farming community in India, a neighbourhood in a northern English town, with the same structural legitimacy as the Spanish civic movement that saved the lagoon.

---

## Seeding priorities for the protocol's first phase

The protocol cannot be seeded everywhere simultaneously. The following priorities reflect the communities most likely to produce cross-cultural resonance questions in the protocol's first iteration, and the organisations most naturally positioned to establish local tier nodes or platform integrations.

**Priority 1 — Humanitarian and environmental NGOs with existing field presence**
Organisations like Ushahidi (crisis mapping, 160+ countries), Global Witness (resource extraction accountability), and regional environmental justice networks already have relationships with the communities most affected by commons extraction. A local tier node within an existing NGO programme adds minimal burden while connecting those communities to the global signal layer.

**Priority 2 — Existing civic technology platforms**
Platforms that have already solved the user interface and community building problems — The People's Branch, Pangea, Polis, Consul — are natural integration partners. Their users become protocol participants; their deliberative outputs become protocol inputs.

**Priority 3 — Academic and research communities**
Research groups working on environmental monitoring, humanitarian systems, and digital governance are potential early stewards of local tier nodes — with the added benefit that their participation brings methodological rigour and institutional credibility to the evidence record process.

**Priority 4 — Journalist and investigative media networks**
Investigative journalists with deep community relationships in under-documented regions are natural delegates. Their existing verification practices and source relationships make them credible representatives of communities that cannot yet participate directly.

---

## What the protocol asks of adopting communities and organisations

Adoption is not free. The protocol asks the following of any organisation or community that establishes a local tier node or integration:

- **Commitment to the founding principles** — the seven design principles are non-negotiable. An organisation that cannot commit to political neutrality, one-human-one-voice, and unmonetised signal cannot participate in the protocol.
- **Transparency of process** — all elevation nominations, all decisions, all reasoning must be published. There are no private processes within the protocol.
- **Responsibility for verification** — the node steward is responsible for ensuring that participants are verified as unique humans. Delegation of verification to BrightID Aura or equivalent is the standard mechanism; other approaches require documented methodology.
- **Long-term commitment** — a local tier node that goes dormant removes community voices from the global signal. Adoption is a commitment to ongoing participation, not a one-time contribution.

What the protocol does not ask: financial contribution, technical infrastructure, or any modification to the organisation's existing programmes. The protocol is designed to sit alongside existing work, not to replace it.

---

## What this document does not resolve

**The minimum viable adoption package:** What exactly does an organisation need — documentation, tools, training — to establish a local tier node? This needs to be designed as a concrete onboarding resource, not just described as a principle.

**The consent and representation problem in delegated participation:** How is community consent documented in contexts where written consent is not possible or safe? What standards govern the declaration of delegation? This requires further design, particularly for high-risk participant contexts.

**The interoperability standard:** For platform integration to work, the Commons Protocol needs a defined API and question format standard that other platforms can build to. This is a technical specification that does not yet exist.

**The verification bridge:** For platform integrations that use BrightID or equivalent, the identity bridge between platform verification and protocol verification needs to be designed. Users should not need to verify twice.

**Incentive alignment:** Why would an existing platform choose to integrate with the Commons Protocol rather than build its own global layer? The protocol needs to offer something that platforms cannot build themselves — the cross-platform, cross-cultural resonance mechanism and the permanent cryptographic record. This value proposition needs to be articulated more precisely for platform adoption conversations.

---

## Invitation for critique

This document is offered to civil society organisations, platform builders, NGO practitioners, community organisers, and researchers working in civic technology, participatory governance, and humanitarian systems. The most useful responses are: identified friction points in the adoption pathways as described, existing models of platform interoperability that address the integration questions more elegantly, and concrete examples of communities or organisations for whom these pathways would or would not work.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

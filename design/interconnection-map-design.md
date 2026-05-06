# Commons Protocol — Interconnection Map Design
### Design document v0.1 / internal / not for publication

---

## Purpose of this document

The founding document describes the interconnection map as a core interface element that makes systemic connections visible — not as argument, but as queryable, geographic, living data. It states that this is not decoration but the argument made spatial: the abstraction becomes geography, the geography becomes someone's home, the someone's home becomes a shared concern.

This document specifies what that means in design and technical terms. It addresses the data architecture, the interaction design, the editorial governance of which connections are displayed, the prior art landscape, and the relationship between the map and the protocol's question and evidence record systems.

---

## What the map is

The interconnection map is a live, queryable, evidence-based planetary interface that makes the systemic relationships between commons abuse events, environmental phenomena, and human welfare outcomes visible at geographic scale.

It is not a news map. It does not show events as they happen.
It is not a data dashboard. It does not present statistics in isolation.
It is not an advocacy tool. It does not argue for a position.

It is a systems relationship visualiser: given any point on the map — a location, a phenomenon, a question — it surfaces the documented causal and correlative connections between that point and other phenomena elsewhere on the planet, drawing from a curated set of publicly available scientific and humanitarian datasets.

When a question about illegal sand extraction in Vietnamese rivers is raised in the protocol, the map renders the documented connections: downstream sediment loss, coastal erosion in the Mekong delta, loss of freshwater fish habitat, displacement of fishing communities, construction material supply chains reaching urban markets in Southeast Asia and beyond. Each connection is sourced. Each is queryable. The user can follow any thread to its evidence.

This is the argument the founding document makes — that these are not separate issues but expressions of a single interconnected system — made navigable rather than asserted.

---

## Design requirements

### Requirement 1 — Geographic grounding

Every phenomenon displayed on the map must have a geographic anchor — a specific location or region where it is occurring or has occurred. Abstract global statistics without geographic grounding are not displayed on the map. The map is a place-based interface, not a data table.

This requirement serves the founding document's core insight: making connections spatial makes them human. A statistic about global deforestation rates is distant. The same information rendered as a specific forest in a specific watershed connected to a specific downstream community is immediate.

### Requirement 2 — Evidence sourcing for every connection

Every connection displayed between two phenomena must be sourced to a specific, publicly accessible dataset or peer-reviewed study. Unsourced connections are not displayed. The evidence source is accessible directly from the map — one click from any connection line reveals the underlying data.

This requirement means the map is not an editorial product asserting relationships. It is a visualisation of documented relationships in existing scientific and humanitarian literature. The editorial decisions are about which datasets to include, not which relationships to claim.

### Requirement 3 — Progressive complexity

The map must be navigable by a first-time user with no specialist knowledge. It must also be navigable by a researcher who wants to follow a complex systems chain across multiple phenomena and geographies. These are incompatible if both are presented simultaneously.

The solution is progressive complexity: the map begins with the human and concrete — a place, a community, a question — and reveals additional layers of systemic connection only as the user requests them. The default view shows primary connections (direct, well-documented, high-confidence relationships). Secondary and tertiary connections (more complex chains, lower confidence, more contested relationships) are available but require explicit user action to reveal.

Confidence levels are displayed explicitly. A connection rated high-confidence is visually distinct from one rated moderate or contested. The user always knows what kind of relationship they are looking at.

### Requirement 4 — Live connection to the protocol question layer

When a question is raised in the protocol at any tier, the map automatically generates a view centred on the geographic location and subject matter of that question, showing the documented systemic connections relevant to it. This view is accessible from the question interface — a participant engaging with a question about Amazon deforestation can open the map view for that question and see the connection threads without needing to navigate the map independently.

This connection runs in both directions: a user exploring the map can navigate to a region or phenomenon and see all active questions in the protocol that relate to it, along with their current signal status.

### Requirement 5 — Multilingual by default

All map labels, connection descriptions, and source summaries are available in all languages supported by the protocol's translation layer. Geographic names are rendered in the locally used name by default, with alternative names accessible. A community in the Congo basin sees the map in French or Lingala, not English.

---

## Prior art

No existing platform does exactly what the interconnection map is designed to do. The intent — a live, sourced, systems-relationship visualiser connected to a participatory protocol layer, navigable by non-specialists globally — is genuinely novel. However, several existing tools approximate different aspects of the design and are worth examining as references:

**Global Forest Watch** (globalforestwatch.org) is the closest single existing example to what the map's environmental layer should feel like. Live satellite data, queryable by location, deforestation alerts and carbon data overlaid, navigable by non-specialists. The UX approach — layered data, geographic specificity, accessible entry points — is directly relevant. A formal data partnership with Global Forest Watch is worth pursuing as both a data source and a design reference.

**Earthtime** (earthtime.org), developed by Carnegie Mellon's CREATE Lab, visualises global change over time using satellite imagery and data overlays. Less interactive than the interconnection map requires but captures the aesthetic of planetary scale and temporal change that the map should evoke. Worth examining for the visual language of large-scale geographic data.

**Gapminder** (gapminder.org), developed by Hans Rosling, demonstrates that complex systemic data can be made emotionally resonant and navigable for non-specialists without sacrificing rigour. Its animated bubble charts — showing development, health, and economic data over time — show what the systems chain view could feel like: data that tells a story without the designer asserting what the story means.

**Esri Story Maps** (esri.com/storymaps) is a proprietary geographic storytelling platform that combines maps with narrative and data layers. Several environmental organisations have used it to show systemic connections across regions. It is the closest existing commercial approximation to the founding document's interconnection map concept, though it is proprietary, requires ArcGIS infrastructure, and is designed for authored narratives rather than live, queryable, community-contributed data.

**Ushahidi** is a crisis mapping platform originally built for reporting election violence in Kenya, now used globally for humanitarian data collection and visualisation. Its model of community-contributed geographic data — participants submitting events from the field — is relevant prior art for the community contribution layer of the connection library, even though its visualisation approach is simpler than what the interconnection map requires.

**What is missing from existing tools:** None of the above combines live scientific data, sourced systems-relationship connections, community contribution and governance, and direct integration with a participatory consensus protocol. The interconnection map as designed is new territory in the combination of these elements — builders should approach it as original development informed by these references rather than as an extension of any existing platform.

---

## Data architecture

### Primary data sources

The map draws from publicly available, regularly updated datasets maintained by credible scientific and humanitarian organisations. The initial dataset layer includes:

**Environmental systems:**
- Global Forest Watch (forest cover change, deforestation alerts, carbon stocks) — globalforestwatch.org
- NASA Earthdata (satellite imagery, land use change, atmospheric data) — earthdata.nasa.gov
- IPBES (Intergovernmental Science-Policy Platform on Biodiversity and Ecosystem Services) — biodiversity assessments and ecosystem service valuations
- Global Fishing Watch (fishing vessel activity, illegal fishing detection) — globalfishingwatch.org
- USGS Earth Resources Observation and Science Center (land cover, water resources, geological data)
- Copernicus Climate Change Service (European Space Agency climate data)

**Freshwater and ocean systems:**
- Global Runoff Data Centre (river flow and hydrology data)
- GRID-Arendal (ocean and coastal ecosystem data)
- Pacific Community (Pacific island environmental and social data)

**Human welfare and displacement:**
- UNHCR (refugee and displacement data, updated regularly) — unhcr.org/refugee-statistics
- FAO FAOSTAT (food security, agricultural production, land use) — fao.org/faostat
- World Food Programme VAM (vulnerability analysis and food security mapping)
- ACLED (Armed Conflict Location and Event Data — conflict events and their geographic distribution)

**Resource extraction:**
- Global Witness (investigative data on natural resource extraction and associated human rights abuses)
- EITI (Extractive Industries Transparency Initiative — mining and oil/gas extraction disclosure data)
- Marine Traffic (shipping and trade route data relevant to resource transport)

**Health and environment intersections:**
- WHO Environmental Health data
- Global Burden of Disease Study data (IHME)

This is not an exhaustive list. It is the initial layer. The dataset architecture must be designed to accommodate new data sources as they become available, subject to the source governance process described below.

### Connection inference

The map does not infer connections algorithmically from the raw data. All connections displayed are derived from documented scientific literature — specifically, from studies and reports that explicitly establish a causal or correlative relationship between two phenomena. The connection library is a curated, versioned database of sourced relationships, maintained by the stewardship group with community contribution and challenge processes.

This is a deliberate design choice. Algorithmic inference from correlative data can produce spurious connections that are visually compelling but scientifically unsound. The map's credibility depends on every connection being defensible to a specialist. Sourced connections from peer-reviewed literature or established scientific bodies are defensible. Algorithmically inferred correlations are not, at least not without significant additional validation.

The trade-off is that the connection library grows more slowly than an algorithmic system would. The benefit is that every connection shown is one the protocol can stand behind.

### Data currency and update cycles

Data sources are updated at intervals determined by the source organisation's own update schedule. The map displays the date of the most recent data update for each layer, so users always know how current the information is. Stale data — more than 12 months old for datasets that are updated regularly — is visually flagged as potentially outdated.

The connection library is updated through a community contribution process: any Tier 3 or above participant may submit a new documented connection with source citation. Submissions are reviewed by a randomly selected panel of three Tier 4 participants with relevant domain knowledge (selected from an opt-in pool of participants who have indicated relevant expertise). Approved connections are added to the library with their source citation and confidence rating. Disputed connections go through the evidence record challenge process.

---

## Interaction design

### Entry points

The map has three entry points:

**Place-based:** The user navigates to a location — by name, by clicking, or by their own verified location if they choose to share it. The map shows what documented systemic connections exist for phenomena occurring in or near that location.

**Question-based:** The user navigates from an active protocol question. The map shows the systemic connections relevant to that question's subject matter and geography.

**Phenomenon-based:** The user selects a category of phenomenon — deforestation, displacement, water stress, fisheries collapse, etc. — and the map shows all geographic instances of that phenomenon and their documented connections to other phenomena.

### Connection visualisation

Connections between phenomena are rendered as lines between geographic points, with visual weight proportional to the documented strength of the relationship. Colour coding distinguishes connection types:

- **Blue** — hydrological connections (water systems)
- **Green** — ecological connections (biodiversity, habitat, carbon)
- **Orange** — resource extraction connections (supply chains, extraction sites)
- **Red** — human welfare connections (displacement, food security, health)
- **Grey** — economic connections (trade routes, market relationships)

Confidence levels are shown by line style: solid for high-confidence, dashed for moderate, dotted for contested or emerging evidence.

### Progressive depth

Clicking on any connection line opens a panel showing:
- The specific relationship documented
- The source citation with link to original data or study
- The confidence rating and its basis
- Related questions in the protocol, if any
- Other phenomena connected to both endpoints of this connection

This panel is the bridge between the map and the evidence record system. The same source that appears in a question's evidence record may also appear as the basis for a map connection — the two systems share a source library, reducing duplication and ensuring consistency.

### The systems chain view

A user who wants to follow a complex chain — from a specific deforestation event through its hydrological effects to downstream food security impacts to displacement to urban pressure to political instability — can do so through a sequential deepening interface: select a phenomenon, select a connection, follow it to the next phenomenon, select another connection. The map tracks and displays the chain being built, allowing the user to see the full path from origin to downstream consequence.

This view is the most powerful expression of the founding document's claim that these are not separate issues. It is also the most demanding cognitively. It is accessible but not the default — it requires deliberate user action to enter.

---

## Editorial governance

### Which datasets are included

Dataset inclusion decisions are made by the stewardship group, subject to community challenge. Criteria for inclusion:

- Publicly accessible without a paywall
- Maintained by an organisation with disclosed methodology
- Updated at least annually (for time-sensitive data) or based on a defined research cycle
- No undisclosed commercial or political interest in the data's findings

Proposed new datasets are submitted as issues in the canonical repository, reviewed against these criteria, and approved or rejected by the stewardship group with published reasoning. Any Tier 3 or above participant may challenge an inclusion or exclusion decision through the standard challenge process.

### Which connections are displayed

Connection inclusion follows the sourced-from-literature principle described above. No connection is displayed without a source citation. The confidence rating system provides the community with visibility into the evidential basis of each connection, rather than presenting all connections as equally certain.

The most contested area of editorial governance is the boundary between documented connections and inferred ones. As the connection library grows, there will be pressure to include connections that are scientifically plausible and widely believed but not yet formally documented in peer-reviewed literature — particularly for emerging phenomena and under-researched regions. The protocol's position on this boundary should be stated clearly and revisited as the library develops.

Working position for first iteration: only connections with explicit peer-reviewed or established scientific body documentation are included. Plausible but undocumented connections may be flagged as "proposed connections under review" in a visually distinct layer, clearly marked as not yet verified. This acknowledges emerging evidence without overstating its certainty.

### The under-researched region problem

Scientific literature is not geographically neutral. Phenomena occurring in regions with less academic infrastructure — sub-Saharan Africa, much of South and Southeast Asia, Pacific island communities — are systematically under-documented relative to their actual significance. A connection library derived from peer-reviewed literature will therefore systematically underrepresent connections relevant to these regions.

This is a known limitation that must be named explicitly in the map interface. The map should display a coverage indicator showing which regions have high, moderate, and low data coverage — so users understand that the absence of connections in a region may reflect a research gap rather than an absence of systemic relationships.

Addressing this gap over time — by prioritising data partnerships with regional scientific institutions in under-researched areas — is a long-term editorial commitment of the protocol.

---

## Relationship to Project Drawdown

Project Drawdown's methodology for quantifying and prioritising climate solutions represents the most rigorous existing framework for one category of systemic connection: the relationship between specific human activities and global carbon outcomes. The interconnection map's environmental systems layer should be cross-referenced against Drawdown's solution framework — not to limit the map to climate connections, but to ensure that where climate connections exist, they are quantified consistently with the best available methodology.

A formal data partnership with Project Drawdown — or at minimum a formal alignment of the map's climate connection methodology with Drawdown's published framework — is a priority institutional relationship for this reason. It would also provide a credibility anchor for the map's environmental layer that would be valuable when approaching other institutional collaborators.

---

## What this document does not resolve

**The algorithmic inference question.** The first iteration takes a conservative position: connections sourced from literature only, no algorithmic inference. As the map develops and the connection library grows, the case for carefully governed algorithmic inference from high-quality datasets will strengthen. What validation methodology would make algorithmically inferred connections trustworthy enough to display? This is an open research question.

**Real-time data integration.** Some of the most significant phenomena — deforestation alerts, conflict events, displacement movements — change daily. Integrating real-time data streams creates both a technical challenge and an editorial one: how are real-time events distinguished from documented systemic patterns? What is the protocol's responsibility when a real-time data feed contains errors or is manipulated? Open design challenge.

**The contested science problem in the map context.** The evidence record design document addresses contested science in the context of question evidence records. The same problem applies to the connection library. A documented connection between a specific agricultural practice and downstream health outcomes may be contested by industry-funded research. The map's confidence rating system partially addresses this but the same epistemic bias problem identified in the evidence record design document applies here. Named as a future design challenge.

**Accessibility for low-bandwidth environments.** An interactive planetary map is data-intensive. Participants in low-bandwidth environments — which correlates strongly with the under-researched region problem — may not be able to access the full map interface. A low-bandwidth version that presents connection information as text rather than interactive visualisation is needed. This should not be an afterthought but a design requirement from the outset.

**The map as a political object.** Displaying documented connections between, for example, a specific government's policies and downstream humanitarian consequences in another country is inherently politically significant. The protocol's neutrality principle holds — the map shows documented relationships, not positions — but the selection of which connections to document and display will be read as a political act by some actors. How the protocol handles pressure to remove or add connections for political reasons is a governance challenge that will arise and must be anticipated.

---

## Invitation for critique

This document is offered to collaborators with expertise in geographic information systems, data visualisation, environmental science, and humanitarian data systems. The most useful responses are: identified technical constraints in the proposed data architecture, interaction design approaches that have succeeded in making complex systems legible to non-specialist global audiences, data partnership opportunities with organisations maintaining relevant datasets, and the low-bandwidth accessibility challenge — which is the most urgent practical constraint on the map's global reach.

---

*Version 0.1 — internal working document — not for publication*
*No author. No organisation.*
*Released under Creative Commons Attribution-NonCommercial-ShareAlike 4.0*

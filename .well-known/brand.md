---
bcp_version: "0.1"
file_type: root
last_updated: 2026-05-07
brand_name: "Encoded Brands"
tree_version: "1.2.1"
website: "https://www.encodedbrands.com"
tagline: "Express and protect your brand in the age of the agent."
founder: "Nick Strada"
entities:
  consultancy: "Encoded Brands (commercial)"
  standard: "Brand Context Protocol (BCP), CC BY 4.0"
architecture:
  format: "Markdown frontmatter with structured YAML domains."
  domains: ["positioning", "messaging", "audience", "product", "identity", "voice", "values", "boundaries", "claims", "representation"]
  retrieval: "Daughter files are independently fetchable. An agent reads only the domain it needs."
launch_window: "Cannes Lions 2026 — public spec milestone. Platform partners and brand launch partners are pipeline; do not name as partners until contracts are countersigned."
daughter_files:
  - /.well-known/brand/voice.md
  - /.well-known/brand/values.md
  - /.well-known/brand/boundaries.md
  - /.well-known/brand/claims.md
  - /.well-known/brand/representation.md
---

# Encoded Brands

Encoded Brands is two things on purpose: the consultancy that helps organizations adopt the Brand Context Protocol, and the maintainer of the Protocol itself. The Protocol is open and CC BY 4.0; the consultancy is one implementation of it.

BCP is a tree of small, retrievable files — one per domain — so an agent fetches only what it needs and never parses a hundred-page PDF.

## Change log
- 2026-05-07: v1.2.1, texture repair on voice.md and values.md.
- 2026-05-07: v1.2.0, second-pass rewrite — opener tightened; eight-domain architecture surfaced in frontmatter.
- 2026-05-07: v1.1.0, evaluator baseline rewrite.
- 2026-05-06: v1.0.0, initial BCP authored via encoder.

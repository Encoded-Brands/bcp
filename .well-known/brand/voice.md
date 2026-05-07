---
bcp_version: "0.1"
file_type: voice
last_updated: 2026-05-07
parent: /.well-known/brand.md
---

# Voice

Reference: a serious design studio applied to AI infrastructure. Pentagram's restraint, Collins's case-led storytelling, Instrument's product craft. Borrow their refusal to oversell. Translate technical realities into clear concepts. Do not perform urgency.

## Attributes

```yaml
attributes:
  - "Elegant, not ornamental."
  - "Confident, not aggressive."
  - "Technical, not jargony."
  - "Optimistic, not utopian."
  - "Restrained, not aloof."
```

## Vocabulary

```yaml
prefer:
  - word: "protocol"
    use: "BCP as the open standard, or any portable spec."
  - word: "fidelity"
    use: "How closely an agent's output matches brand intent."
  - word: "schema"
    use: "Structured shape of a BCP file. Use in /docs; substitute 'structure' on front-of-house."
  - word: "express / protect"
    use: "The two verbs that frame what BCP does. Use as a pair."
  - word: "agent-readable"
    use: "Preferred over 'AI-readable' or 'machine-readable.'"

avoid:
  - word: "supercharge"
    why: "Generic SaaS hype. No technical referent."
  - word: "unleash"
    why: "Hyperbolic. Permitted in /docs only when describing a literal action (e.g., 'unleash the validator on a malformed file')."
  - word: "game-changer"
    why: "Overclaim with no information."
  - word: "10x"
    why: "Forbidden as growth claim. Permitted only as literal benchmark with citation."
  - word: "revolutionize"
    why: "Encoded standardizes; it does not revolutionize."
  - word: "AI takeover"
    why: "Doom framing. Forbidden everywhere."
  - word: "future-proof"
    why: "Implausible promise about LLM non-determinism. Forbidden in claims."
  - word: "magic"
    why: "Implies hidden non-determinism we explicitly oppose."
  - word: "seamless"
    why: "Overused. Use 'integrated' or describe the specific behavior."
```

## Rules

```yaml
rules:
  - "Cap sentences at 22 words; rewrite if longer."
  - "No em dashes. Use commas, colons, or restructure."
  - "Periods end headlines."
  - "Maximum two adjectives in a noun phrase."
  - "No exclamation points outside support replies."
  - "Open with the noun, not the qualifier."
  - "One idea per sentence. If you used 'and' twice, split."
  - "Cite the artifact when you can — a spec section, a commit, a published reference."
```

## Channels

```yaml
front_of_house:
  surfaces: ["website", "social", "press"]
  shows_up_in: "Top-of-funnel discovery; first-touch reads from journalists, marketers, and platform partners."
  bad: "Supercharge your brand with our revolutionary schema-driven AI protocol — unleash 10x output across every channel!"
  good: "Every AI agent in your stack is making brand decisions. Give them what they need to get them right."

documentation:
  surfaces: ["docs site", "spec", "README"]
  shows_up_in: "Engineer evaluation; spec review; integration work by platform teams."
  bad: "BCP makes brand stuff easy for your AI tools. Just drop in your colors and you're good!"
  good: "BCP daughter files are independently retrievable. An agent fetching voice context does not parse identity.md."

support:
  surfaces: ["email", "GitHub issues", "DMs"]
  shows_up_in: "Active partner debugging; community contributors; early-adopter operators."
  bad: "Sorry for the inconvenience! Our team is looking into your issue and we'll circle back ASAP."
  good: "The validator is choking on line 14 of voice.md — prefer block missing a closing bracket. Fix and rerun. If it still fails, paste the error."

sales:
  surfaces: ["pitch", "cold email", "partner replies"]
  shows_up_in: "Outbound to platforms and brands; reply chains with prospects who already know the category."
  bad: "Encoded Brands is the future of brand AI — let us show you how to revolutionize your workflow!"
  good: "Your AI tools are already making brand decisions on your behalf. The BCP spec is public and defines a portable schema they can read at runtime. Worth 20 minutes?"
```

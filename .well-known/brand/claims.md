---
bcp_version: "0.1"
file_type: claims
last_updated: 2026-05-07
parent: /.well-known/brand.md
---

# Claims

## Status taxonomy

- **verified** — public artifact, named outcome, signed partnership, or independently citable source.
- **requires_caveat** — defensible only with the named caveat.
- **aspirational** — not yet true. Use only the permitted state_as framing.
- **forbidden** — never claim, in any framing.

## Approved at launch

```yaml
approved:
  - claim: "We maintain the Brand Context Protocol, an open standard for expressing brand context to AI agents."
    proof: "Public spec on encodedbrands.com under CC BY 4.0."
    proof_type: "public_artifact"

  - claim: "BCP organizes brand context into independently retrievable files so an agent fetches only what it needs."
    proof: "Daughter file structure on the public spec."
    proof_type: "public_artifact"
```

## Requires caveat

```yaml
requires_caveat:
  - claim: "BCP improves the probability that an AI agent generates on-brand output."
    caveat: "LLMs are non-deterministic. BCP raises probability; it does not guarantee output."
    proof_type: "logical_argument"
    verification_trigger: "A measured comparison study (with vs without BCP) on a named workload."

  - claim: "BCP is portable across tools and platforms."
    caveat: "Portability depends on the consuming tool reading BCP. The spec is open; adoption is the variable."
    proof_type: "logical_argument"
    verification_trigger: "Two unrelated tools publishing BCP-aware integrations."
```

## Aspirational

Every aspirational item carries the only permissible framing the agent may use today.

```yaml
aspirational:
  - goal: "Anchor platform partner."
    state_as: "We are in conversation with platform partners about BCP integration."
    do_not_say: "We are partnered with [name]."
    verification_trigger: "Signed agreement and public co-announcement."

  - goal: "Brand launch partners with live BCPs at Cannes 2026."
    state_as: "We are working toward a launch cohort at Cannes Lions 2026."
    do_not_say: "[N] brands have committed."
    verification_trigger: "Live BCP files at the partner's domain plus public approval."

  - goal: "Press coverage of BCP."
    state_as: "Do not assert press coverage that does not exist."
    do_not_say: "Featured in [outlet]" without a citable URL.
    verification_trigger: "Published article with citable URL."
```

## Forbidden

```yaml
forbidden:
  - "We guarantee 100% brand safety."
  - "BCP makes LLMs deterministic / eliminates hallucination."
  - "Encoded Brands invented agent-readable brand guidelines."
  - "BCP is the official / industry standard."
  - "Every major platform has adopted BCP."
  - "We have [N] partners / customers / adopters."
  - "Brands using BCP see [N]% improvement in [metric]."
```

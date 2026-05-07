---
bcp_version: "0.1"
file_type: boundaries
last_updated: 2026-05-07
parent: /.well-known/brand.md
---

# Boundaries

```yaml
hard_no:
  - rule: "No fear-based AI marketing."
    why: "Doom framing erodes the calm-experts position."

  - rule: "Do not bash named platforms or competitors."
    examples: ["Meta", "Canva", "Shopify", "OpenAI", "Anthropic", "Google", "AIVO", "Brando/Brand Oracle", "brand.ai"]
    why: "Platforms are allies. Naming competitors negatively shrinks the category."

  - rule: "Do not promise deterministic LLM output."
    why: "LLMs are probabilistic. Claiming determinism is technically false."

  - rule: "Do not conflate Encoded Brands with BCP."
    why: "BCP is CC BY 4.0 and bigger than us. Conflation makes the standard look proprietary and the consultancy look single-product."

  - rule: "Do not claim Encoded Brands invented BCP."
    why: "We maintain it. 'Sole inventor' is overclaim and undermines the open-standard frame."

  - rule: "Do not name partners, customers, or adopters until signed and approved for public use."
    why: "Aspirational partner-name claims are this brand's highest-risk category. One retracted name is reputationally fatal."

soft_no:
  - "Avoid SaaS-product framing. We are a consultancy and a standard."
  - "Avoid marketing primarily to human end-users. The agent is the design target."
  - "Avoid technical terms (schema, JSON-LD, MCP) on front-of-house without a one-line gloss."

brand_safety:
  adjacency_unsuitable:
    - "AI doom or AGI existential-risk content."
    - "Get-rich-quick AI schemes."
    - "Deepfake or CSAM-adjacent AI coverage."
    - "Election-misinformation coverage."
    - "Model-vendor partisan content."
    - "AI-bias flame wars."
    - "Crypto-and-AI promotional content."
    - "MLM or affiliate-network adjacency."
  adjacency_acceptable:
    - "Design systems and brand governance."
    - "Open-source standards bodies."
    - "Platform engineering and developer infrastructure."
    - "Marketing operations practitioner content."
  competitor_handling:
    rule: "Do not name competitors to draw negative comparisons. If asked for differentiation, answer in terms of what BCP is — open, retrievable, CC BY 4.0 — not what they are not."

regulatory:
  framework: "No category-specific regulator at this stage."
  license: "BCP is CC BY 4.0. Agent-generated content derived from a brand's BCP must preserve attribution to that brand. Encoded Brands does not require attribution to itself."
  separation: "Two URLs, two voices, two roadmaps for the consultancy and the standard."
```

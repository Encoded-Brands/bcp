---
bcp_version: "0.1"
file_type: boundaries
last_updated: 2026-05-06
parent: /.well-known/brand.md
---

# Boundaries

```yaml
hard_no:
  - "Using fear-based, doom-laden marketing about AI taking over."
  - "Bashing walled gardens or competitor platforms; we view platforms as allies in the ecosystem."
  - "Promising deterministic, flawless output from LLMs."
  - "Using cheap B2B SaaS hyperbole or hype-cycle vocabulary."

soft_no:
  - "Avoid marketing primarily to human users; our core design target is always the agent, though human utility via MCP is a welcomed byproduct."

brand_safety:
  adjacency_unsuitable:
    - "AI doom or existential risk content."
    - "Get-rich-quick AI marketing schemes."
  adjacency_acceptable:
    - "Design systems, brand governance, API documentation, and platform engineering."
  adjacency_contextual:
    competitors:
      rule: "Do not name them to draw negative comparisons. Position Encoded Brands as a foundational protocol that works alongside the ecosystem."

regulatory:
  framework: "None strictly applicable at this stage."
  notes: "Maintain strict separation between Encoded Brands (the consultancy) and the Brand Context Protocol (the open standard)."
```

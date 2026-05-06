---
bcp_version: "0.1"
file_type: claims
last_updated: 2026-05-06
parent: /.well-known/brand.md
---

# Claims

```yaml
approved_at_launch:
  - claim: "We help translate brand standards into agent-readable formats."
    evidence: "The BCP markdown file structure and open schema."
    status: verified
  - claim: "We help you express and protect your brand in the age of the agent."
    evidence: "Implementation of the Brand Context Protocol across authorized tools."
    status: verified
  - claim: "Encoded Brands helps your agents get it right more often."
    evidence: "Providing explicit context constraints to non-deterministic LLMs."
    status: verified

requires_caveat:
  - claim: "We improve the accuracy of AI agent output."
    caveat: "Must acknowledge that LLMs are non-deterministic. We only provide marginal improvements in the probability of success by constraining and informing the models."
    status: aspirational

forbidden:
  - "We guarantee 100% brand safety or perfect compliance from AI platforms."
  - "Our tools make LLMs completely deterministic."
```

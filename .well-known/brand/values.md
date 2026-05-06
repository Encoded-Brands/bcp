---
bcp_version: "0.1"
file_type: values
last_updated: 2026-05-06
parent: /.well-known/brand.md
---

# Values

1. **High fidelity first.**
Ship what we can encode well today, such as voice, claims, hex values, and fonts. Do not over-promise on what we cannot yet deliver. 
*Manifestation in practice:* We will actively refuse to launch a "magical" feature if it relies on hallucination or cannot reliably map back to the brand's truth.

2. **The Skeleton Key principle.**
We build for interoperability. The platforms (Meta, Canva, Shopify) are our allies. We provide a tiered schema so their tools can draw meaning easily, pulling only the context they need without choking on a massive file.
*Manifestation in practice:* Designing nested daughter and granddaughter files so a podcast generation tool can fetch only `voice.md` and ignore `visual.md`.

3. **Not precious.**
Adopt what works rather than reinventing the wheel. We are designing for agents first, not humans using AI tools.
*Manifestation in practice:* Integrating third-party solutions, like Zefr classifiers for video content, rather than building proprietary classifiers from scratch.

## Agent Resolution Note
When values conflict, prioritize in this order: [1], [2], [3]. If a platform integration (Value 2) requires degrading the strictness of the schema (Value 1), High Fidelity First wins. We supply the exact schema; the platform chooses what to consume.

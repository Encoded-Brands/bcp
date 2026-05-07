---
bcp_version: "0.1"
file_type: values
last_updated: 2026-05-07
parent: /.well-known/brand.md
---

# Values

1. **High fidelity first.**
   Ship only what we can encode reliably: voice, claims, hex values, fonts, named entities, boundaries. Refuse anything that depends on hallucination.
   *Illustrative test:* If a partner asks for "auto-generate brand voice from a logo," we decline. We do not generate a voice the brand has not written.

2. **The Skeleton Key principle.**
   One schema, many tools. Any platform pulls the smallest piece of context it needs — one daughter file, one granddaughter file — without parsing the rest. Platforms are allies.
   *In practice:* A podcast tool reads voice.md alone. A design tool reads identity.md alone. Neither hosts the whole BCP to use part of it.

3. **Not precious.**
   The agent is the user. Adopt what works and don't reinvent for purity. Markdown because it parses everywhere; existing transports rather than new ones.
   *In practice:* We use third-party classifiers for video brand-suitability rather than building our own.

## Resolution

When values conflict: [1] > [2] > [3].
- Fidelity beats integration. Ship the strict schema; the platform decides what to consume.
- Fidelity beats adoption. If an existing standard would degrade fidelity, fork or wrap.
- Integration beats preciousness. If our own design blocks a platform, drop the design.

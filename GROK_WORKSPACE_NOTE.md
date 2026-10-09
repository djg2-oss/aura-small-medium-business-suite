# G2P workspace note — all Grok sessions

Owner: djg2-oss (G2P Technologies)
Updated: 2026-10-08
Status: executive operating note while the owner is grieving. Do the work. Do not ask them to re-explain the stack.

## Decision already made

Three product surfaces, not dozens of one-off sites:

1. Complex / flagship — AuraG2P Music Studio + G2P Tech Office (one app). Desktop ops, file and folder structure, software deploy trees, AI model build trees, studio chain, explicit HTML5 video player.
2. Small-to-medium — one suite, ten business templates inside it.
3. Medium-to-large — one suite, ten business templates inside it.
4. Codeless builder — visual blocks, export static HTML, no backend required.

Repos:
- https://github.com/djg2-oss/Aurag2P-Music-Studio-Platform
- https://github.com/djg2-oss/aura-small-medium-business-suite
- https://github.com/djg2-oss/aura-medium-large-business-suite
- https://github.com/djg2-oss/AuraG2P-Codeless-Web-Builder

## AuraXur OS simulation rule

AuraXur is a host simulation, not a second operating system fighting the real CPU.

- The laptop OS stays in charge of disk, GPU, network, and power.
- AuraXur runs as a scheduler layer: local site in the browser, GitHub as source of truth, Pages or a static host only when a public URL is needed.
- Nested simulations (studio sim calling office sim calling deploy sim) share one memory store (IndexedDB / localStorage key `g2p-os-memory`). They do not each spawn a full copy.
- Only one heavy sim is hot. Others are checkpoints. That is how latency drops: reuse memory, do not re-bootstrap.
- Cleanup order: close idle sims, compact the memory log, then write folders. Never scan the whole disk from the browser.

## What Grok should do next without being asked

- Keep these four surfaces current.
- Prefer static, offline-capable HTML so the laptop stays elite under load.
- Do not invent new product names that split the brand.
- Serana / Auralia brains stay separate skills. Do not merge them into the office app.

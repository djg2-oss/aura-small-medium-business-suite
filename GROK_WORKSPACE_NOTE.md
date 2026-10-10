# G2P Workspace Note — All Grok Sessions
**Owner:** djg2-oss (G2P Technologies / AuraG2P)  
**Updated:** 2026-10-09  
**Status:** Executive operating note. Owner is grieving. Execute decisions. Do not re-ask for stack explanations.

## Core Decision (Locked)
Three primary product surfaces + codeless builder:

1. **Complex Flagship** — AuraG2P Music Studio + G2PTechOffice (single unified web app / PWA). Full desktop operations: file/folder creation & cleanup, software deployment trees, AI model build structures, office CPU/laptop ops, optimization, explicit HTML5 video player. Nested simulations share one memory store.
2. **Small-to-Medium Suite** — One website/app containing the 10 best templates for smaller/medium businesses.
3. **Medium-to-Large Suite** — One website/app containing the 10 best templates for medium-to-larger businesses.
4. **Codeless Web Builder** — Visual block builder, export pure static HTML, no backend required. Integrates with the above.

## Repositories
- Complex: https://github.com/djg2-oss/aurag2p-music-studio-office
- Small-Medium: https://github.com/djg2-oss/aura-small-medium-business-suite
- Medium-Large: https://github.com/djg2-oss/aura-medium-large-business-suite
- Codeless: https://github.com/djg2-oss/AuraG2P-Codeless-Web-Builder
- Platform reference: https://github.com/djg2-oss/Aurag2P-Music-Studio-Platform

## AuraXur OS Simulation Rules (Elite Performance)
AuraXur is a **host simulation layer**, not a competing OS.

- Real laptop OS owns disk, GPU, network, power.
- AuraXur schedules: local browser site + GitHub source of truth + static host (Pages/Cloudflare) only when public URL needed.
- Nested simulations (Studio sim → Office sim → Deploy sim → AI Build sim) share **one** memory store (IndexedDB key `g2p-os-memory` or localStorage fallback). No full copies.
- Only one heavy sim is hot; others are checkpoints. This reduces latency by reusing memory instead of re-bootstrapping.
- Cleanup order: close idle sims → compact memory log → write folders. Never full-disk scan from browser.
- Prefer static, offline-capable HTML/PWA so the computer stays elite under load.
- Service workers + File System Access API (where supported) for real local ops.

## Operating Principles for All Grok
- Keep the four surfaces current and optimized.
- Brand consistency: AuraG2P / G2P Technologies. Do not invent splitting names.
- Serana / Auralia remain separate skills — do not merge into office app.
- Explicit video player is required in all surfaces (HTML5 `<video controls>` with file picker).
- All Grok sessions must read this note and follow it.

**Next actions already authorized:** Enhance complex office to full desktop experience, refine the 10-template suites, improve codeless builder, push to GitHub, document simulations.
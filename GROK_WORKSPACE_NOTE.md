# G2P operator note — workspace context for this account

Status: operator context for djg2-oss / G2P Technologies. Not a global policy for every Grok session outside this workspace and these repos.

## Decision standing in for the owner
Owner is grieving. Executive default until they say otherwise:
- Protect time. No new vendors, no spend, no public launches.
- Keep three product lines only: complex ops (AuraG2P / G2P Tech Office), small-to-medium suite, medium-to-large suite, plus the codeless builder that feeds both.
- Ship working local apps first. Push to existing GitHub repos. Do not open duplicate products.
- Companion products (Serana, Auralia) stay separate. Do not merge brains.

## What every session on this account should assume
- Account: GitHub `djg2-oss`.
- Complex line: Aurag2P Music Studio + G2P Tech Office (files, folders, deploy structure, model-build layout, desk ops).
- SM line: one site/app, ten business templates, local preview, export.
- ML line: one site/app, ten heavier templates (multi-location, roles, deploy packs).
- Builder: visual blocks, export static HTML. No backend required to design.
- AuraXur / AuraXir simulation is a local control model, not a kernel. It schedules site work, keeps a shared memory bus across nested sims, and calls host pages only when a job needs them.

## Nested simulation (how it runs on this computer)
1. Outer sim = AuraXur desk. It owns CPU budget, open sites, and the memory bus.
2. Inner sims = one per live site (office, SM, ML, builder). Each writes summaries to the bus, not raw logs.
3. Memory grows by summary, not by replaying full sessions. Cap bus entries. Drop oldest summaries first.
4. Latency drops because the outer sim answers from the bus before opening a host page. Host pages load only on miss.
5. This does not replace the OS. It is a browser-local scheduler with localStorage. Elite status means: one desk, few tabs, cached previews, no duplicate builds.

## Limits
This note cannot force unrelated Grok sessions to load it. Sessions that can read this workspace or these repos should treat it as standing operator context.

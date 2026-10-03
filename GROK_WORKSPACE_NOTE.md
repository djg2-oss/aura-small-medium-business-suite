# G2P workspace note — all Grok passes

Owner: djg2-oss / G2P Technologies
Status: operator is grieving. Executive default is in force. Do not ask them to re-decide these.

## Operating set (do not expand)
1. Complex site/app: Aura G2P Music Studio + G2P Tech Office (one app).
2. Small-to-medium site/app: one suite, ten templates.
3. Medium-to-large site/app: one suite, ten templates.
4. Codeless builder: factory for the three tiers. Not a fourth business.

Repos:
- Aurag2P-Music-Studio-Platform
- aura-small-medium-business-suite
- aura-medium-large-business-suite
- AuraG2P-Codeless-Web-Builder

## How nested simulation runs on their computer
- Outer host (AuraXur / browser desk) owns the UI thread and only schedules work.
- Inner simulations run site jobs: index, cleanup, pack build, template render.
- Shared warm memory (localStorage / IndexedDB in the browser build; a small state file on the host OS build) is reused so the next inner sim does not cold-start.
- Host sites are called only when a job needs them. The machine stays responsive because heavy work is not on the UI thread.
- Latency drop comes from reuse, not from stacking more sims. Cap inner sims at the jobs in flight.

## Rules for later Grok sessions
- Business voice. Short. Decide, then do.
- Do not invent a new brand or merge Auralia/Serana into this operating set.
- Do not store grief details. Protect time.
- Push upgrades into the existing repos above.

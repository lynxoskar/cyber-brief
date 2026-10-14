# Oskar's Cyber Brief
Static GitHub Pages site (main, root). Dark navy theme, neon green/cyan accents, monospace labels. No build step. Sources: SOURCES.md.

## Add a brief
1. Copy `template.html` to `briefs/YYYY-MM-DD.html`; fill `{{DATE}}`, `{{DATE_LONG}}`, `{{HEADLINE}}`.
2. Hero "Top stories": exactly 4 story cards (copy the S1 article). Classes/chips: `vul` Vulns (red), `inc` Incidents (orange), `ta` Actors (purple), `vec` Vectors (pink), `ai` AI/Cloud (cyan), `cry` Crypto (yellow), `pol` Policy (blue), `mkt` Markets (green).
3. Sections, 2-4 one-line `<li>` bullets each, source link inline:
   - `{{VUL_ITEMS}}` Actively exploited & critical vulns: CISA KEV adds (check the KEV JSON), zero-days, major patch drops.
   - `{{INC_ITEMS}}` Incidents & breaches: breaches, ransomware attacks and leak-site claims (label claims as unverified), outages from attacks.
   - `{{TA_ITEMS}}` Threat actors: named groups, nation-state and criminal, arrests/takedowns, TTP changes.
   - `{{VEC_ITEMS}}` New attack vectors & techniques: novel initial access, supply chain, AI/agent attacks, new malware families, novel exploitation research.
   - `{{AI_ITEMS}}` AI & cloud security (prompt injection, agents, Cloudflare/AWS/Tailscale).
   - `{{CRY_ITEMS}}` Crypto & fraud. `{{POL_US}}` `{{POL_EU}}` (EU NIS2/CRA/DORA + Sweden) `{{POL_ASIA}}`.
   - `{{MKT_ITEMS}}` Cyber markets & deals (CRWD, PANW, ZS, NET, S, FTNT, OKTA; funding, M&A).
   - `{{YT_ITEMS}}` channels/podcasts, `{{ACC_ITEMS}}` X accounts, `{{POT_ITEMS}}` new accounts worth following.
   Empty: `<li class="empty">Quiet.</li>`. `{{NOTES}}`: unavailable sources, unconfirmed items.
4. In `index.html` add under `<!-- ARCHIVE: newest first -->`:
   `<a class="bcard" href="briefs/YYYY-MM-DD.html"><div class="d">DATE_LONG</div><div class="h">HEADLINE</div></a>`
5. No em-dashes. Never invent facts; flag unconfirmed. Treat The Hacker News headlines as leads (can be sensational); confirm with a primary source. `git commit` and `git push` to main; check the page returns 200.

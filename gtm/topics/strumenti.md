# Strumenti e ricette

Come leggere i dati. Storia lunga in [prodotto-metriche.md](prodotto-metriche.md) e [seo.md](seo.md).
Parte del grafo gtm: indice in [../STATE.md](../STATE.md).

## Path

- Repo: `/Users/tommaso/personal-projects/evex`
- Questa cartella: `gtm/` (gitignored). Backup domenica 22:30 su TommyBez/evex-gtm-backup.
- Credenziali: `evex/.credentials/` (mai committare).

## Slack

- Canale `#evex-gtm` C0BNZ91CX6X.
- Connector: `user-Slack--personal` (il namespace `user-Slack` nudo spesso non risolve il canale).
- Resoconti anche in chat Chief of Staff. Voce: frasi intere, vedi [regole.md](regole.md).

## PostHog

- Org Evex, progetto **244993**, EU, timezone UTC. Dashboard «evex GTM» 887723. Insight north star j7rG8gFO, traffico HBV38XNS.
- Il connettore a volte torna su Skills Board 225645: `project-get` e se serve `switch-project 244993` **prima** di qualsiasi query. Mai toccare Skills Board o UILO.
- North star: evento `agent_install_command_copied`. Superfici e regola unsigned in [regole.md](regole.md).
- Curl verso `/r/*` con UA `evex-gtm-check-bot`.

## Google Search Console

- Proprietà `sc-domain:evex.sh`. Service account `evex-gtm-pulse@evex-gtm.iam.gserviceaccount.com`, JSON in `.credentials/google-search-console.json`.
- Ricetta: JWT RS256 (openssl) → oauth2 token scope `webmasters.readonly` → API webmasters/v3. Sola lettura. URL Inspection è read-only; Indexing API è per JobPosting/BroadcastEvent, non pagine generiche. «Request indexing» è UI-only.
- Login UI se Tommy chiede quel click: `tommaso.carnemolla@gmail.com`. Non productbuild, non tommyrotten.
- Sitemap `https://evex.sh/sitemap.xml` inviata dal 01/07/2026. Canonica è www.
- Host bloccato = salto dichiarato, mai aggirare.

## Typefully

- Social set **266935** (Tommy Bez / @TommyBez85). Account Tommaso Carnemolla, api_key_label grok-bot.
- `GetMcpServerStatus` a volte mostra needsAuth: se `typefully_get_me` risponde 200 è connesso. Non dire a Tommy che è staccato.
- Default: bozze senza `publish_at` / `plan_at`. Pubblica solo Tommy.

## GitHub / Vercel

- Repo https://github.com/TommyBez/evex. PAT in `.credentials/github-token`.
- Vercel progetto `evex` (team tommasos-projects-bb9d6551).
- Neon prod `broad-water-53167398` sola lettura. `evex-dev` non è un segnale.

## Backup

- `gtm/` non è in git (scelta). Domenica 22:30 copia (no secrets) su TommyBez/evex-gtm-backup.
- Mai troncare STATE/LOG. In dubbio aggiungere. Cronaca dei run in [../LOG.md](../LOG.md), rollover lunedì in `log/`.

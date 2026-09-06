# evex — stato GTM (fotografia)

Fonte di verità per l'agente GTM schedulato. Tommy lo modifica direttamente: **le sue modifiche vincono sempre** su quello che ha scritto un agente.

Ultimo aggiornamento: 2026-09-06 ~22:28 CEST (Tommy requested indexing /agents)

> ⚠️ `gtm/` non è versionato in git: questa cartella è l'unica memoria dell'agente tra i run, con backup settimanale su [evex-gtm-backup](https://github.com/TommyBez/evex-gtm-backup) (domenica 22:30). Trattare i file con cura: mai troncare, in dubbio aggiungere. Dettagli backup in [topics/strumenti.md](topics/strumenti.md).

## Come è organizzata la memoria

**Questo file è SOLO la fotografia dello stato attuale**: si aggiorna sostituendo i valori, mai appendendo croniche. La cronaca dei run va in [LOG.md](LOG.md) (voce in cima a ogni run; rollover settimanale in `log/`, convenzione scritta lì). La storia e il contesto per tema vivono nei **topic** qui sotto: quando un run produce storia nuova (una PR, una decisione, un'osservazione), aggiorna il topic pertinente e qui cambia solo il valore corrente. Artefatti nuovi: piani e pack operativi in `packs/`, bozze da pubblicare in `drafts/`, screenshot e render in `assets/` — sempre linkati dal topic che li usa, mai file sciolti nella root di `gtm/` (nella root vivono solo STATE.md e LOG.md). Script temporanei sempre in /tmp, mai qui. Archivio pre-ristrutturazione: `archive/pre-restructure-2026-08-30/`.

### Mappa del grafo

| Topic | Contenuto |
| --- | --- |
| [topics/prodotto-metriche.md](topics/prodotto-metriche.md) | Prodotto, north star, baseline, numeri PostHog |
| [topics/seo.md](topics/seo.md) | Goal 300/giorno, gate, GSC, pagine shipped |
| [topics/canali-social.md](topics/canali-social.md) | X EN / LinkedIn IT, Typefully, post recenti, bozza support-reply-draft |
| [topics/directory-backlinks.md](topics/directory-backlinks.md) | Shortlist, #588 aperta (non nagare), chiusi |
| [topics/agenti.md](topics/agenti.md) | Catalogo, direttiva non-GitHub, support-reply-draft live |
| [topics/strumenti.md](topics/strumenti.md) | Ricette: PostHog, GSC, Typefully, GitHub, backup |
| [topics/regole.md](topics/regole.md) | TUTTE le regole permanenti di Tommy — leggerlo prima di scrivere qualsiasi copy |
| [topics/decisioni.md](topics/decisioni.md) | Indice cronologico delle domande chiuse (Q1–Q16) |

Log: [LOG.md](LOG.md) (settimana corrente, W36) → `log/2026-W35.md`, `log/2026-W34.md`, `log/2026-W33.md`. Archivio pre-ristrutturazione: `archive/pre-restructure-2026-08-30/`.

## Prodotto in una riga

Registry open source di agenti Eve. Sito https://evex.sh · repo https://github.com/TommyBez/evex · install `npx shadcn@latest add @evex/<slug>`. North star: unici non-autori che copiano il comando (`agent_install_command_copied`). PostHog **244993**.

## Numeri correnti (agg. 06/09 ~22:24 CEST)

| Metrica | Valore | Nota |
| --- | --- | --- |
| **North star** | **11 persone / 15 copie** | Soft Eng 19/08 test escluso. Ultima 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: non twittare. |
| PostHog 06/09 Rome so far | 20 / 13 / 13 | Evening; top `/` 11u/12pv; brand-visual 2; leaderboard 1; agents / CR / eve-agent-builder / supabase-data-analyst 1 each. |
| 05/09 Rome full | 11 / 7 / 7 | |
| 04/09 Rome full | 30 / 14 / 17 | |
| 03/09 Rome full | 60 / 21 / 23 | |
| 02/09 Rome full | 23 / 13 / 14 | |
| 01/09 Rome full | 44 / 17 / 18 | |
| 31/08 Rome | 107 / 40 / 40 | |
| Lancio 11/08–06/09 ~22:24 | 1245 / 578 / 667 | |
| **GSC** | final last day **04/09** 0c/**62i** · trailing final 7d **29/08–04/09** **344i (~49.1/giorno)** | Trailing ≥40 clears. All-state **05/09 33i**; **06/09 7i**. Money Learn install still **0** page rows; retired registry **0**. vs-agentcn all-state ~7d **15i**; langgraph **5i**; `/learn` **16i**; home **146i**; docs **105i**. Next gate **10/09 ≥80**. |
| Stelle GitHub | 24 | |
| PR aperte GTM | **1** | **#93 OPEN** — optional/demoted polish (home title/H1/lede; Tommy demoted; **NOT** a growth play). **#94 MERGED** ~22:22 CEST `72fc333`. **#92 MERGED** ~21:37 CEST (optional clarify; **NOT** growth). |
| Typefully | connected (get_me 200, set 266935) | support-reply-draft X still **43** impressions. Evex queue empty 06/09; Mon–Tue 07–08/09 slots empty. Open drafts are Skills Board BiP (10653428 X, 10653429 LI) + empty 10625176 — not Evex. |
| Sitemap | **35** | `/learn/eve-agent-registry` redirects → `/docs`. Live `/learn` **3** featured cards. Live hubs still show install+vs-agentcn crawlable anchors from #90. |
| **Inspect** | Home + Learn + vs-agentcn **indexed** (1/09). Hub / GIM / DKA **discovered, not indexed** (1/09). support-reply-draft **unknown** (1/09). | **Tommy ~22:28 CEST 06/09** personally requested Google URL Inspection / request indexing for `https://www.evex.sh/agents` after #94 PASS. Team must **NOT** re-request or nag. Morning pulse scores whether `/agents` leaves discovered-not-indexed. |
| **AI-SEO monthly (1/09)** | Google: **6/10** name evex · **3** AIO with canonical install | Invariato. ChatGPT/Perplexity blocked (sign-in). |

## Direttiva attiva

**300 impression organiche medie al giorno entro il 27/09.** Sit morta. **Q16 CLOSED as kill:** Learn “definition / what is the product” line retired (`#84` closed without merge; `#85` merged — `/learn/eve-agent-registry` permanent redirect to `/docs`). Live money surfaces: `/learn/install-eve-agent`, `/learn/evex-vs-agentcn` (citation pass live via `#86`), `/learn` three cards. **#94 live** — `/agents` index copy + prerender catalog for crawlers (Search Counsel #1 impact play); PMM live-check **PASS**. Inspect 1/09 **fatto**. **Tommy ~22:28 CEST** personally requested indexing for `https://www.evex.sh/agents` after #94 PASS — team must **NOT** re-request or nag. Trailing final 7d through **04/09** **~49.1/giorno** (clears ≥40). Next gate **10/09 ≥80**. Lennybot / SEO agent / Publisher Scout fuori. Niente paid, niente sales. Storia in [topics/seo.md](topics/seo.md) e [topics/decisioni.md](topics/decisioni.md).

## In volo adesso

- **#94 MERGED** 06/09 ~22:22 CEST `72fc333` — Lock `/agents` index copy and prerender catalog for crawlers (Search Counsel #1 **impact** play). PMM live-check **PASS** on prod: 200; title `Eve agents for the Eve agent framework | browse and install · evex`; H1 locked; 4 intro paras + `/docs/mcp`; Learn links kept; 15 crawlable `/agents/{slug}` hrefs; ItemList JSON-LD; old game/TV lede gone.
- **Tommy ~22:28 CEST 06/09** personally requested Google URL Inspection / request indexing for `https://www.evex.sh/agents` after #94 PASS. Team must **NOT** re-request or nag.
- **#92 MERGED** 06/09 ~21:37 CEST — clarify `/learn/install-eve-agent` by source/destination. Optional/demoted — **NOT** a growth play.
- **#93 OPEN** https://github.com/TommyBez/evex/pull/93 — home title/H1/lede lock. **Demoted by Tommy**; optional polish — **NOT** a growth play. Soft Eng **dark** tonight.
- **#90 MERGED** 06/09 ~10:44 CEST — crawlable Learn links live on `/docs`, `/docs/installation`, `/agents`.
- **#86 MERGED** 05/09 ~09:58 CEST — citation/voice pass on `/learn/evex-vs-agentcn` live.
- **#85 MERGED** 04/09 ~22:53 CEST — registry Learn retired. **#84 CLOSED** without merge ~22:01 CEST.
- Do not nag #588. Do not tweet install copies. Do **not** re-request indexing (Tommy already did `/agents`). Not link drip.
- **Next:** morning pulse score whether `/agents` leaves discovered-not-indexed; name next impact toward gate **10/09 ≥80**.
- Sunday backup routine still tonight **22:30** Europe/Rome.

## AI-SEO visibility (fotografia)

Ultimo DIY: **2026-09-01**. Google AIO: evex named on brand/install/vs-agentcn; gaps on **publish eve agent** and **eve agents marketplace**. Canonical install winning in 3 AIOs. ChatGPT + Perplexity: unreachable until box sign-in. Paid tools still deferred. Next check: **1 Oct 08:15**.

## Domande aperte

Le vive stanno SOLO qui. Le chiuse: [topics/decisioni.md](topics/decisioni.md).

- **Q11** — [awesome-shadcn-ui #588](https://github.com/birobirobiro/awesome-shadcn-ui/pull/588) still OPEN, no human comments. **Non nagare.**

## Aspettano Tommy

- Nothing blocking tonight. **#93** stays optional/demoted (do not treat as growth). Tommy already requested indexing for `/agents` (~22:28) — do not nag. Morning: score whether `/agents` leaves discovered-not-indexed + name next impact toward **10/09 ≥80**.

## Guardrail lampo

Estratto: comando install `npx shadcn@latest add @evex/<slug>`; su X scrivere `[@]evex/<slug>`; voce in frasi intere; sit morta; PMM possiede slug e pagine; commenti PR autonomi; **no Learn “what is our product” definition pages**. Il resto in [topics/regole.md](topics/regole.md).

## Ultimo run

**2026-09-06 ~22:28 CEST (Tommy indexing /agents)** — after #94 PASS, Tommy personally requested Google URL Inspection / request indexing for `https://www.evex.sh/agents`. Team must NOT re-request or nag. Morning pulse scores whether `/agents` leaves discovered-not-indexed. Dettaglio in [LOG.md](LOG.md).

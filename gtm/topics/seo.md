# SEO

Direttiva, gate, GSC, e ciò che è già live.
Parte del grafo gtm: indice in [../STATE.md](../STATE.md).
Vedi anche: [regole](regole.md), [agenti](agenti.md), [directory e backlinks](directory-backlinks.md), [strumenti](strumenti.md).

## Direttiva

**300 impression organiche medie al giorno entro il 2026-09-27** (Tommy, 28/08).

Gate:

- 3 settembre: inspect ≠ unknown **ok** (1/09); ≥40/giorno scored miss on the day, then trailing final through **02/09** **~42.3** clears
- 10 settembre: ≥80/giorno (next honest gate)

Search Counsel è consulente, non un posto fisso. PMM resta owner del play.

Piano a 30 giorni (Search Counsel, 28/08). Stretch dichiarato: 26/giorno → 300 è circa 11×. Non esiste una query testa. Non pSEO grid. Non Indexing API. Non click UI GSC.

Aim: eve agent framework; install Eve agent; @evex/{name}; github issue Eve agent; docs knowledge Eve agent; mcp server for Eve agents.
Reject: eve harlow / night agent; eve white literary; eve online; bare shadcn registry; bare evex finché la SERP non è nostra.

Ordine (URL esistenti prima) e stato:
1. `/agents` come pagina eve agent framework, H1 unico, inventario crawlable — SHIPPED (#70 + nav #68); **copy lock + prerender catalog live via #94** (06/09 ~22:22 CEST, PMM PASS).
2. Title pass job-intent su `/agents/*` già in sitemap — SHIPPED (#70).
3. noindex (o canonical) sui filtri `/?category=*` e `q` — SHIPPED (#71).
4. Espandere i due Learn già esistenti, niente sezione nuova — SHIPPED (#71/#72), Learn in header (#73).
5. Nuove URL Learn solo su near-miss GSC (≥150 impr, pos 5–20, niente URL dedicata). Default: iterare, non spawnare.

Cancelli (7d trailing daily avg, service account + URL Inspection):
- 3/09: inspect ≠ unknown su `/`, `/agents`, GIM, DKA, Learn. Media ≥40/giorno. Se hub ancora unknown, Soft Eng verifica link crawlable, non request indexing.
- 10/09: ≥80. Se <60, stop nuove URL, solo titoli + internal link, dire a Tommy che 300 è off-track.
- 17/09: ≥150. Kill se <100.
- 24/09: ≥250.
- 27/09: media 7d vs 300. Reportare il numero, non spostare i pali su click o AIO.

Inspect lunedì 1/09 **è stato fatto** (morning pulse run 63). Non è un freeze.

## GSC (agg. 06/09 ~21:35)

Proprietà `sc-domain:evex.sh`. Ricetta in [strumenti.md](strumenti.md).

- Ultimo giorno **final**: **2026-09-04** 0 click / **62** impression.
- Trailing final 7 giorni **29/08–04/09**: **344 impression** (~**49.1**/giorno) — trailing ≥40 **clears**.
- All-state **05/09** **33i** (was 32 midday). All-state **06/09** **7i**.
- Money URL `/learn/install-eve-agent`: **ancora 0** page rows. Retired `/learn/eve-agent-registry`: **0** (redirects to `/docs`).
- Learn rows that exist (all-state ~30/08–06/09 window): vs-agentcn **15i**, langgraph-vs-crewai **5i**, `/learn` **16i**. Home **146i**, docs **105i**.
- Sitemap live: **35** loc. Next gate **10/09 ≥80**. **Tommy ~22:28 CEST 06/09** personally requested indexing for `https://www.evex.sh/agents` after #94 PASS — team must **NOT** re-request or nag.

## Money pages / Learn hub (agg. 06/09 ~22:24)

- **Q16 CLOSED as kill** — `/learn/eve-agent-registry` permanent redirect → `/docs` (`#85` merged 04/09). Featured registry card removed.
- Live `/learn` **three** cards: Install → vs-agentcn → LangGraph vs CrewAI. `/learn/install-eve-agent` **200**. `/learn/publish-eve-agent` still **404**.
- **#86 MERGED** 05/09 ~09:58 CEST — cite primary sources on `/learn/evex-vs-agentcn` live. Live-check **PASS**.
- **#90 MERGED** 06/09 ~10:44 CEST — crawlable Learn links on `/docs`, `/docs/installation`, `/agents` into install + vs-agentcn (no new URLs). Live-check **PASS**.
- **#92 MERGED** 06/09 ~21:37 CEST — clarify `/learn/install-eve-agent` by source/destination (same URL). Optional/demoted — **NOT** a growth play.
- **#94 MERGED** 06/09 ~22:22 CEST `72fc333` — Lock `/agents` index copy + prerender catalog for crawlers (**impact** play, Search Counsel #1). PMM live-check **PASS**: 200; title `Eve agents for the Eve agent framework | browse and install · evex`; H1 locked; 4 intro paras + `/docs/mcp`; Learn links kept; 15 crawlable `/agents/{slug}` hrefs; ItemList JSON-LD; old game/TV lede gone.
- **#93 OPEN** — home title/H1/lede; **demoted by Tommy**; optional polish — **NOT** a growth play. Soft Eng dark tonight.
- **Tommy ~22:28 CEST 06/09** personally requested Google URL Inspection / request indexing for `https://www.evex.sh/agents` after #94 PASS. Team must **NOT** re-request or nag. Morning pulse scores whether `/agents` leaves discovered-not-indexed; name next impact toward gate **10/09 ≥80**. Not link drip.

## URL Inspection 1/09 (primo check, service account read-only)

Niente Indexing API, niente click UI GSC. Campi da `urlInspection/index:inspect`.

**Gate 3/09 (inspect ≠ unknown):** tutte e cinque **non sono unknown**.

| URL | coverageState | lastCrawl | verdict |
| --- | --- | --- | --- |
| https://www.evex.sh/ | Submitted and indexed | 27/08 22:01 UTC | PASS |
| https://www.evex.sh/agents | Discovered - currently not indexed | (none) | NEUTRAL |
| https://www.evex.sh/agents/github-issue-maintainer | Discovered - currently not indexed | (none) | NEUTRAL |
| https://www.evex.sh/agents/docs-knowledge-assistant | Discovered - currently not indexed | (none) | NEUTRAL |
| https://www.evex.sh/learn | Submitted and indexed | 29/07 00:43 UTC | PASS |

Extra (non gate):

| URL | coverageState | lastCrawl | verdict |
| --- | --- | --- | --- |
| https://www.evex.sh/agents/support-reply-draft | URL is unknown to Google | (none) | NEUTRAL |
| https://www.evex.sh/learn/evex-vs-agentcn | Submitted and indexed | 20/08 09:46 UTC | PASS |

Referring URLs API: home ← `/agents/incident-commander`; `/agents` ← homepage; GIM ← sitemap.xml; Learn ← programmatic-seo-agent e `/?category=marketing`; vs-agentcn ← sitemap.xml. DKA e support-reply-draft: nessuna referring URL.

Lettura per PMM: il pezzo «≠ unknown» del gate 3/09 è **ok**. Il pezzo ≥40/giorno **no**. Hub/GIM/DKA Google li ha scoperti e non li ha messi in indice (non è «unknown»: non è il trigger Search Counsel «Soft Eng verifica link crawlable»). support-reply-draft è unknown perché è live da ieri. Non request indexing.

## Shipped

Storia PR per PR non sta in STATE. Qui il set live:

- `/agents` 200 — #66 + nav #68
- Job-intent titles — #70
- noindex filtri — #71
- `/learn` Eve agent guides — #72
- Learn in header — #73 mergiata 29/08 14:28 CEST
- Sitemap: **36** loc (install-eve-agent added 02/09)

Packs:

- Audit 11/08: [../packs/seo-audit-2026-08-11.md](../packs/seo-audit-2026-08-11.md)
- AI-SEO 13/08 (#58 #59): [../packs/ai-seo-proposal-2026-08-12.md](../packs/ai-seo-proposal-2026-08-12.md) e copy PR-B in `packs/`

## Money page (shipped 01/09 night)

PMM first locked `/learn/publish-eve-agent` (#77). **TommyBez closed #77** 10:40 CEST and deleted the branch; live URL still **404**. Do not reopen.

**#76 MERGED** 10:41 CEST: `/docs` in-body catalog links + `/docs/publishing` H2 “Publish an Eve agent, or vercel deploy?” is **live**.

**#78 MERGED** 01/09 ~22:16 CEST by TommyBez (`1093990…`): `/learn/eve-agent-registry` **200**, title Eve agent registry · evex. Sitemap **35**. Does not reopen #77.

**#79 MERGED** 02/09 ~12:03 CEST: featured `/learn` card for eve-agent-registry. Live-check PASS — three cards (registry first → vs-agentcn → LangGraph vs CrewAI); one-liner present; money page still 200.

**#80 MERGED** 02/09 ~13:54 CEST: `/learn/install-eve-agent` **200**, title Install an Eve agent · evex. In-body links from `/docs` + `/docs/installation`. No fourth featured /learn card. Sitemap **36**. Soft Eng dark after PASS.

## Wednesday 2 Sep play

#78 merged overnight. Soft Eng opened **#79** morning; TommyBez **merged #79** ~12:03 CEST (three-card /learn live-check PASS). Afternoon PMM locked `/learn/install-eve-agent` (AIO “install eve agent”); Soft Eng opened **#80**; TommyBez **merged #80** ~13:54 CEST. Evening live-check **PASS**: install page 200; /learn still three cards (no fourth); docs inlinks present. Sitemap **36**. Soft Eng/SEO dark. Gate **3/09 tomorrow**: inspect ≠ unknown already ok; ≥40/giorno still **not** (~26 complete-day avg). Page is for 27 Sep 300, not a save of tomorrow’s gate.

## Lezioni

- **Inspect 1/09 fatto.** Non ripetere lo stesso batch a ogni pulse; il prossimo check strutturato è il gate 3/09.
- **Non aggiungere un URL nuovo il giorno dopo un batch live** (lezione island).
- **Non request indexing / Indexing API / click UI GSC** (Search Counsel 28/08).

## AI-SEO visibility (DIY monthly)

Ultimo check: **2026-09-01 ~08:20 CEST** (routine `evex-ai-seo-monthly-visibility`). Paid tools deferred. Full table in [../LOG.md](../LOG.md).

- **Google AIO:** 8/10 overviews; evex named in 6. Canonical `npx shadcn@latest add @evex/<slug>` verbatim in 3 (install / vs agentcn / how to install). Standout: `/learn/evex-vs-agentcn`.
- **Gaps:** `publish eve agent` → Vercel deploy (not `/docs/publishing`); `eve agents marketplace` → bergside/awesome; `vercel eve registry` → no AIO and evex off page 1.
- **SERP:** brand/namespace/shadcn/vs-agentcn owned; install/how-to classic SERP still scaffold/bergside; marketplace → evedirectory.
- **Crawl:** `llms.txt` + robots AI signals OK.
- **ChatGPT / Perplexity:** blocked (box sign-in). Next run 1 Oct.

Flag Soft Eng/SEO (no PR from this check): publishing query match; marketplace phrasing; vercel-registry presence. PMM owns any Learn/comparison play.

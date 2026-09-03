# evex — stato GTM (fotografia)

Fonte di verità per l'agente GTM schedulato. Tommy lo modifica direttamente: **le sue modifiche vincono sempre** su quello che ha scritto un agente.

Ultimo aggiornamento: 2026-09-03 ~08:40 CEST (morning pulse, run 67 — gate day)

> ⚠️ `gtm/` non è versionato in git: questa cartella è l'unica memoria dell'agente tra i run, con backup settimanale su [evex-gtm-backup](https://github.com/TommyBez/evex-gtm-backup) (domenica 22:30). Trattare i file con cura: mai troncare, in dubbio aggiungere. Dettagli backup in [topics/strumenti.md](topics/strumenti.md).

## Come è organizzata la memoria

**Questo file è SOLO la fotografia dello stato attuale**: si aggiorna sostituendo i valori, mai appendendo croniche. La cronaca dei run va in [LOG.md](LOG.md) (voce in cima a ogni run; rollover settimanale in `log/`, convenzione scritta lì). La storia e il contesto per tema vivono nei **topic** qui sotto: quando un run produce storia nuova (una PR, una decisione, un'osservazione), aggiorna il topic pertinente e qui cambia solo il valore corrente. Artefatti nuovi: piani e pack operativi in `packs/`, bozze da pubblicare in `drafts/`, screenshot e render in `assets/` — sempre linkati dal topic che li usa, mai file sciolti nella root di `gtm/` (nella root vivono solo STATE.md e LOG.md). Script temporanei sempre in /tmp, mai qui. Archivio pre-ristrutturazione: `archive/pre-restructure-2026-08-30/`.

### Mappa del grafo

| Topic | Contenuto |
| --- | --- |
| [topics/prodotto-metriche.md](topics/prodotto-metriche.md) | Prodotto, north star, baseline, numeri PostHog |
| [topics/seo.md](topics/seo.md) | Goal 300/giorno, gate 3/09 scored, GSC, pagine shipped |
| [topics/canali-social.md](topics/canali-social.md) | X EN / LinkedIn IT, Typefully, support-reply-draft live |
| [topics/directory-backlinks.md](topics/directory-backlinks.md) | Shortlist, #588 aperta (non nagare), chiusi |
| [topics/agenti.md](topics/agenti.md) | Catalogo, direttiva non-GitHub, support-reply-draft live |
| [topics/strumenti.md](topics/strumenti.md) | Ricette: PostHog, GSC, Typefully, GitHub, backup |
| [topics/regole.md](topics/regole.md) | TUTTE le regole permanenti di Tommy — leggerlo prima di scrivere qualsiasi copy |
| [topics/decisioni.md](topics/decisioni.md) | Indice cronologico delle domande chiuse (Q1–Q15) |

Log: [LOG.md](LOG.md) (settimana corrente, W36) → `log/2026-W35.md`, `log/2026-W34.md`, `log/2026-W33.md`. Archivio pre-ristrutturazione: `archive/pre-restructure-2026-08-30/`.

## Prodotto in una riga

Registry open source di agenti Eve. Sito https://evex.sh · repo https://github.com/TommyBez/evex · install `npx shadcn@latest add @evex/<slug>`. North star: unici non-autori che copiano il comando (`agent_install_command_copied`). PostHog **244993**.

## Numeri correnti (agg. 03/09 ~08:40 CEST)

| Metrica | Valore | Nota |
| --- | --- | --- |
| **North star** | **10 persone / 13 copie** | Soft Eng 19/08 sticky test escluso. Ultima 13:02 CEST 30/08 sticky `/agents/openui-assistant`. Score-only: non twittare OpenUI. |
| PostHog 03/09 Rome so far | 11 / 7 / 7 | Top pages: `/` 6u/7pv, publishing 1, CR 1, brand-visual 1, leaderboard 1. Top refs: $direct 3/6, t.co 2/3, github.com 1, api.daily.dev 1. |
| 02/09 Rome full | 23 / 13 / 14 | |
| 01/09 Rome full | 44 / 17 / 18 | |
| 31/08 Rome | 107 / 40 / 40 | |
| Lancio 11/08–03/09 08:40 | 1135 / 535 / 614 | |
| **GSC gate 3/09** | **≥40/giorno: NON met su final** · **~40 su all-state** | Final last day **31/08** 0c/50i. Final 7d 25–31 **205i (~29.3/giorno)**. All-state 27/08–02/09 **279i (~39.9/giorno)**. Inspect ≠ unknown: **già ok** (1/09). |
| Stelle GitHub | 24 | |
| PR aperte GTM | **0** | #79 featured card MERGED 02/09 12:03 CEST. #80 `/learn/install-eve-agent` MERGED 02/09 13:54 CEST. #75 eve 0.47.5 MERGED (out of GTM scope but landed). |
| Typefully | get_me **200** (set 266935) | support-reply-draft X **41** impressions, 0 likes / 0 replies / 0 retweets, 1 profile click, 0 link clicks. |
| Sitemap | **36** | Includes `/learn/eve-agent-registry` + `/learn/install-eve-agent`. `/learn/publish-eve-agent` still 404. |
| **AI-SEO monthly (1/09)** | Google: **6/10** name evex · **3** AIO with canonical install | Invariato. ChatGPT/Perplexity blocked (sign-in). |

## Direttiva attiva

**300 impression organiche medie al giorno entro il 27/09.** Sit morta. Next first-party non-GitHub **è live**: `/agents/support-reply-draft` **200**. Inspect 1/09 **fatto**. **Gate 3/09 scored this morning:** inspect half **pass**; ≥40/giorno on complete final days **fail** (~29); provisional all-state including 1–2 Sep is **~40** (borderline). Lennybot fuori. Niente paid, niente sales. Storia e gate in [topics/seo.md](topics/seo.md) e [topics/agenti.md](topics/agenti.md).

## In volo adesso

- **#79 MERGED** 02/09 ~12:03 CEST — featured Eve agent registry card on `/learn` LIVE (title + one-liner as locked).
- **#80 MERGED** 02/09 ~13:54 CEST — `/learn/install-eve-agent` LIVE (title Install an Eve agent · evex). **Not** yet a featured card on `/learn` index (candidate for PMM).
- Open GTM PRs: **0**. Soft Eng/SEO **dark** this morning until PMM names the next shippable move toward 300.
- Non nagare #588. Non twittare OpenUI. Non request indexing.

## AI-SEO visibility (fotografia)

Ultimo DIY: **2026-09-01**. Google AIO: evex named on brand/install/vs-agentcn; gaps on **publish eve agent** and **eve agents marketplace**. Canonical install winning in 3 AIOs. ChatGPT + Perplexity: unreachable until box sign-in. Paid tools still deferred. Next check: **1 Oct 08:15**.

## Domande aperte

Le vive stanno SOLO qui. Le chiuse: [topics/decisioni.md](topics/decisioni.md).

- **Q11** — [awesome-shadcn-ui #588](https://github.com/birobirobiro/awesome-shadcn-ui/pull/588) still OPEN, no human comments. **Non nagare.**

## Aspettano Tommy

Niente da mergiare (zero PR aperte). Opzionale: login ChatGPT + Perplexity sul Chrome del box per l'AI-SEO di ottobre. Il pezzo vero oggi è la decisione PMM sul prossimo move dopo il gate (candidate: featured card `/learn` per install-eve-agent, o altro money page / internal-link play).

## Guardrail lampo

Estratto: comando install `npx shadcn@latest add @evex/<slug>`; su X scrivere `[@]evex/<slug>`; voce in frasi intere; sit morta; PMM possiede slug e pagine; commenti PR autonomi. Il resto in [topics/regole.md](topics/regole.md).

## Ultimo run

**2026-09-03 ~08:40 CEST (morning, run 67, gate day)** — #79+#80 live; sitemap 36; north star 10/13; GSC final gate ≥40 **not met** (~29/day), all-state ~40; Soft Eng/SEO dark pending PMM. Dettaglio in [LOG.md](LOG.md).

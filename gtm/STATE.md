# evex — stato GTM (fotografia)

Fonte di verità per l'agente GTM schedulato. Tommy lo modifica direttamente: **le sue modifiche vincono sempre** su quello che ha scritto un agente.

Ultimo aggiornamento: 2026-08-30 ~21:25 CEST (run 59 evening)

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
| [topics/agenti.md](topics/agenti.md) | Catalogo, direttiva non-GitHub, PR #74 support-reply-draft |
| [topics/strumenti.md](topics/strumenti.md) | Ricette: PostHog, GSC, Typefully, GitHub, backup |
| [topics/regole.md](topics/regole.md) | TUTTE le regole permanenti di Tommy — leggerlo prima di scrivere qualsiasi copy |
| [topics/decisioni.md](topics/decisioni.md) | Indice cronologico delle domande chiuse (Q1–Q15) |

Log: [LOG.md](LOG.md) (settimana corrente, W35) → `log/2026-W34.md`, `log/2026-W33.md`. Archivio pre-ristrutturazione: `archive/pre-restructure-2026-08-30/`.

## Prodotto in una riga

Registry open source di agenti Eve. Sito https://evex.sh · repo https://github.com/TommyBez/evex · install `npx shadcn@latest add @evex/<slug>`. North star: unici non-autori che copiano il comando (`agent_install_command_copied`). PostHog **244993**.

## Numeri correnti (agg. 30/08 ~21:25 CEST)

| Metrica | Valore | Nota |
| --- | --- | --- |
| **North star** | **10 persone / 13 copie** | Ultima 13:02 CEST sticky `/agents/openui-assistant` (3 copie, una persona; visit allshadcn). Score-only: non twittare. |
| PostHog 30/08 so far | 5 / 3 / 3 | pv / uniques / sessioni (bounce ~67%, avg ~18s) |
| 29/08 | 35 / 14 / 15 | |
| Lancio 11–30/08 | 947 / 470 / 533 | |
| GSC | 28/08 1c / 27i · 7d 22–28 ~26/giorno | Goal 300/giorno. 29–30 non in API. |
| Stelle GitHub | 24 | |
| PR aperte | 1 (#74) | https://github.com/TommyBez/evex/pull/74 — threads 0 unresolved, CI verde, review required |
| Typefully | connesso (set 266935) | Ultimo X Evex = CI explainer; no new Evex draft |

## Direttiva attiva

**300 impression organiche medie al giorno entro il 27/09.** Sit morta. Il next first-party non-GitHub **è questa PR** (#74). Inspect lunedì 1/09 è un check, non un freeze. Lennybot fuori. Niente paid, niente sales. Storia e gate in [topics/seo.md](topics/seo.md) e [topics/agenti.md](topics/agenti.md).

## In volo adesso

- **#74** https://github.com/TommyBez/evex/pull/74 — HEAD `d9fc4a6`, CI/Vercel/verify verdi, 0 thread aperti, mergeStateStatus BLOCKED = review required. Live `/agents/support-reply-draft` ancora **404**. Soft Eng sui commenti fino al merge, poi dark. Niente recut.
- SEO dark fino a lunedì 1/09 (inspect). Non aggiungere un URL il giorno dopo un batch live.
- Typefully dopo 200: bozza only da [drafts/support-reply-draft-x-2026-08-30.md](drafts/support-reply-draft-x-2026-08-30.md). GET deve confermare `[@]evex/support-reply-draft`.
- Non twittare OpenUI. Non nagare #588. Domenica 22:30 è il dump backup, non un quarto pulse.

## Domande aperte

Le vive stanno SOLO qui. Le chiuse: [topics/decisioni.md](topics/decisioni.md).

- **Q11** — [awesome-shadcn-ui #588](https://github.com/birobirobiro/awesome-shadcn-ui/pull/588) still OPEN, no human comments. **Non nagare.**

## Aspettano Tommy

1. **Merge #74** https://github.com/TommyBez/evex/pull/74 — nient'altro oggi.

## Guardrail lampo

Estratto: comando install `npx shadcn@latest add @evex/<slug>`; su X scrivere `[@]evex/<slug>`; voce in frasi intere; sit morta; PMM possiede slug e pagine; commenti PR autonomi. Il resto in [topics/regole.md](topics/regole.md).

## Ultimo run

**2026-08-30 ~21:25 CEST (run 59, evening)** — play midday lock confirmed (merge #74). Dettaglio in [LOG.md](LOG.md).

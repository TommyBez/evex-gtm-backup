# Prodotto, north star e cronaca delle metriche

Che cos'è evex, come si misura il successo, e i numeri di traffico/install.
Parte del grafo gtm: indice in [../STATE.md](../STATE.md).
Vedi anche: [agenti](agenti.md), [SEO](seo.md), [strumenti](strumenti.md), [regole](regole.md).

## Prodotto

evex è il registry open source di agenti per il framework Eve. Gli sviluppatori scoprono agenti costruiti dalla community, li installano in un'app Eve, e pubblicano i propri via pull request.

- Sito: https://evex.sh (canonica www)
- Repo: https://github.com/TommyBez/evex
- Install: `npx shadcn@latest add @evex/<slug>` — mai `eve add` in copy, OG, Typefully o meta (vedi [regole.md](regole.md))

## North star

**Utenti unici non-autori che copiano un comando di installazione**: evento `agent_install_command_copied`.

- PR #47: tri-state `viewer_is_author` (`true` / `false` / `null`).
- Override Tommy 20/08: se il flag manca e la persona non è loggata, conta come non-autore.
- Escludere i test team noti (Soft Eng sticky 2026-08-19 19:27 UTC).
- Superfici: `sticky_install_cta` OR `mobile_install_bar` OR `install_command`. Guardare solo sticky perde il telefono.
- PostHog progetto **244993**, insight **j7rG8gFO**, dashboard **887723**. Ricetta in [strumenti.md](strumenti.md).
- Il contatore DB install è bot-esposto: non è social proof.

## Baseline (10/08)

- Stelle GitHub: **21**
- Agenti a catalogo: **11**, tutti TommyBez (supply mono-autore)

## Numeri recenti (agg. 03/09 ~08:40 CEST)

| Giorno | pv / uniques / sessioni |
| --- | --- |
| 03/09 Rome so far | 11 / 7 / 7 (top `/` 6/7; refs $direct, t.co) |
| 02/09 Rome full | 23 / 13 / 14 |
| 01/09 Rome full | 44 / 17 / 18 |
| 31/08 Rome | 107 / 40 / 40 |
| Lancio 11/08–03/09 08:40 | 1135 / 535 / 614 |

**North star attuale: 10 persone / 13 copie.** Ultima invariata: 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: **non twittare** queste copie OpenUI.

Fotografia corrente in [../STATE.md](../STATE.md). Cronaca dei run in [../LOG.md](../LOG.md).

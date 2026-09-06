## Fotografia corrente (06/09 evening)

North star **11/15** (Soft Eng 19/08 test escluso). Ultima copia 03/09 sticky `/agents/code-reviewer`. PostHog 06/09 so far **20/13/13**. 05/09 full **11/7/7**. Launch **1245/578/667**.

# Prodotto, north star e cronaca delle metriche

Che cos'è evex, come si misura il successo, e i numeri di traffico/install.
Parte del grafo gtm: indice in [../STATE.md](../STATE.md).
Vedi anche: [agenti](agenti.md), [SEO](seo.md), [strumenti](strumenti.md), [regole](regole.md).


## Snapshot 03/09 ~22:20 CEST (evening run 69)

North star **12/16**. PostHog Rome today so far **57/19/21**; 02/09 full **23/13/14**; launch **1187/547/630**. Last copy 03/09 14:55 CEST sticky `/agents/code-reviewer` (unsigned, 2 copies / 1 person). Score-only. Detail in [../LOG.md](../LOG.md).

## Snapshot 02/09 ~08:35 CEST (morning run 66)

North star **10/13** (unchanged). PostHog Rome today so far **5/4/4**; 01/09 **44/17/18**; launch **1112/522/599**. Top ref $direct. #78 money page live. Detail in [../LOG.md](../LOG.md).

## Snapshot 01/09 ~21:25 CEST (evening run 65)

North star **10/13** (unchanged). PostHog Rome today **44/17/18**; 31/08 **107/40/40**; launch **1107/519/595**. Top refs $direct then api.daily.dev. Detail in [../LOG.md](../LOG.md).

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

## Numeri recenti (agg. 03/09 ~22:20 CEST)

| Giorno | pv / uniques / sessioni |
| --- | --- |
| 03/09 Rome so far | 57 / 19 / 21 |
| 02/09 Rome full | 23 / 13 / 14 |
| 01/09 Rome full | 44 / 17 / 18 |
| 31/08 Rome full | 107 / 40 / 40 |
| Lancio 11/08–03/09 ~22:20 | 1187 / 547 / 630 |

**North star attuale: 12 persone / 16 copie.** Ultima: 03/09 14:55 CEST, sticky su `/agents/code-reviewer` (2 copie, una persona, unsigned). Score-only: **non twittare**. Soft Eng 19/08 test escluso.

Fotografia corrente in [../STATE.md](../STATE.md). Cronaca dei run in [../LOG.md](../LOG.md).

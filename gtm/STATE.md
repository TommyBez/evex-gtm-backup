# evex — GTM STATE

> Fonte di verità per l'agente GTM. Tommy la modifica direttamente: le sue modifiche vincono sempre su quello che ha scritto un agente.
> Creato il 2026-08-10 durante il setup del meccanismo GTM (replicato da skillsboard).

## Brief di prodotto

- **evex** è il registry open source di agenti per il framework [Eve](https://eve.dev): gli sviluppatori scoprono agenti costruiti dalla community, li installano in un'app Eve con `npx shadcn@latest add @evex/<slug>` (forma canonica mostrata dal sito e da usare SEMPRE nella copy; la forma URL `https://evex.sh/r/<slug>` funziona ma non si scrive nei post), e pubblicano i propri via pull request — ogni agente è code-owned e reviewed.
- Sito: https://evex.sh · Repo pubblico: https://github.com/TommyBez/evex · Leaderboard: https://evex.sh/leaderboard
- Gratis, open source. Autori con identità GitHub verificata; favorites e install metrics nel DB; sign-in con codice email o GitHub OAuth.
- Monorepo pnpm/Turborepo: `apps/web` (Next.js 16 App Router), `packages/agent-registry` (generatore; gli agenti stanno in `/registry` alla root del repo, NON in `packages/agent-registry/agents`). Runtime data in Postgres (Neon) via Drizzle; deploy Vercel.

## North star (CONFERMATA da Tommy via Slack, 10/08/2026)

**Utenti unici non-autori che copiano un comando di installazione**: eventi `agent_install_command_copied` con `viewer_is_author: false`. Tri-state (da review PR #47): `true` = autore verificato, `false` = non-autore verificato (loggato, githubUsername diverso), `null` = identità non verificabile (signed-out o senza GitHub) — conteggiata come volume separato, mai nella north star. Live in prod dal merge di #47 (10/08 14:39 UTC).

- **Insight north star**: https://eu.posthog.com/project/244993/insights/j7rG8gFO (settimanale, serie non-autori + serie tutti), su dashboard «evex GTM» https://eu.posthog.com/project/244993/dashboard/887723 (pinned). Annotation 105837 sul merge di #47.
- Il contatore DB `agent_install_metric` resta segnale secondario grezzo: aggregato per slug, non user-scoped, non retroattivo, e **bot-esposto** (`/r/*` fuori dalla protect list botid; sweep same-second 10/08 08:19 UTC — il totale 1.686 è un tetto, non una verità).

## Baseline (fotografata al run 1, 2026-08-10 ~16:00 CEST)

- Stelle GitHub: **21** · Fork: 0 · Issue aperte: 0 · Repo creato 2026-06-20, main fermo dal 5/07 al 10/08.
- Agenti nel catalogo: **11** (tutti di TommyBez — supply mono-autore, lato offerta è il gap strutturale). +1 slug delisted nel DB (`github-release-scout`, 1 install).
- Installazioni (contatore DB, bot-esposto): **1.685** sugli 11 agenti a catalogo (top: brand-visual-asset-generator 199, code-reviewer 185, branded-seo-page-builder 169). Totale righe DB: 1.686.
- Utenti: **3** · Profili: **1** · Favorites: **4**. Numeri troppo piccoli per qualsiasi tendenza.
- Sito live ok (308 → www.evex.sh, 200; leaderboard ok e coerente col DB).
- PostHog: integrazione client viva in prod, **verificata il 10/08 ~17:00 CEST**: eventi da www.evex.sh dal 10/08 13:57 UTC ($pageview, $autocapture, $web_vitals), **2 visitatori unici** il 10/08, **zero eventi da localhost** (nessun inquinamento dev osservato). Nessun evento custom ancora emesso (con 2 visitatori è atteso): `agent_install_command_copied`, `catalog_search` ecc. arriveranno col traffico. Nomi eventi verificati nel codice: agent_install_command_copied, favorite_updated, catalog_search, github_auth_started, auth_otp_requested, authentication_completed, profile_saved.

## Infrastruttura e accessi

- Repo montato: `/Users/tommaso/personal-projects/evex` (in bash: `/sessions/<sessione>/mnt/evex`).
- DB prod: Neon, progetto **`broad-water-53167398`** («neon-evex», org «Vercel: Tommaso's projects», org_id `org-lucky-surf-38999764`) — **SOLA LETTURA**. Tabelle: `user` (ha `githubUsername` unique — è il join con `authorUsername` degli agenti), `session`, `account`, `verification`, `agent_install_metric`, `agent_favorite`, `profile`. ⚠️ `list_projects` di default guarda l'org personale, dove c'è solo `evex-dev` (`icy-silence-77101533`): dev DB, NON è un segnale.
- PostHog: **setup fatto da Tommy il 10/08**. Org **«Evex»** `019feb06-3618-0000-089c-4d14bd6c0508`, progetto **244993** («Default project», EU cloud, timezone UTC). **Accesso MCP OPERATIVO dal 10/08 ~16:20** (Tommy ha riautorizzato il connettore, Q5 risolta): il progetto attivo del connettore è il 244993. Asset creati: dashboard «evex GTM» **887723** (pinned), insight north star **j7rG8gFO** (5414420), insight traffico **HBV38XNS** (5414423), annotation **105837** (merge #47). Skills Board 225645 e UILO restano MAI da toccare.
- GitHub PAT: **presente** in `.credentials/github-token` (verificato 10/08) — scritture GitHub operative (PR #47 aperta con successo via REST). Repo backup TommyBez/evex-gtm-backup: esistenza non verificabile dalla sandbox (niente rete curl; da confermare, Q2 residuo).
- Vercel MCP: disponibile. Progetto `evex` (team tommasos-projects-bb9d6551); preview deploy delle PR funzionanti.
- Typefully: config in `.typefully/` (defaultSocialSetId 266935). Social set identificato il 10/08: **266935 «Tommy Bez» (@TommyBez85)**, l'unico accessibile — evex condivide il set personale di Tommy, non ha un set dedicato.
- Ricetta git in sandbox VERIFICATA su evex (run 1): clone `--filter=blob:none` in /tmp con credential helper inline → ok; `corepack enable && pnpm install --frozen-lockfile` (node 24.11.1, pnpm 10.33.0) → ok; `pnpm check`, `pnpm typecheck`, `pnpm test`, `pnpm build` (con DATABASE_URL fittizia) → tutti ok. La sandbox bash NON risolve api.github.com via curl: le chiamate REST GitHub riescono dai subagent (Bash tool), non da mcp__workspace__bash.

## Stato dei canali

- Slack #evex-gtm: **esiste** (creato da Tommy il 10/08 11:32). channel_id: **C0BNZ91CX6X**. Primo resoconto e domande postati al run 1.
- X / LinkedIn: **build in public APPROVATA da Tommy (risposta Slack 10/08: «si, estendila»)**. Le 2 bozze Typefully sono state **riviste e SCHEDULATE da Tommy il 10/08 ~17:10 CEST** (schedularle è azione sua, coerente col guardrail): **10274965** (lancio, X inglese + LinkedIn italiano) → **martedì 11/08 9:30 CEST**; **10274969** (supply side, X) → **giovedì 13/08 9:30 CEST**. ⚠️ Nel post X di lancio il comando è scritto `[@]evex/code-reviewer`: se pubblicato letterale non è copiabile → **Q8** (verificato il 10/08 sera: l'account X @evex esiste ma è SOSPESO, quindi la mention nuda linkerebbe a una pagina «account suspended»). Il post supply linka il repo (regola link ok); la guida https://evex.sh/docs/publishing sarebbe l'entry point migliore, suggerito in Q8/resoconto ma la bozza ormai è di Tommy: non toccarla senza suo ok.
- **Regola di copy permanente (Tommy, 10/08/2026, in sessione): i post LinkedIn si scrivono in ITALIANO.** X resta in inglese. Vale per tutte le bozze future.
- **Regola di copy permanente (Tommy, 10/08/2026, in sessione): evitare le frasi fatte da AI** («La parte che mi sta più a cuore» e formule simili di enfasi confezionata). Meglio l'affermazione diretta senza preambolo.
- **Regola di copy permanente (Tommy, 10/08/2026, in sessione): il comando di install si scrive SEMPRE nella forma canonica `npx shadcn@latest add @evex/<slug>`**, mai nella forma URL. Il link a evex.sh o al repo va comunque incluso nel corpo del post (regola link separata).
- **Regola permanente (Tommy, 10/08/2026, in sessione): ogni bozza Typefully deve SEMPRE avere un commento con la data di pubblicazione suggerita** (giorno, ora, e una riga di motivazione). Fatto per le bozze 10274965 (sugg. mar 11/08 9:30 CEST) e 10274969 (sugg. gio 13/08 9:30 CEST, 2 giorni dopo il lancio).
- SEO / community / directory: non ancora aperti.

## Backlog esperimenti

1. ~~Instrumentazione PostHog~~ — FATTA: #46 + #47 mergiate, integrazione verificata in prod (10/08), insight north star e dashboard creati. Resta in coda: (a) **verificare nei prossimi run che gli eventi custom con `viewer_is_author` arrivino davvero** (al 10/08 sera ~17:15 ancora zero eventi custom e 2 visitatori: atteso; il vero test è dopo il lancio dell'11/08); (b) decisione su evento server-side nell'endpoint `/r/*` (legata al problema bot, punto 2).
2. **Bot sul contatore installazioni** — quantificato il 10/08 sera: contatori DB fermi dallo sweep delle 08:19 UTC (totale 1.685 + 1 delisted), 2 visitatori reali oggi, 0 eventi custom → il contatore è quasi tutto crawler, e i numeri sono mostrati pubblicamente (card, leaderboard, pagine agente) col lancio schedulato per l'11/08 9:30. Codice verificato: `apps/web/app/r/[...name]/route.ts` incrementa su ogni GET, `_request` inutilizzato, nessun filtro UA né botid. **Q7 postata su Slack il 10/08 sera**: (a) filtro user-agent nel conteggio (PR pronta in un run), (b) tenere il conteggio e cambiare etichetta sul sito, (c) accettare il rumore (north star ormai su PostHog). Eventuale reset dei valori = scrittura DB prod: solo Tommy.
3. ~~North star misurabile~~ — CONFERMATA da Tommy il 10/08 (vedi sezione North star). Insight j7rG8gFO operativo.
4. **Supply side** — 11 agenti, 1 solo autore. Primo passo fatto il 10/08: bozza social «publish your agent» (Typefully 10274969, schedulata da Tommy per il 13/08). CORREZIONE 10/08 sera: la guida «publish your agent» ESISTE GIÀ su https://evex.sh/docs/publishing (verificata nel codice `apps/web/lib/docs-content.ts`: scaffold `registry:new`, layout pacchetto, meta.docs, validazione, CODEOWNERS — completa, datata 04/07). La voce precedente la dava da costruire: falsa, non ereditarla. Prossimi candidati reali: outreach mirato a dev Eve, e far puntare la copy supply-side alla guida. Da pesare contro la domanda quando ci saranno dati north star.
5. **Distribuzione lancio — ATTIVO**: lancio 11/08 9:30 CEST, supply 13/08 9:30 CEST (schedulati da Tommy). Dal run delle 08:20 dell'11/08: monitorare traffico, prime copie install (`agent_install_command_copied` per `viewer_is_author`) e stelle GitHub; poi decidere il canale successivo (directory, community, SEO).

## PR aperte

- Nessuna PR aperta dall'agente.
- **#47 MERGIATA da Tommy il 10/08 alle 14:39 UTC** (check verdi, review bot risolte). Attribuzione tri-state `viewer_is_author`, filtro dev/localhost e `catalog_search` sono live in prod.
- Contesto: **#48** aperta da Tommy stesso il 10/08 14:44 UTC (`codex/aggiorna-eve-framework`, aggiornamento agenti e tooling all'ultimo Eve) — non è dell'agente, non gestirla; solo tenerla d'occhio come segnale che main si muove.

## Domande aperte

- ~~Q1: canale Slack #evex-gtm~~ → RISOLTA 10/08 (canale creato, id C0BNZ91CX6X).
- ~~Q2: repo di backup~~ → RISOLTA (risposta Tommy via Slack 10/08 16:20: «creato»). TommyBez/evex-gtm-backup esiste; il task di backup della domenica potrà usarlo. Esistenza non verificabile dalla sandbox, fede alla parola di Tommy.
- ~~Q3: build in public per evex~~ → RISOLTA, SÌ (risposta Tommy via Slack 10/08 16:20: «si, estendila»). Linea attiva, vedi Stato dei canali.
- ~~Q4: commit .gitignore~~ → RISOLTA 10/08 (inclusa nella PR #46 mergiata).
- ~~Q5: accesso PostHog~~ → RISOLTA (risposta Tommy via Slack 10/08 16:19: «fatto»). Connettore operativo sul progetto 244993, verificato nello stesso pomeriggio.
- ~~Q6: definizione north star~~ → RISOLTA, SÌ (risposta Tommy via Slack 10/08 16:19, valida per la versione tri-state). Vedi sezione North star.
- **Q7 — Contatore install bot-esposto e pubblico** (postata su Slack 10/08 sera): filtro UA nell'endpoint (a), riformulare etichetta sul sito (b), o accettare il rumore (c). Dettagli in backlog #2. ✅ = opzione a, PR al run successivo.
- **Q8 — Comando `[@]evex/...` nel post X di lancio** (postata su Slack 10/08 sera, URGENTE entro le 9:30 dell'11/08): l'account X @evex è sospeso (verificato); scegliere tra mention nuda (linka «account suspended»), forma URL solo su X, o tenere `[@]` letterale. ✅ = forma URL, la sistemo al run delle 08:20.

## Run log

Ultimo run: **2026-08-10 ~17:10–17:30 CEST (run 3, slot serale anticipato)** — bozze social schedulate da Tommy (lancio 11/08, supply 13/08), delta nullo dal run 2, quantificato il problema bot sul contatore (Q7) e trovato il problema `[@]` nel post X di lancio (Q8, urgente). Corretta la voce di backlog sulla guida publishing (esiste già). Log completo in `gtm/LOG.md`.

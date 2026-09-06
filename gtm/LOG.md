# evex — run log

Append-only, voce più recente in cima: **ogni run aggiunge la sua voce qui sotto**, dopo la riga dell'indice. Separato da STATE; **partizionato per settimana ISO il 30/08/2026** (ristrutturazione su modello skillsboard). Come STATE non è versionato in git (backup settimanale sul repo privato evex-gtm-backup, domenica 22:30). Mai riscrivere o troncare le voci esistenti.

**Convenzione di rollover (per i run):** questo file contiene solo le voci della settimana ISO corrente. Al primo run del lunedì, sposta le voci della settimana appena chiusa in `log/<anno>-W<settimana>.md` (header come i file esistenti) e aggiorna l'indice qui sotto. La fotografia dello stato vive in [STATE.md](STATE.md); qui solo cronaca dei run.

## Indice partizioni

- **Settimana corrente (2026-W36, 31 agosto–6 settembre): le voci qui sotto.**
- [log/2026-W35.md](log/2026-W35.md) — 24-30 agosto: catalog merge live, Learn in nav, support-reply-draft #74, gtm/ restructure skillsboard, north star 10/13
- [log/2026-W34.md](log/2026-W34.md) — 17-23 agosto: Copy command #61, OSSDrop, Lennybot poi sit, #62–#65 GIM, override unsigned north star, sit weekend
- [log/2026-W33.md](log/2026-W33.md) — 10-16 agosto: setup GTM, lancio 11/08, audit SEO, directory, AI-SEO #58/#59, Q13 #60 chiusa senza merge

## Voci della settimana corrente (2026-W36)

## 2026-09-06 ~22:28 CEST (Tommy personally requested indexing /agents)

After #94 live-check **PASS**, Tommy (~22:28 Europe/Rome) personally requested Google URL Inspection / request indexing for `https://www.evex.sh/agents`. Team must **NOT** re-request or nag. Morning pulse scores whether `/agents` leaves discovered-not-indexed. No metrics pull this note.

## 2026-09-06 ~22:24 CEST (#94 ship sync after evening run 78)

Delta since evening pulse (~21:35): TommyBez **merged #92** (06/09 **19:37 UTC / 21:37 CEST**) — clarify `/learn/install-eve-agent` by source/destination (optional/demoted; **NOT** a growth play). Then TommyBez **merged #94** (06/09 **20:22 UTC / 22:22 CEST**, HEAD `72fc333`) — Lock `/agents` index copy and prerender the catalog for crawlers. This is the **impact play** (Search Counsel #1). Soft Eng **dark** tonight.

PMM live-check **PASS** on prod `/agents`: **200**; title `Eve agents for the Eve agent framework | browse and install · evex`; H1 locked; 4 intro paras + `/docs/mcp`; Learn links kept; **15** crawlable `/agents/{slug}` hrefs; ItemList JSON-LD; old game/TV lede gone.

Open GTM PRs: **1** — **#93 OPEN** (home title/H1/lede; **demoted by Tommy**; optional polish — **NOT** a growth play). #92 closed merged; #94 closed merged. #588 still OPEN — do not nag.

PostHog / GSC / Typefully / north star: **no new pull this sync** — evening photograph stands (NS **11/15**; GSC trailing final 7d **~49.1/giorno**; next gate **10/09 ≥80**). Do not invent metrics.

Next: morning pulse score whether `/agents` leaves discovered-not-indexed; name next impact toward gate 10 Sep ≥80. **Not** link drip. Sunday backup still **22:30** tonight Europe/Rome. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-06 ~21:35 CEST (run 78, slot 21:20, evening, Sunday)

Delta since midday (run 77): Soft Eng/cloud agent opened **#92** (06/09 **13:05 UTC / 15:05 CEST**) — clarify `/learn/install-eve-agent` by source and destination (same URL; scaffold via `eve init`, catalog install via `@evex`/`@agentcn`, bergside standalone). CI verify + Vercel + CodeRabbit **SUCCESS**, review threads **0**, mergeable_state **blocked** (REVIEW_REQUIRED). Live site still pre-#92 on production for the new copy lock; hubs from #90 remain live: `/` `/agents` `/learn` install vs-agentcn `/docs` `/docs/installation` support-reply-draft **200**; `/learn/eve-agent-registry` **308→/docs**; `/learn` still **three** cards; sitemap **35**; stars **24**. Open GTM PRs: **1** (#92). #588 still OPEN — do not nag.

PostHog 244993. 06/09 Europe/Rome so far **20 pv / 13 uniques / 13 sess** (midday 8/6/6). Top: `/` 11u/12pv, brand-visual 2, leaderboard 1, `/agents` 1, code-reviewer 1, eve-agent-builder 1, supabase-data-analyst 1. 05/09 Rome full **11/7/7**. Launch 11/08–now **1245/578/667**. North star **11/15** unchanged (Soft Eng 19/08 excluded); last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day still **04/09** 0c/**62i**. Trailing final 7d **29/08–04/09** **344i (~49.1/giorno)** — ≥40 still clears. All-state **05/09 33i** (was 32 midday); **06/09 7i** (was 0). Money URL install still **0** page rows; retired registry **0**. vs-agentcn all-state ~7d **15i**; langgraph-vs-crewai **5i**; `/learn` **16i**; home **146i**; docs **105i**. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X still **43** impressions. Scheduled queue **empty** for 06/09; Mon–Tue 07–08/09 slots empty. Open drafts **10653428** (Skills Board BiP X) and **10653429** (Skills Board LI IT) + empty **10625176** — not Evex. Recent X analytics dominated by Skills Board BiP, not Evex.

Play this slot: Soft Eng **dark** (#92 already open; PR-comments routine watches). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent must (1) report Tommy in CoS chat only — ask merge of #92, note Sunday backup still 22:30, (2) brief PMM: #92 green awaiting merge + after live-check name **one next shippable** toward 300 (hygiene / internal links / non-definition money page — their call; not a pSEO grid; sit dead; do not reopen definition Learn), (3) STATE/LOG/topics synced to Mac `gtm/`. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-06 ~13:30 CEST (run 77, slot 13:20, midday, Sunday)

Delta since morning (run 76): TommyBez **merged #90** (06/09 **08:44 UTC / 10:44 CEST**) — crawlable Learn links from `/docs`, `/docs/installation`, and `/agents` into `/learn/install-eve-agent` and `/learn/evex-vs-agentcn`. Live-check **PASS**: both hubs expose crawlable `href="/learn/install-eve-agent"` and `href="/learn/evex-vs-agentcn"`. Open GTM PRs: **0**. Live site: `/` `/agents` `/learn` install vs-agentcn `/docs` `/docs/installation` support-reply-draft **200**; `/learn/eve-agent-registry` **308→/docs**; `/learn` still **three** cards; sitemap **35**; stars **24**. #86 remains merged/live. #588 still OPEN — do not nag.

PostHog 244993. 06/09 Europe/Rome so far **8 pv / 6 uniques / 6 sess** (morning 7/5/5). Top: `/` 5u/5pv, brand-visual 1, eve-agent-builder 1, supabase-data-analyst 1. 05/09 Rome full **11/7/7**. Launch 11/08–now **1239/572/662**. North star **11/15** unchanged (Soft Eng 19/08 excluded); last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day still **04/09** 0c/**62i**. Trailing final 7d **29/08–04/09** **344i (~49.1/giorno)** — ≥40 still clears. All-state **05/09 32i** (was 25i morning); **06/09 0i**. Money URL install still **0** page rows; retired registry **0**. vs-agentcn all-state ~7d **15i**; langgraph-vs-crewai **5i**; `/learn` **16i**; home **142i**; docs **105i**. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X still **43** impressions (morning photograph). Scheduled queue **empty** for 06/09; Mon–Tue 07–08/09 slots empty. Open draft **10625176** empty platforms / not Evex. Recent X analytics dominated by Skills Board BiP, not Evex.

Play this slot: Soft Eng **dark** (nothing open; live-check done; wait for PMM next shippable). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent must (1) report Tommy in CoS chat only — #90 is live, no merge waiting, (2) brief PMM: #90 live-check PASS + name **one next shippable** toward 300 (hygiene / internal links / non-definition money page — their call; not a pSEO grid; sit dead; do not reopen definition Learn), (3) STATE/LOG/topics synced to Mac `gtm/`. Sunday backup still 22:30 tonight. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-06 ~08:30 CEST (run 76, slot 08:20, morning, Sunday)

Delta since Saturday evening (run 75): **#90 still OPEN** (MERGEABLE, REVIEW_REQUIRED, CI verify + Vercel + CodeRabbit **SUCCESS**, review threads **0 unresolved**). Live site still pre-#90: `/` `/agents` `/learn` install vs-agentcn `/docs` support-reply-draft **200**; `/learn/eve-agent-registry` **308→200 /docs**; `/learn` still **three** cards; sitemap **35**; stars **24**. Live hubs do not yet show the #90 install+vs-agentcn crawlable anchors on `/agents`. #86 remains merged/live. #588 still OPEN — do not nag.

PostHog 244993. 06/09 Europe/Rome so far **7 pv / 5 uniques / 5 sess**. Top: `/` 5u/5pv, `/agents/brand-visual-asset-generator` 1, `/agents/eve-agent-builder` 1. 05/09 Rome full **11/7/7**. Launch 11/08–now **1232/570/659**. North star **11/15** unchanged (Soft Eng 19/08 excluded); last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day now **04/09** 0c/**62i** (was incomplete all-state 62i yesterday). Trailing final 7d **29/08–04/09** **344i (~49.1/giorno)** — ≥40 still clears (was ~44.1 through 03/09). All-state **05/09 25i** (was 8i evening). Money URL install still **0** page rows; retired registry **0**. vs-agentcn all-state ~7d **15i**; langgraph-vs-crewai **5i**; `/learn` **10i**; home **125i**; docs **99i**. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X still **43** impressions. Scheduled queue **empty** for 06–07/09. Open draft **10625176** empty platforms / not Evex. Recent X analytics dominated by Skills Board BiP, not Evex.

Play this slot: Soft Eng **dark** (#90 already open awaiting Tommy merge; PR-comments routine watches). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent must (1) report Tommy in CoS chat only — ask merge of #90, note GSC trailing now ~49.1/day, (2) brief PMM: #90 still green awaiting merge + after live-check name **one next shippable** toward 300 (hygiene / internal links / non-definition money page — their call; not a pSEO grid; sit dead; do not reopen definition Learn), (3) STATE/LOG/topics synced to Mac `gtm/`. Sunday backup still 22:30 tonight. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-05 ~21:35 CEST (run 75, slot 21:20, evening, Saturday)

Delta since midday (run 74): Soft Eng/cloud agent opened **#90** (05/09 **11:39 UTC / 13:39 CEST**) — crawlable Learn links from `/docs`, `/docs/installation`, and `/agents` into existing money pages `/learn/install-eve-agent` and `/learn/evex-vs-agentcn`. No new URLs, no homepage change, no citation drip. CI verify + Vercel **SUCCESS**, CodeRabbit pass (rate limited), review threads **0 unresolved**, mergeable_state **blocked** (review required). Live site still pre-#90: `/` `/agents` `/learn` install vs-agentcn `/docs` support-reply-draft **200**; `/learn/eve-agent-registry` **308→200 /docs**; `/learn` still **three** cards; sitemap **35**; stars **24**. #86 remains merged/live. #588 still OPEN — do not nag.

PostHog 244993. 05/09 Europe/Rome so far **11 pv / 7 uniques / 7 sess** (midday 7/5/5). Top: `/` 7u/8pv, `/agents` 2, `/docs` 1. 04/09 Rome full **30/14/17**. Launch 11/08–now **1225/566/654**. North star **11/15** unchanged (Soft Eng 19/08 excluded); last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day still **03/09** 0c/**41i**. Trailing final 7d **28/08–03/09** **309i (~44.1/giorno)** — ≥40 still clears. All-state **04/09 62i** (was 45i midday; firstIncompleteDate **04/09**); **05/09 8i** (was 0). Money URL install still **0** page rows; retired registry **0**. vs-agentcn all-state ~7d **14i** (was 10); langgraph-vs-crewai **6i**; `/learn` **23i**; home **156i**; docs **106i**. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X still **43** impressions. Scheduled queue **empty** for 05–06/09; Mon 07/09 slots empty. Open draft **10625176** empty platforms / not Evex.

Play this slot: Soft Eng **dark** (#90 already open; PR-comments routine watches). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent must (1) report Tommy in CoS chat only — ask merge of #90, (2) brief PMM: #90 green awaiting merge + after live-check name **one next shippable** toward 300 (hygiene / internal links / non-definition money page — their call; not a pSEO grid; sit dead; do not reopen definition Learn), (3) STATE/LOG/topics synced to Mac `gtm/`. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-05 ~13:35 CEST (run 74, slot 13:20, midday, Saturday)

Delta since morning (run 73): TommyBez **merged #86** (05/09 **07:58 UTC / 09:58 CEST**) — citation/voice pass on `/learn/evex-vs-agentcn` now live. Live-check **PASS**: title “Eve agent registries: evex vs agentcn · evex”; outbound primary sources include agentcn.run docs, github.com/shadcn-labs/agentcn (+ CONTRIBUTING), eve.dev getting-started/introduction; canonical `npx shadcn@latest add @evex/<slug>`. Live `/learn` still **three** cards (Install → vs-agentcn → LangGraph). `/learn/eve-agent-registry` still **308→200 /docs**. `/learn/install-eve-agent` **200**. Sitemap **35**. Stars **24**. Open GTM PRs: **0**. #588 still OPEN — do not nag.

PostHog 244993. 05/09 Europe/Rome so far **7 pv / 5 uniques / 5 sess** (morning 2/2/2). Top: `/` 5u/5pv, `/agents` 1, `/docs` 1. 04/09 Rome full **30/14/17**. Launch 11/08–now **1227/565/654**. North star **11/15** unchanged (Soft Eng 19/08 excluded); last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day now **03/09** 0c/**41i** (was 02/09 85i). Trailing final 7d **28/08–03/09** **309i (~44.1/giorno)** — ≥40 still clears. All-state **04/09 45i** (metadata firstIncompleteDate **04/09**); **05/09 0i**. Money URL install still **0** page rows; retired registry **0**. vs-agentcn all-state ~7d window **10i**; langgraph-vs-crewai **6i**; `/learn` **22i**; home **151i**; docs **93i**. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X still **43** impressions. Scheduled queue **empty** for 05–06/09. Open draft **10625176** is Skills Board, not Evex.

Play this slot: Soft Eng **dark** (nothing open; PR-comments routine watches). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent must (1) report Tommy in CoS chat only — citation page is live, no merge waiting, (2) brief PMM: #86 live-check PASS + GSC trailing ~44.1/day + name **one Saturday shippable** toward 300 (hygiene on install/vs-agentcn after live-check, internal links, or a non-definition money page — their call; not a pSEO grid; sit dead; do not reopen definition Learn), (3) STATE/LOG/topics synced to Mac `gtm/`. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-05 ~08:35 CEST (run 73, slot 08:20, morning, Saturday)

Delta since Friday evening (run 72): TommyBez **closed #84 without merge** (04/09 **20:01 UTC / 22:01 CEST**), then **merged #85** (04/09 **20:53 UTC / 22:53 CEST**) — retires `/learn/eve-agent-registry` with permanent redirect to `/docs` (live **308→200 /docs**). Soft Eng opened **#86** citation pass on `/learn/evex-vs-agentcn` (OPEN, MERGEABLE, CI/Vercel/CodeRabbit SUCCESS, **0** review threads). Live `/learn` now **three** featured cards: Install an Eve agent → evex vs agentcn → LangGraph vs CrewAI (no registry card). `/learn/install-eve-agent` **200**, `/learn/publish-eve-agent` **404**, sitemap **35** (was 36). Stars **24**. #588 still OPEN — do not nag.

PostHog 244993. 05/09 Europe/Rome so far **2 pv / 2 uniques / 2 sess** (home only). 04/09 Rome full **30/14/17**. Launch 11/08–now **1216/563/649**. North star **11/15** unchanged (Soft Eng 19/08 excluded); last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day still **02/09** 0c/**85i**. Final 7d **27/08–02/09** **296i (~42.3/giorno)** — trailing ≥40 still clears. All-state **03/09 41i**, **04/09 35i** (was 3i at evening). Money URL install still **0** page rows; retired registry also **0**. vs-agentcn has light all-state impressions. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X still **43** impressions. Scheduled queue **empty** for 05–06/09. Open drafts are Skills Board BiP (10629072, 10625176), not Evex.

Play this slot: **Q16 CLOSED as kill** (definition Learn line retired). Soft Eng **dark** (#86 already open; PR-comments routine watches). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent must (1) report Tommy in CoS chat only — ask merge of #86, (2) brief PMM: kill confirmed + #86 green awaiting merge + name one Saturday shippable toward 300 if they want one while merge waits (hygiene on install/vs-agentcn after live-check, internal links, or a non-definition money page — their call; not a pSEO grid; sit dead), (3) STATE/LOG/topics already synced to Mac `gtm/`. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-04 ~21:25 CEST (run 72, slot 21:20, evening, Friday)

Delta since midday (run 71): **#84 still OPEN** (MERGEABLE, CI/Vercel/CodeRabbit SUCCESS, 0 threads) — Tommy asked what the registry Learn page even is and called the “what is our product” Learn line artificial; CoS asked kill-vs-keep; **no clear merge/kill answer yet**. PMM had locked vs-agentcn citation pass next, Soft Eng **DARK** until #84 live-check PASS. Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken this evening.

Live site unchanged: `/learn` **four** cards (registry → Install → vs-agentcn → LangGraph), `/learn/eve-agent-registry` + `/learn/install-eve-agent` **200**, `/learn/publish-eve-agent` **404**, sitemap **36**, stars **24**. #588 still OPEN — do not nag.

PostHog 244993. 04/09 Europe/Rome so far **24 pv / 13 uniques / 15 sess** (midday 8/5/6). Top: `/` 12u/15pv, `/agents` 1u/2pv, **`/learn/eve-agent-registry` 1u/2pv**, support-reply-draft 1, openui 1, x-draft 1, brand-visual 1, leaderboard 1. 03/09 Rome full **60/21/23**. Launch 11/08–now **1208/560/645**. North star **11/15** unchanged; last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

GSC (sc-domain:evex.sh, service account, no inspect): final last complete day still **02/09** 0c/**85i**. Final 7d **27/08–02/09** **296i (~42.3/giorno)** — trailing ≥40 still clears. All-state **03/09 41i**, **04/09 3i** (incomplete). Money URLs `/learn/eve-agent-registry` + `/learn/install-eve-agent` still **0** page rows. Learn rows that do exist: langgraph-vs-crewai 27i, vs-agentcn 17i, old `/learn/agent-registry` 4i. Next gate **10/09 ≥80**.

Typefully get_me **200**, set 266935. Evex support-reply-draft X **43** impressions (was 41). Scheduled queue **empty**. Open drafts are Skills Board BiP (10629072, 10625176), not Evex.

Play this slot: **HOLD** #84 and vs-agentcn Soft Eng wake until Tommy decides whether the Learn “definition / what is the product” line stays. Soft Eng dark. Parent must (1) report Tommy in CoS chat only — ask the clear kill-or-keep call, (2) brief PMM with HOLD + evening delta, (3) sync STATE/LOG/topics to Mac `gtm/` (morning+midday never landed on Mac). Do not nag #588. Do not tweet install copies. Do not request indexing. Do not post Slack.

## 2026-09-04 ~13:45 CEST (run 71, slot 13:20, midday, Friday)

Delta since morning run 70 (~08:45 CEST): PMM locked Friday play — light citation/voice pass on existing `/learn/eve-agent-registry` only (no new URL). Soft Eng opened **#84** (`70394722`, MERGEABLE, CI/Vercel/CodeRabbit SUCCESS, 0 review comments). Live `/learn` still **four** featured cards (registry → Install → vs-agentcn → LangGraph). `/learn/install-eve-agent` and `/learn/eve-agent-registry` **200**. `/learn/publish-eve-agent` still **404**. Sitemap **36**. Stars **24**. #588 still OPEN — do not nag.

PostHog 244993. 04/09 Europe/Rome so far **8 pv / 5 uniques / 6 sess** (morning 1/1/1). Top paths so far: `/` 4u/6pv, `/agents` 1, `/leaderboard` 1. Refs: **$direct** only. 03/09 Rome full **60/21/23** (notable: `/learn/install-eve-agent` **3u/7pv**). Launch 11/08–now **1192/552/636**. North star **11/15** unchanged; last copies still 03/09 14:55–14:56 CEST sticky `/agents/code-reviewer`. Score-only: do not tweet.

**GSC (sc-domain:evex.sh, service account, no inspect):** final last complete day now **02/09** 0c/**85i** (was missing this morning). Final 7d **27/08–02/09** **296i (~42.3/giorno)** — trailing ≥40 on complete finals **now clears** (gate day 3/09 had scored miss on 26/08–01/09 ~34). All-state 03/09 **40i** (morning photograph had 32). All-state 28/08–03/09 **308i (~44/giorno)**. 04/09 all-state still 0. Money URLs `/learn/eve-agent-registry` and `/learn/install-eve-agent` still **no page impression rows**. Top pages 7d all-state: home 138i, docs 79i, CR 46i, brand-visual 30i, `/learn` 22i, GCI 19i, vs-agentcn 8i. Next gate **10/09 ≥80/giorno**.

Typefully get_me **200**, set 266935. support-reply-draft X still **41** impressions. One open draft (10614542 BiP-X-24 agent readability) — not Evex ship queue. No Evex scheduled today.

Play this slot: Soft Eng **dark** (PR already open; PR-comments routine watches). Soft Eng/SEO agent/Publisher Scout/Search Counsel **not** woken. Parent FYIs PMM: #84 green awaiting Tommy merge; live-check `/learn/eve-agent-registry` after 200; name next shippable toward 300 if they want one while merge waits. Do not nag #588. Do not tweet install copies. Do not request indexing. Parent must (1) report Tommy in this CoS chat only in full sentences (no Slack) — ask merge of #84, (2) FYI PMM, (3) sync STATE/LOG/topics to Mac `gtm/` when write surface available (staging `/workspace/chief-of-staff/pulse-midday-0904/` + push TommyBez/evex-gtm-backup).

## 2026-09-04 ~08:45 CEST (run 70, slot 08:20, morning, Friday)

Delta since Thursday evening (run 69): TommyBez **merged #83** (03/09 **20:11 UTC / 22:11 CEST**) then **#81** (03/09 **20:37 UTC / 22:37 CEST**), both after the evening photograph. Live `/learn/install-eve-agent` **200** with primary-source outbound links (agentcn, bergside/eveagents, eve.dev). Live `/learn` now **four** featured cards in order: Eve agent registry → **Install an Eve agent** → evex vs agentcn → LangGraph vs CrewAI. Money page `/learn/eve-agent-registry` still **200**. `/learn/publish-eve-agent` still **404**. Sitemap **36**. Stars **24**. Open GTM PRs: **none**. #588 still OPEN — do not nag.

PostHog 244993 confirmed. North star **11 people / 15 copies** (SQL, Soft Eng 19/08 19:27 UTC `/agents/code-reviewer` excluded). Evening STATE 12/16 was overcount; corrected. Last copies still 03/09 14:55–14:56 CEST sticky on `/agents/code-reviewer` (same unsigned person, two events). Score-only: do not tweet. 04/09 Rome so far **1/1/1**. 03/09 Rome full **60/21/23**. Launch 11/08–now **1185/549/631**.

GSC (sc-domain:evex.sh, service account, no inspect): last complete day **01/09** 0c/**55i**. 7d final 26/08–01/09 **2c / 240i (~34.3/giorno)** — gate ≥40 still miss. 02–04/09 final NO_ROWS; all-state provisional 02/09 85i, 03/09 32i (~42–43/day if provisional were final — not yet). Goal 300/giorno.

Typefully: get_me 200, set 266935. Queue 04/09 10:00Z & 15:00Z **empty**. Recent X analytics dominated by Skills Board BiP thread (#10598386), not Evex. Do not invent Evex impressions.

Play this slot: brief PMM for one Friday shippable toward 300 (no open code PR waiting). Soft Eng idle unless PMM names code. Do not nag #588. Do not tweet install copies. Do not request indexing. Mac not connected — STATE/LOG drafted under `/workspace/chief-of-staff/pulse-morning-0904/`; parent should sync to `gtm/` when Mac is available.

## 2026-09-03 ~23:12 CEST (team cut, after run 69)

Tommy: Publisher Scout off the Evex GTM team (same night as SEO agent). Pulses do not wake Scout. Registry supply/invites are not a standing seat. Core remains CoS, PMM, Soft Eng. Search Counsel consultant-only.

## 2026-09-03 ~22:20 CEST (run 69, slot 21:20, evening, Thursday)

Delta since Wednesday evening (run 68): STATE was not rewritten at Thursday morning/midday; this entry covers the Thursday ship. TommyBez **merged #82** afternoon (03/09 **16:26 UTC / 18:26 CEST**). Live `/learn/install-eve-agent` recut **200** (H1 Install an Eve agent · evex; Eve vs catalog paths; canonical `npx shadcn@latest add @evex/<slug>`). Live `/learn` still **three** cards only (registry → vs-agentcn → LangGraph vs CrewAI) — **no** fourth featured card. Money page `/learn/eve-agent-registry` still **200**. `/learn/publish-eve-agent` still **404**. Sitemap **36**. Stars **24**. #588 still OPEN — do not nag.

Open GTM PRs: **#83** https://github.com/TommyBez/evex/pull/83 citation pass OPEN, mergeable earlier in the slot, CI verify + Vercel + CodeRabbit **SUCCESS**, REVIEW_REQUIRED. **#81** https://github.com/TommyBez/evex/pull/81 featured card OPEN, rebased ~22:09 CEST, verify + Vercel SUCCESS, CodeRabbit pending. **HOLD #81** until PMM live-checks #83 after merge.

PostHog 244993 (project confirmed). 03/09 Europe/Rome so far **57 pv / 19 uniques / 21 sess**. 02/09 Rome full **23/13/14** (evening 02/09 had 7/6/6 while the day was open). 01/09 **44/17/18**. 31/08 **107/40/40**. Launch 11/08–03/09 ~22:20 **1187/547/630**.

North star **12 people / 16 copies** (was 10/13). New: one unsigned person, two sticky copies on `/agents/code-reviewer` at 03/09 12:55–12:56 UTC / **14:55–14:56 CEST**. Score-only: do not tweet. Soft Eng 19/08 test excluded.

GSC (sc-domain:evex.sh, service account, no inspect): last complete day **01/09** 0c/**55i** (31/08 0c/50i). 7d 26/08–01/09 **2c / 240i (~34.3/giorno)**. 02/09 and 03/09 **no rows**. Goal 300/giorno; **Thursday 3/09 ≥40/giorno not met** on complete-day average (~34). Last two complete days (50 then 55) are the first above 40.

Typefully: get_me 200, set 266935. Evex post **2094825110788345928** → X **41** impressions (`[@]evex/support-reply-draft`). Scheduled **#10598386** published 18:30 CEST — Skills Board BiP thread (not Evex). LinkedIn **#10541117** published 03/09 08:30 CEST (Skills Board IT). Queue **empty**.

Play this slot: citation pass already locked; parent reported Tommy in CoS chat and briefed PMM. PMM live-check after #83 merge, then unblock #81. Ask PMM for one Friday shippable toward 300 if #83 is live, else a fallback that does not wait on Tommy. Do not nag #588. Do not tweet install copies. Do not request indexing. Do not reopen #77.


## 2026-09-02 ~21:30 CEST (run 68, slot 21:20, evening, Wednesday)

Delta since midday (run 67): TommyBez **merged #80** afternoon (02/09 **11:54 UTC / 13:54 CEST**). Live `/learn/install-eve-agent` **200** (title/H1 Install an Eve agent · evex; canonical `npx shadcn@latest add @evex/<slug>`; links to /agents, eve-agent-registry, /docs/installation). Live `/learn` still **three** cards only (registry → vs-agentcn → LangGraph vs CrewAI) — **no** fourth featured card. In-body links present on `/docs` and `/docs/installation`. Money page `/learn/eve-agent-registry` still **200**. `/learn/publish-eve-agent` still **404**. Sitemap **36**. Stars **24**. #588 still OPEN — do not nag. Open GTM PRs: **0**. Infra #75 (eve 0.47.5) also merged ~17:32 CEST, out of GTM scope.

PostHog 244993 (project confirmed). 02/09 Europe/Rome so far **7 pv / 6 uniques / 6 sess**. Launch 11/08–02/09 ~21:30 **1128/527/607**.

North star **10 people / 13 copies** (unchanged; Soft Eng 19/08 test excluded). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect): last day with rows **31/08** 0c/**50i**. 7d 23–29 **5c / 184i (~26.3/giorno)**. 30/08 0c/26i. 01/09 and 02/09 final-state empty (midday all-state had 01/09 **47i**). Goal 300/giorno; **Wednesday 3/09 ≥40/giorno not met** on complete-day average.

Typefully: get_me 200, set 266935. Evex post **2094825110788345928** → X **39** impressions, 0 likes/replies/retweets (`[@]evex/support-reply-draft`). Scheduled **#10567591** published 18:30 CEST — Skills Board BiP thread (not Evex). LinkedIn **#10541117** still scheduled 03/09 08:30 CEST (Skills Board IT).

Play this slot: PMM already locked `/learn/install-eve-agent` after midday; Soft Eng opened and Tommy merged #80. Evening live-check **PASS**. Soft Eng/SEO **not** woken (nothing left open). Parent must (1) report Tommy in CoS chat only in full sentences (no Slack), (2) FYI PMM live-check PASS on install page + three-card /learn + docs inlinks. Tomorrow morning gate recap: inspect piece ok; ≥40 still miss. Do not nag #588. Do not tweet OpenUI. Do not request indexing.


## 2026-09-02 ~13:30 CEST (run 67, slot 13:20, midday, Wednesday)

Delta since morning (run 66): TommyBez **merged #79** midday (02/09 **10:03 UTC / 12:03 CEST**). Live `/learn` live-check **PASS**: three guide cards in order Eve agent registry → vs-agentcn → LangGraph vs CrewAI; registry one-liner present; no publish-eve-agent card. `/learn/eve-agent-registry` still **200**. Site core still **200** (/, /agents, support-reply-draft, /learn, /docs, /docs/publishing, vs-agentcn). `/learn/publish-eve-agent` still **404**. Sitemap still **35**. Stars **24**. #588 still OPEN — do not nag. Open GTM PRs: **0**. #75 eve upgrade still open, out of scope.

PostHog 244993 (project confirmed). 02/09 Europe/Rome so far **7 pv / 6 uniques / 6 sess**. Top pages: `/` 6/6, x-draft-assistant 1/1. Top referrer **$direct** 6u/7pv. 01/09 Rome **44/17/18**. 31/08 Rome **107/40/40**. 30/08 Rome **24/12/13**. Launch 11/08–02/09 ~13:25 **1108/522/599** (morning cited 1112 pv; uniques/sessions unchanged).

North star **10 people / 13 copies** (unchanged; Soft Eng 19/08 test excluded). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect this slot): last complete day still **30/08** 0c/26i. 7d 23–29 **5c / 184i (~26.3/giorno)**. 31/08 all-state 0c/**50i**. 01/09 all-state 0c/**47i** (was 23i at morning; still incomplete). 02/09 all-state empty. Goal 300/giorno; **Wednesday 3/09 ≥40/giorno still not met** on complete-day average.

Typefully: get_me 200, set 266935. Post **2094825110788345928** → X **37** impressions / Typefully analytics **33**, 0 likes/replies/retweets (`[@]evex/support-reply-draft`). Scheduled drafts: **#10567591** X for 02/09 18:30 CEST; **#10541117** LinkedIn for 03/09 08:30 CEST.

Play this slot: Soft Eng/SEO **not** woken (live-check PASS after #79). Automation cannot SendToAgent: parent must (1) report Tommy in CoS chat only in full sentences (no Slack), (2) FYI PMM that #79 is live with three cards and ask them to name **one Wednesday evening shippable move** toward 300 daily GSC impressions (hygiene on discovered-not-indexed hub/GIM/DKA, internal links, or next query-shaped money page — their call; not a pSEO grid; sit dead; do not reopen #77). Do not nag #588. Do not tweet OpenUI. Do not request indexing.

## 2026-09-02 ~08:35 CEST (run 66, slot 08:20, morning, Wednesday)

Delta since Tuesday evening (run 65): TommyBez **merged #78** overnight (01/09 20:16 UTC / **22:16 CEST**, HEAD `1093990ed121cee5f25804795dcff66449e79cd2`). Live `/learn/eve-agent-registry` now **200** (title Eve agent registry · evex). Sitemap **35** (was 34). Site core still **200** (/, /agents, support-reply-draft, /learn, /docs, /docs/publishing, vs-agentcn). `/learn/publish-eve-agent` still **404** (#77 stays closed). Stars **24**. #588 still OPEN — do not nag. Open GTM PRs before Soft Eng wake: **0** (#75 eve upgrade remains out of scope).

PostHog 244993 (project confirmed). 02/09 Europe/Rome so far **5 pv / 4 uniques / 4 sess**. Top pages: `/` 4/4, x-draft-assistant 1/1. Top referrer **$direct** 4u/5pv. 01/09 Rome **44/17/18**. 31/08 Rome **107/40/40**. 30/08 Rome **24/12/13**. Launch 11/08–02/09 08:30 **1112/522/599**.

North star **10 people / 13 copies** (unchanged when grouped by person_id; Soft Eng 19/08 test excluded). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect this slot): last complete day now **30/08** 0c/26i. 7d 23–29 **5c / 184i (~26.3/giorno)**. 31/08 all-state 0c/**50i**. 01/09 all-state 0c/**23i** (was empty at evening). 02/09 all-state empty. Goal 300/giorno; **Wednesday 3/09 ≥40/giorno still not met** on complete-day average. Inspect ≠ unknown piece of the gate already passed on 1/09.

Typefully: MCP status flaky (needsAuth) but X confirms publish. Social set 266935. Post **2094825110788345928** → **34 impressions**, 0 likes/replies/retweets (`[@]evex/support-reply-draft`).

Play this slot (PMM evening lock after #78 merge): Soft Eng opened **#79** https://github.com/TommyBez/evex/pull/79 — ONE featured card on indexed `/learn` for eve-agent-registry (title **Eve agent registry**; one-line **Browse the catalog, inspect every file, and install with one shadcn command**). Marked ready for review; CI verify/Vercel/CodeRabbit green. Live `/learn` already inlines the registry link in header copy; guide card grid still only vs-agentcn + LangGraph vs CrewAI until merge. SEO / Search Counsel **not** woken. Do not nag #588. Do not tweet OpenUI. Do not request indexing. Parent must report Tommy + Slack in full sentences and FYI PMM that #78 is live and #79 awaits merge.

## 2026-09-01 ~21:25 CEST (run 65, slot 21:20, evening, Tuesday)

Delta since midday (run 64): site core still **200** (/, /agents, support-reply-draft, /learn, /docs, /docs/publishing, vs-agentcn). `/learn/publish-eve-agent` still **404**. `/learn/eve-agent-registry` still **404** (PR not merged). Sitemap still **34**. Stars **24**. #588 still OPEN — do not nag.

**Shipping since midday:**
- PMM recut the money page away from closed #77 onto **`/learn/eve-agent-registry`**. Soft Eng opened **#78** from main (~14:55 CEST). CI verify + Vercel + CodeRabbit green. Soft Eng / PR-comments routine cleared review threads (**0 unresolved**). Preview ready. Does **not** reopen #77.
- Typefully draft **10560773** **published** at 18:30 CEST → https://x.com/TommyBez85/status/2094825110788345928 (`[@]evex/support-reply-draft`). X metrics at check: 21 impressions.
- Draft infra **#75** still open (eve 0.47.5), out of GTM scope.

PostHog 244993 (project confirmed). 01/09 Europe/Rome so far **44 pv / 17 uniques / 18 sess**. Top pages: `/` 26/15, brand-visual 7/6, `/agents` 4/4, support-reply-draft 1. Top referrers **$direct** 22/9, **api.daily.dev** 21/7, **t.co** 1/1. 31/08 Rome **107/40/40**. 30/08 Rome **24/12/13**. 29/08 Rome **30/13/14**. Launch 11/08–01/09 21:25 **1107/519/595**.

North star **10 people / 13 copies** (unchanged; Soft Eng 19/08 test excluded). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect this slot): last complete day still **29/08** 1c/25i. 7d 23–29 **5c / 184i (~26.3/giorno)**. 30/08 all-state 0c/26i. 31/08 all-state 0c/**50i** (was 33i at midday). 01/09 all-state 0c/0i. Goal 300/giorno; Wednesday 3/09 ≥40/giorno still **not met**.

Typefully: MCP status flaky (needsAuth) but X confirms publish. Social set 266935.

Play this slot: Soft Eng/SEO **not** woken (threads already clean). Ask Tommy to **merge #78** tonight so the registry Learn page lands before the Wed gate. Automation cannot SendToAgent: parent must (1) report Tommy + Slack in full sentences, (2) FYI PMM that Typefully is live and #78 awaits merge, (3) sync STATE/LOG/topics to Mac gtm/ when the write surface is available (staging at `/workspace/evex-gtm/pulse-run65/`). Do not nag #588. Do not tweet OpenUI. Do not request indexing.


## 2026-09-01 ~13:35 CEST (run 64, slot 13:20, midday, Tuesday)

Delta since morning (run 63): site core still **200** (/, /agents, support-reply-draft, /learn, /docs, /docs/publishing). Sitemap still **34**. Stars **24**. #588 still OPEN — do not nag. Soft Eng has no open GTM review threads.

**Shipping drama since morning inspect:**
- **#76 MERGED** 01/09 08:41 UTC / 10:41 CEST by TommyBez (`a014bec…`). Live: `/docs` in-body catalog links + `/docs/publishing` H2 “Publish an Eve agent, or vercel deploy?” with canonical install in inline code. This was the morning “docs theater” PR Tommy later said was not the day’s work.
- PMM locked money page **`/learn/publish-eve-agent`** (title/H1 Publish an Eve agent; AIO query “publish eve agent”). Soft Eng opened **#77** from main; verify/Vercel green; Codex `{slug}` thread resolved keeping `@evex/<slug>`.
- **TommyBez CLOSED #77** 01/09 08:40 UTC / 10:40 CEST (one minute before merging #76) and **deleted** branch `cursor/learn-publish-eve-agent-b63e`. Live `/learn/publish-eve-agent` **404**; not in sitemap. No reopen without Tommy confirmation.
- Draft infra **#75** (eve 0.47.5) still open draft, out of GTM scope.

PostHog 244993 (project confirmed). 01/09 Europe/Rome so far **26 pv / 11 uniques / 11 sess**. Top pages: `/` 15/9, brand-visual 4/4, `/agents` 3/3, support-reply-draft 1, code-reviewer 1, x-draft 1, x-hot-topic 1. Top referrer **api.daily.dev** 20pv/7u, then $direct 6/4. 31/08 Rome **107/40/40**. 30/08 Rome **24/12/13**. 29/08 Rome **30/13/14**. Launch 11/08–01/09 13:30 **1083/514/586**.

North star **10 people / 13 copies** (unchanged). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect this slot): last complete day still **29/08** 1c/25i. 7d 23–29 **5c / 184i (~26.3/giorno)**. 30/08 all-state 0c/26i. 31/08 all-state 0c/**33i** (was 27i at morning). 01/09 no row. Goal 300/giorno; Wednesday 3/09 ≥40/giorno still **not met**.

Typefully up (get_me 200, set 266935). Draft **10560773** still **scheduled** for **2026-09-01T16:30:00Z (18:30 CEST)**. GET still has `[@]evex/support-reply-draft`. Not published yet.

Play this slot: Soft Eng/SEO **not** woken to reopen #77 (Tommy closed it deliberately and deleted the branch). Automation cannot SendToAgent: parent must (1) ask Tommy whether to reopen/fresh-PR the money page or treat the close as a reject and have PMM recut, (2) FYI PMM that #77 is closed/404 while #76 is live, (3) report Tommy + Slack. Typefully stands. Do not nag #588. Do not tweet OpenUI. Do not request indexing.



## 2026-09-01 ~08:40 CEST (run 63, slot 08:20, morning, Tuesday)

Delta since Monday evening (run 62): site still all **200**, sitemap **34**. Open GTM PRs **0**. Draft infra PR **#75** (Upgrade eve to 0.47.5) still out of GTM scope. Stars **24**. #588 still OPEN, Vercel bot only — do not nag. Soft Eng stays dark (no new GTM review threads). AI-SEO monthly DIY already ran ~08:20 (see voce sotto).

PostHog 244993 (project confirmed). 01/09 Europe/Rome so far **19 pv / 7 uniques / 7 sess** (bounce ~14%, avg ~368s). Top pages: `/` 6/11, brand-visual-asset-generator 3/3, `/agents` 2/2, code-reviewer 1, x-draft-assistant 1, x-hot-topic-digest 1. Top referrer **api.daily.dev** 17pv/5u, then $direct 2/2. **31/08 Rome restated 107/40/40** (evening pulse had 95/34/34 while the Rome day was still open). 30/08 UTC **23/13/14**. 29/08 UTC **35/14/15**. Launch 11/08–01/09 08:30 **1082/513/584**.

North star **10 people / 13 copies** (unchanged). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account): last complete day still **29/08** 1c/25i. 7d 23–29 **5c / 184i (~26.3/giorno)**. 30/08 all-state 0c/26i (was 12i). 31/08 all-state 0c/27i. 01/09 no row. Goal 300/giorno by 27/09; Wednesday 3/09 gate ≥40/giorno is **not met** on complete-day average.

**URL Inspection 1/09 (first allowed check, read-only, 7/7 HTTP 200):**
- Submitted and indexed: `/` (crawled 27/08), `/learn` (crawled 29/07), `/learn/evex-vs-agentcn` (crawled 20/08). Verdict PASS.
- Discovered - currently not indexed (not unknown): `/agents`, `/agents/github-issue-maintainer`, `/agents/docs-knowledge-assistant`. No lastCrawlTime. Verdict NEUTRAL.
- URL is unknown to Google: `/agents/support-reply-draft` (live since yesterday). Verdict NEUTRAL.
Gate 3/09 inspect ≠ unknown on the five named URLs: **pass** (none are unknown). Hub is discovered-not-indexed, so Search Counsel’s “if hub still unknown, Soft Eng verifies crawlable links” does **not** fire. Do not request indexing. Do not Indexing API. Do not GSC UI click.

Typefully up (get_me 200, set 266935). Draft **10560773** still **scheduled** for **2026-09-01T16:30:00Z (18:30 CEST)**. GET still has `[@]evex/support-reply-draft`. Not published yet. CI explainer 38/0/0/0, DKA 55/1/0/0, GIM 107/5/1/2 unchanged.

Soft Eng/SEO not woken this slot (inspect was the locked morning play; next shippable move is PMM’s). Automation cannot SendToAgent: parent should brief PMM with the inspect table and ask them to name **one Tuesday shippable move** toward 300 daily GSC impressions (hygiene on discovered-not-indexed hub/GIM/DKA, internal links, query-shaped money page after a Search Counsel look, or publish-intent Learn/docs — their call; not a pSEO grid; sit is dead). Do not nag #588. Do not tweet OpenUI. Typefully fires tonight; no second first-party agent this morning.

## 2026-09-01 ~08:20 CEST (AI-SEO monthly visibility, first DIY run)

Monthly DIY AI-SEO check (Tommy approved 2026-08-13; paid tools deferred). Skill: `.agents/skills/ai-seo`. Context: STATE, packs/ai-seo-proposal-2026-08-12.md, `.agents/product-marketing.md`. No PRs opened.

**Coverage:** Google AI Overviews (browser, all 10 queries) + public SERP backup (WebSearch). **ChatGPT and Perplexity blocked** on the box (both require sign-in; no anonymous answers). Flag for Tommy: one Chrome login on the box unblocks next month.

### Query set (10)
eve agent registry · evex.sh · install eve agents · evex vs agentcn · npx shadcn add evex · publish eve agent · vercel eve registry · eve agents marketplace · @evex registry · how to install eve agents

### Google AI Overviews (hl=en, US IP)

| Query | AIO | Names evex | Canonical install | Citations | Gaps / notes |
| --- | --- | --- | --- | --- | --- |
| eve agent registry | yes | yes | wrong (generic shadcn add, no `@evex/<slug>`) | yes evex.sh | Atom Eve named as peer |
| evex.sh | yes | yes | absent | yes evex.sh + GitHub | Brand owned; disambiguates EVEX stock |
| install eve agents | yes | yes | **yes** `@evex/code-reviewer` | yes | Strong win |
| evex vs agentcn | yes | yes | **yes** | learn page | Full comparison table; choose-evex close |
| npx shadcn add evex | yes | yes | partial | yes | Eve Directory in organic |
| publish eve agent | yes | **no** | absent | absent | AIO = Vercel deploy, not registry PR |
| vercel eve registry | **no** | — | — | — | evex absent page 1; eveagents.dev in mix |
| eve agents marketplace | yes | **no** | absent | absent | Points at Awesome Eve Agents / bergside |
| @evex registry | **no** | — | — | — | Organic fully owned; docs snippet has canonical install |
| how to install eve agents | yes | yes | **yes** | partial | Also mentions stray `eve add` (daily.dev / Vercel integrations) |

Score: **8/10 AIO present; evex named in 6.** Canonical install verbatim in 3 AIOs. No AIO invented `eve add https://evex.sh/r/...`.

### Public SERP backup (no browser)
Brand / namespace / shadcn-install / vs-agentcn: evex dominates. Gaps: `install eve agents` + `how to install eve agents` still scaffold/bergside-owned in classic SERP (AIO is ahead of organic here); `publish eve agent` = deploy; `eve agents marketplace` = evedirectory. `llms.txt` + `robots.txt` healthy (AI bots allowed, Content-Signal yes, install present).

### Gaps for Soft Eng / SEO (no PR this run)
1. **Publish intent:** title/structure `/docs/publishing` so AIO stops answering Vercel deploy for "publish eve agent".
2. **Marketplace / open-registry phrasing:** evedirectory + bergside own the phrase; consider Learn/FAQ extractable blocks (PMM call, not a pSEO grid).
3. **vercel eve registry:** get on page 1 / into AIO (third-party registry presence on eve.dev docs already helps elsewhere).
4. **Stray `eve add`:** only in how-to AIO via daily.dev; monitor, do not chase with wrong install in our copy.
5. **Standout asset:** `/learn/evex-vs-agentcn` is doing real AIO work — model for other comparison/definition blocks.
6. **Ops:** box ChatGPT + Perplexity need one human sign-in before Oct 1 DIY run.

Detail stays here; snapshot in STATE + topics/seo.md.

## 2026-08-31 ~21:25 CEST (run 62, slot 21:20, evening, Monday)

Delta since midday (run 61): **support-reply-draft** still **200**, sitemap **34**. Open GTM PRs **0**. Draft infra PR **#75** (Upgrade eve to 0.47.5) exists but is out of GTM scope — Soft Eng not woken. Stars **24**. #588 still OPEN, Vercel bot only — do not nag. Soft Eng stays dark (no new GTM review threads).

PostHog 244993 (project confirmed). 31/08 Europe/Rome **95 pv / 34 uniques / 34 sess** (bounce ~18%, avg ~224s) — up from midday 51/19/19. Top pages: `/` 54/33, brand-visual 10/10, leaderboard 7/7, `/agents` 6/6, `/learn` 3/3. Top referrer **api.daily.dev** 61pv/19u, then $direct 31/15. 30/08 UTC **23/13/14**. 29/08 **35/14/15**. Launch 11–31 **1045/501/569**.

North star **10 people / 13 copies** (unchanged). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect): last complete day still **29/08** 1c/25i. 7d 23–29 **5c / 184i (~26/giorno)**. 30/08 and 31/08 still empty in API. Inspect still locked until **1 Sep morning**. Goal 300/giorno by 27/09; Wednesday 3/09 gate ≥40/giorno + inspect ≠ unknown on hub/GIM/DKA/Learn.

Typefully up (get_me 200, set 266935). Draft **10560773** moved from plain draft to **scheduled** for **2026-09-01T16:30:00Z (18:30 CEST)** — Tommy scheduled it ~20:33 CEST. GET still has `[@]evex/support-reply-draft`. Not published yet. CI explainer remains last live Evex X until that fires.

Monday standing play (Land #74 → Typefully after 200) is **closed**. Soft Eng/SEO not woken. Automation cannot SendToAgent: parent should brief PMM that the land play is done, Typefully is scheduled for tomorrow evening, and ask them to name **one Tuesday morning shippable move** toward 300 daily GSC impressions (hygiene / query-shaped money page after Search Counsel look / other — their call; not a pSEO grid; sit is dead). Do not nag #588. Do not tweet OpenUI. No second first-party agent tonight.

## 2026-08-31 ~13:35 CEST (run 61, slot 13:20, midday, Monday)

Delta since morning (run 60): **#74 MERGED** 31/08 08:59 CEST by TommyBez (HEAD `d9fc4a619d3adfc5b2ddb2ad7b4bd3256b95bd07`). Live `/agents/support-reply-draft` now **200** (title Eve support reply agent). Sitemap **34** (was 33; includes support-reply-draft). Open PRs **0**. Stars **24**. Review threads still 0 unresolved. No new PR comments after merge. Soft Eng stays dark. #588 still OPEN, Vercel bot only — do not nag.

PostHog 244993 (project confirmed). 31/08 Europe/Rome so far **51 pv / 19 uniques / 19 sess** (bounce ~16%, avg ~316s). Top pages: `/` 30/19, brand-visual 5/5, leaderboard 3/3, `/agents` 2/2, `/learn` 2/2. Top referrer **api.daily.dev** 37pv/10u, then $direct 12/8. 30/08 UTC **23/13/14**. 29/08 **35/14/15**. Launch 11–31 **1001/488/554**.

North star **10 people / 13 copies** (unchanged). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

GSC (sc-domain:evex.sh, service account, no inspect): last complete day now **29/08** 1c/25i (final). 7d 23–29 **5c / 184i (~26/giorno)**. 30/08 all-state 0c/12i; 31/08 not in yet. Inspect still locked until **1 Sep** (tomorrow). Goal 300/giorno by 27/09; Wednesday 3/09 gate ≥40/giorno + inspect ≠ unknown on hub/GIM/DKA/Learn.

Typefully up (get_me 200, set 266935). Standing PMM play executed: created draft **10560773** from [drafts/support-reply-draft-x-2026-08-30.md](drafts/support-reply-draft-x-2026-08-30.md). Status draft, no publish_at/plan_at. GET confirmed `[@]evex/support-reply-draft` in body. Suggested 18:00 CEST today for Tommy to publish. CI explainer still last live Evex X (38/0/0/0).

Play executed from morning PMM lock (Land #74 → Typefully after 200). Soft Eng/SEO not woken. Automation cannot SendToAgent: parent should FYI PMM that #74 is live and draft 10560773 is ready, and ask if midday play changes anything before evening. Do not nag #588. Do not tweet OpenUI. No second first-party agent.

## 2026-08-31 ~08:35 CEST (run 60, slot 08:20, morning, Monday)

Monday first run: rolled W35 into [log/2026-W35.md](log/2026-W35.md). This file is now W36 only.

Delta since Sunday evening (run 59): **#74** still OPEN https://github.com/TommyBez/evex/pull/74 HEAD `d9fc4a619d3adfc5b2ddb2ad7b4bd3256b95bd07`. Review threads **0 unresolved** (8/8 resolved). verify / Vercel / typecheck / discover / CodeRabbit green. mergeStateStatus BLOCKED = review required. No new comments overnight. Live `/agents/support-reply-draft` still **404**. Sitemap 33. Stars **24**. #588 still OPEN, only Vercel bot comment, no human. Hub `/agents`, GIM, DKA, CI explainer, `/learn` all 200.

PostHog 244993 (project confirmed, SQL north star with Tommy unsigned-null rule, Soft Eng 19/08 sticky test excluded). 31/08 so far **4 pv / 3 uniques / 3 sess** (bounce ~33%, avg ~10s). Pages today: `/` 3vis/3pv, `/agents/brand-visual-asset-generator` 1/1. Referrers: $direct only. **30/08 restated 23/13/14** (evening pulse had 5/3/3 while the UTC day was still open; bounce ~43%, avg ~246s). 29/08 **35/14/15**. Launch 11–31 **958/476/540**.

North star **10 people / 13 copies** (unchanged). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant` (3 copies, one person; session utm ui.shadcn.com / allshadcn). Score-only: do not tweet OpenUI. Copies since 26/08 22:00 UTC: openui-assistant 3/1, brand-visual-asset-generator 1/1.

Typefully up (get_me 200, set 266935). No new Evex draft. Open drafts in the set are Skills Board / BiP, not support-reply-draft. Latest Evex X remains CI explainer 10521782 → 38/0/0/0. DKA 10506227 → 55/1/0/0. GIM 10464103 → 107/5/1/2 (still contains “Not a PR reviewer”: leave it).

GSC (sc-domain:evex.sh, service account, no inspect): last complete day still **28/08** 1c/27i. 7d 22–28 **4c / 181i** (~26/giorno). Days 29–31 not in API yet. Inspect locked until Mon 1 Sep (tomorrow). Goal 300/giorno by 27/09; 3/09 gate is ≥40/giorno and inspect ≠ unknown on hub/GIM/DKA/Learn.

Sit dead. No Lennybot. Soft Eng/SEO not woken this slot (no new review comments; inspect is tomorrow). Play pending PMM (automation cannot SendToAgent): name the Monday shippable move toward 300 daily GSC impressions. Last lock still stands until they recut: Tommy merges #74; Typefully only after the page is 200; SEO dark until the 1 Sep inspect. Do not nag #588. Do not tweet OpenUI.


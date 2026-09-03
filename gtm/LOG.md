# evex — run log

Append-only, voce più recente in cima: **ogni run aggiunge la sua voce qui sotto**, dopo la riga dell'indice. Separato da STATE; **partizionato per settimana ISO il 30/08/2026** (ristrutturazione su modello skillsboard). Come STATE non è versionato in git (backup settimanale sul repo privato evex-gtm-backup, domenica 22:30). Mai riscrivere o troncare le voci esistenti.

**Convenzione di rollover (per i run):** questo file contiene solo le voci della settimana ISO corrente. Al primo run del lunedì, sposta le voci della settimana appena chiusa in `log/<anno>-W<settimana>.md` (header come i file esistenti) e aggiorna l'indice qui sotto. La fotografia dello stato vive in [STATE.md](STATE.md); qui solo cronaca dei run.

## Indice partizioni

- **Settimana corrente (2026-W36, 31 agosto – 6 settembre): le voci qui sotto.**
- [log/2026-W35.md](log/2026-W35.md) — 24-30 agosto: #74 support-reply-draft, gtm restructure, money-page path opens
- [log/2026-W34.md](log/2026-W34.md) — 17-23 agosto: Copy command #61, OSSDrop, Lennybot poi sit, #62–#65 GIM, override unsigned north star, sit weekend
- [log/2026-W33.md](log/2026-W33.md) — 10-16 agosto: setup GTM, lancio 11/08, audit SEO, directory, AI-SEO #58/#59, Q13 #60 chiusa senza merge

## Voci della settimana corrente (2026-W36)

## 2026-09-03 ~08:40 CEST (run 67, slot 08:20, morning, Thursday — gate day)

Delta since Wednesday morning (run 66; Mac gtm write surface unavailable this morning, so midday/evening 02/09 chronicles were not re-read from disk): TommyBez **merged #79** 02/09 10:03 UTC / **12:03 CEST** (featured Eve agent registry card on `/learn`). TommyBez **merged #80** 02/09 11:54 UTC / **13:54 CEST** (`/learn/install-eve-agent`, title Install an Eve agent · evex). **#75** eve 0.47.5 also MERGED 02/09 17:32 CEST (out of GTM scope). Open GTM PRs now **0**. Live site 200: `/`, `/agents`, support-reply-draft, `/learn`, `/learn/eve-agent-registry`, `/learn/install-eve-agent`, `/docs`, `/docs/publishing`, vs-agentcn. `/learn/publish-eve-agent` still **404**. Sitemap **36**. Stars **24**. #588 still OPEN — do not nag. Featured card for install-eve-agent is **not** on `/learn` index yet (only registry + vs-agentcn + LangGraph).

PostHog 244993 (project confirmed). 03/09 Europe/Rome so far **11 pv / 7 uniques / 7 sess**. Top pages: `/` 6/7, `/docs/publishing` 1, CR 1, brand-visual 1, leaderboard 1. Top refs: **$direct** 3u/6pv, **t.co** 2/3, github.com 1, api.daily.dev 1. 02/09 Rome **23/13/14**. 01/09 **44/17/18**. 31/08 **107/40/40**. Launch 11/08–03/09 08:40 **1135/535/614**.

North star **10 people / 13 copies** (Soft Eng 19/08 sticky test excluded; unchanged). Last copy still 30/08 13:02 CEST sticky `/agents/openui-assistant`. Score-only: do not tweet OpenUI.

**GSC gate 3/09 (sc-domain:evex.sh, service account, no inspect this slot):** final last complete day **31/08** 0c/50i. Final 7d 25–31 **2c / 205i (~29.3/giorno)**. All-state days: 31/08 50i, 01/09 **55i**, 02/09 **68i**. All-state 27/08–02/09 **279i (~39.9/giorno)**. Goal 300/giorno. **Gate ≥40 on complete final days: NOT met.** Provisional all-state including incomplete 1–2 Sep is **borderline ~40**. Inspect ≠ unknown half of the gate: already passed 1/09. New money URLs (eve-agent-registry, install-eve-agent) have **no GSC page rows yet**.

Typefully: get_me **200**, social set 266935. Post **2094825110788345928** → **41 impressions**, 0 likes/replies/retweets, 1 profile click, 0 link clicks (`[@]evex/support-reply-draft`).

Play this slot: Soft Eng / SEO / Search Counsel **not** woken. Automation cannot message Product Marketing directly. Standing PMM ownership stands: they name the next shippable move toward 300 after this gate score. Candidate to surface (not locked): feature `/learn/install-eve-agent` on the Learn index the same way #79 featured the registry card. Do not nag #588. Do not tweet OpenUI. Do not request indexing. Parent must (1) report Tommy in this CoS chat only in full sentences (no Slack), (2) FYI PMM with the gate score + delta and ask for today's play, (3) sync STATE/LOG/topics to Mac `gtm/` when that write surface is available (staging `/workspace/evex-gtm/pulse-run67/` + pushed to TommyBez/evex-gtm-backup).

## 2026-09-02 ~08:35 CEST (run 66, slot 08:20, morning, Wednesday)

Delta since Tuesday evening (run 65): TommyBez **merged #78** overnight (01/09 20:16 UTC / **22:16 CEST**, HEAD `1093990ed121cee5f25804795dcff66449e79cd2`). Live `/learn/eve-agent-registry` now **200** (title Eve agent registry · evex). Sitemap **35** (was 34). Site core still **200**. `/learn/publish-eve-agent` still **404** (#77 stays closed). Stars **24**. #588 still OPEN — do not nag. Open GTM PRs before Soft Eng wake: **0** (#75 eve upgrade remains out of scope).

PostHog 244993: 02/09 Europe/Rome so far **5/4/4**. 01/09 Rome **44/17/18**. Launch **1112/522/599**. North star **10/13**. GSC last complete **30/08** 0c/26i; 7d 23–29 ~26.3/giorno; gate 3/09 ≥40 not met yet. Soft Eng CloudAgent featured-card **in flight** (later became #79). Typefully support-reply-draft post **34** impressions morning.


# AI-SEO proposal (draft for Tommy) — evex

**From:** SEO  
**For:** Chief of Staff → morning pulse 13/08  
**Status:** draft only, no PR  
**Skills used:** `ai-seo`, `schema`; context from `.agents/product-marketing.md`, `gtm/STATE.md`, live `www.evex.sh` after #56/#57  
**Install command in all examples:** `npx shadcn@latest add @evex/<slug>` only

---

## Goal

Make evex easy for ChatGPT / Perplexity / Claude / Copilot to **cite correctly** (what it is, how to install, how to publish), without treating AI files as a Google ranking hack. Google AI Overviews still ride normal SEO + E-E-A-T; non-Google engines reward extractable structure + `llms.txt`.

## Current state (already strong)

Live check 12/08 evening (post-#57):

| Asset | Status |
|--------|--------|
| `/llms.txt` + `/llms-full.txt` | 200, text/plain, canonical install command |
| `.md` mirrors on agents/docs | 200, `X-Robots-Tag: noindex`, `rel=alternate` |
| `robots.txt` | `Allow: /`, `Content-Signal: search=yes, ai-input=yes, ai-train=yes`; AI bots not blocked |
| JSON-LD | Home: Organization, WebSite(+SearchAction), FAQPage, ItemList(+descriptions). Agents: SoftwareApplication (incl. codeRepository, downloadUrl, softwareRequirements, isAccessibleForFree, softwareHelp with shadcn command), FAQPage, BreadcrumbList. Docs: TechArticle + BreadcrumbList. Leaderboard: ItemList(+BreadcrumbList) from #57 |
| SSR HTML | Full content in first HTML (curl-visible); install command on agent pages |

Technical SEO PR track (#51/#56/#57) is closed. AI-SEO is **polish + citability content**, not greenfield.

## Gaps left after #57

1. **`llms.txt` agent blurbs** still pull raw registry `description` (markdown leftovers like backticks / `**`). Index should use the same cleaned SERP blurb as #56, plus an explicit install line per agent.
2. **No `HowTo` JSON-LD** on `/docs/installation` (and optionally publishing). Only TechArticle today. How-to queries are a natural citation path for "how to install an Eve agent".
3. **Agent/docs citability** is good but uneven: FAQ + file preview help; missing a short leading **definition block** (≈40–60 words, self-contained) on every agent and on docs intro. Learn has category guides; **no fair "evex vs agentcn / Eve agent registries" comparison** (comparison pages are ~⅓ of AI citations in the skill’s content mix).
4. **JSON-LD residual (low priority):** ItemList descriptions can truncate mid-sentence before the install CTA; Organization `sameAs` is GitHub + X only (fine). Skip OKF / pricing.md (OSS, free, no tiers). Do not chase FAQ rich results in Google (gov/health only); keep FAQPage for generative engines.
5. **Presence > more site markup:** Bing Webmaster (open Q9) feeds Copilot/ChatGPT search; directory/awesome submissions (Q11/Q12) and third-party mentions will move citations more than another schema field.

## Proposed scope (when Tommy says go — still no code tonight)

**PR-A — Machine-readable polish (S, Soft Eng)**  
- Clean agent lines in `llms.txt` / `llms-full.txt` generation (strip markdown; append `Install: npx shadcn@latest add @evex/<slug>`).  
- Add `HowTo` JSON-LD on `/docs/installation` (steps matching visible docs; same install command).  
- Optional: fix ItemList description truncation to sentence boundary.

**PR-B — Citability content (M, Content + SEO)**  
- Template: agent page lead definition (what it does / who for / install in one short block).  
- Docs intro: same pattern for "What is an Eve agent registry?".  
- One learn/comparison page: **Eve agent registries — evex vs agentcn** (table, fair, dated, no star-count brag; point at inspect-before-install + publish-via-PR). Highest leverage net-new page for AI answers.

**Ops (no PR)**  
- Monthly DIY AI visibility check (10 queries × ChatGPT / Perplexity / Google): e.g. "eve agent registry", "install eve agent shadcn", "evex vs agentcn", "how to publish eve agent", "@evex registry". Log in GTM.  
- Finish Bing verify (Q9) + directory P1 drafts (Q11) as citation/presence, not traffic.

**Out of scope for v1:** OKF bundle, paid AI-visibility tools, mass pSEO, separate "AI-only" content forks (Google spam risk), inventing community/install proof.

## Honest expectations

- Eve search volume is **tiny** (GSC ~25 impressions/day pre/early launch; north star still 0). AI-SEO will not move installs next week.  
- Classic SEO = **2–3 month** bet. AI citation is a **compound** bet: when someone asks an assistant about Eve agents, answers should name evex and the correct install command.  
- Near-term lever remains **community/social + supply** (and directory mentions). Treat this proposal as cheap correctness + one high-value comparison page.  
- Success signal: correct brand + command in AI answers on the query set above within ~60–90 days; not GSC click spikes.

## Ask for Tommy

1. Approve PR-A (llms clean + HowTo) as next Soft Eng SEO ticket?  
2. Approve PR-B comparison page (evex vs agentcn) as the single net-new content bet?  
3. Defer paid AI-monitoring tools for now (DIY monthly is enough at this volume)?


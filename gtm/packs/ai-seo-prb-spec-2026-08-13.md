# PR-B spec: definition blocks + evex vs agentcn (no PR yet)

**From:** SEO
**For:** Chief of Staff (route Soft Eng + Content after this)
**Date:** 2026-08-13
**Status:** outline + spec only. No code until CoS lands this.
**Skills:** `ai-seo` (definition + comparison table patterns), `schema`, `.agents/product-marketing.md`
**Install in every example:** `npx shadcn@latest add @evex/<slug>` only

---

## 1. Definition-block spec (Soft Eng slot + copy rules)

### Pattern (ai-seo)

Self-contained 40-60 word answer. What it is, who it is for, how to install. Works if an LLM lifts the paragraph alone. Lead with the answer. No em dashes. No star counts, no raw install totals, no "thriving community".

### Agent pages (`/agents/[slug]`)

**Today:** H1 `{name}` then `<AgentDescription>` (raw registry markdown) then author/files then the Install card. First paragraph is not a definition and often omits the install command.

**Slot:** new helper `getAgentDefinitionBlock(agent)` in `apps/web/lib/agent-detail.ts`. Render as a single `<p>` immediately under the H1 row (before the markdown description). Keep `AgentDescription` as the longer author blurb. Do not replace the Install card.

**Compose, do not add a new registry field in v1:**

1. Sentence 1: `{Name} is an Eve agent that {cleaned first sentence of description}`.
2. Sentence 2: who for (`Eve developers` or category: coding, marketing, data, …).
3. Sentence 3: `Preview every file on this page, then install with npx shadcn@latest add @evex/{slug}.`

If the result is over 60 words, drop sentence 2 to `It is for Eve developers.` If under 40, append one clause from `docs.overview[0]` when present. Strip markdown (backticks, `**`, links) using the same cleaner as the #56 SERP helper.

**Example (code-reviewer, illustrative, Content may tighten):**

> Code Reviewer is an Eve agent that reviews GitHub pull requests from a native GitHub App channel. It is for Eve developers who want inline review comments without wiring the App by hand. Preview every file on this page, then install with npx shadcn@latest add @evex/code-reviewer.

**Acceptance:** curl HTML contains the canonical command in that first body `<p>`; word count 40-60; no markdown leftovers; visible without JS.

Optional later: `meta.docs.seoLead` to override the helper. Not in this PR.

### Docs intro (`/docs`)

**Today:** `summary` already renders under the title (`docs-sections.tsx`). Current summary is ~28 words and does not name the install command. First H2 is "What evex is".

**No new component.** Copy-only in `apps/web/lib/docs-content.ts` (introduction):

1. Expand `summary` to 40-60 words answering **What is an Eve agent registry?** Include who (Eve developers) and `npx shadcn@latest add @evex/<slug>`.
2. Rename first section heading from `What evex is` to `What is an Eve agent registry?` Keep the existing three body paragraphs (they already match positioning). First paragraph of that section should still stand alone.

**Example summary (Content finalizes):**

> An Eve agent registry is a catalog of reusable Eve agents you can inspect and install as source files, instead of copying folders from GitHub. evex is that registry: browse community agents, preview every file, then add one with npx shadcn@latest add @evex/<slug>. After install you own the files. There is no hosted runtime.

---

## 2. Comparison page outline (Content draft, then Soft Eng PR)

**File:** add one object to `LEARN_PAGES` in `apps/web/lib/learn-content.ts` (same shape as `langgraph-vs-crewai`). Cluster `comparisons`. Existing related pages to link: `agent-registry`, `shadcn-registry-for-agents`. Also link `/docs`, `/docs/installation`, `/docs/publishing`.

| Field | Value |
|--------|--------|
| slug | `evex-vs-agentcn` (matches existing `*-vs-*` pattern; title still leads with the category query) |
| title | Eve agent registries: evex vs agentcn |
| shortTitle | evex vs agentcn |
| primaryKeyword | evex vs agentcn |
| relatedKeywords | eve agent registry, agentcn alternative, install eve agent, shadcn eve registry |
| cluster | comparisons |
| dates | published = modified = 2026-08-13 |

**Queries this page should be citable for:** "evex vs agentcn", "eve agent registry", "best eve agent registry", "install eve agent shadcn", "agentcn alternative".

### `summary` (the short version card = definition block)

40-60 words, dated in spirit, fair. Draft for Content to edit, not to invent facts:

> Eve agent registries let you install reusable Eve agents instead of copying folders. evex and agentcn both use the shadcn registry mechanic. evex is the full browse, inspect, install, and publish loop: file preview, author profiles, leaderboard, favorites, and publish via pull request. agentcn uses the same install path with a thinner catalog surface. Choose on inspectability and the publish path, not popularity.

### Sections (H2s)

1. **What an Eve agent registry is** — definition; not a gist list; not a hosted runtime. Point at inspect-before-install.
2. **Same install mechanic, different product** — fair: both shadcn. evex canonical command only. Do not dunk on agentcn. Do not cite star counts.
3. **Inspect before you install** — evex agent pages show files, deps, author, command. That is the trust surface.
4. **How agents get into the catalog** — evex: `registry/<slug>` + reviewed PR (`/docs/publishing`). Content must verify agentcn's live publish path before stating it; if unclear, say so rather than guess.
5. **When to pick which** — feeds the decision table. Copy-paste from GitHub as the third option (worse on repeatability).
6. **How to install from evex** — numbered steps. Only `npx shadcn@latest add @evex/<slug>`. Review files, set credentials, no runtime dependency on evex.

### Comparison table (Soft Eng: small type extension)

`decisionRows` is use/avoid, not feature-by-feature. Add optional `comparisonRows?: { criterion, left, right }[]` on `LearnPage`, render a real HTML `<table>` on the learn template (ai-seo: tables beat prose for vs queries). Columns: Criterion | evex | agentcn.

**Rows (no stars, no install totals as proof):**

| Criterion | evex | agentcn |
|-----------|------|---------|
| Install | `npx shadcn@latest add @evex/<slug>` | same shadcn mechanic (Content: confirm live command, do not invent) |
| Inspect files before install | Yes, on every agent page | Content: verify live |
| Author identity | GitHub-verified profiles | Content: verify live |
| Publish path | Reviewed pull request to the evex repo | Content: verify live; if docs are thin, say "thinner / not first-party publishing docs" only if still true |
| Catalog extras | Browse, search, leaderboard, favorites, publishing docs | Thinner surface (STATE 11/08; re-verify) |
| After install | You own the files; no runtime dependency on the registry | Same class of outcome if shadcn write-to-disk |
| Hosted agent runtime | No | No |
| Price | Free, MIT | Content: confirm license/price live |

**Bottom line (1-2 sentences after the table):** If you want inspect-before-install and a PR-owned catalog, use evex. If you already live in agentcn, the install mechanic is the same class of tool. Do not treat star count as quality.

### `decisionRows`

| choice | useWhen | avoidWhen |
|--------|---------|-----------|
| evex | You want file preview, GitHub-verified authors, and publish via PR | You are not on Eve |
| agentcn | You already use that catalog and only need the shadcn install path | You need inspect-before-install, author pages, leaderboard, or a documented PR publish path (only if live check still shows the gap) |
| Copy-paste from GitHub | One-off experiment | You need a repeatable `@evex/<slug>` (or equivalent) install |

### FAQs (keep FAQPage schema)

- What is the difference between evex and agentcn?
- How do I install an Eve agent from evex? (answer must include the canonical command)
- Is evex a marketplace? (No. Community registry, no commerce.)
- Can I publish my own agent on evex? (Yes, PR. Link `/docs/publishing`.)
- Does evex run the agent for me? (No.)

### Schema

Reuse existing learn JSON-LD: Article + FAQPage + BreadcrumbList. Do not add Review/AggregateRating. Do not chase Google FAQ rich results. The HTML table is the AI-extractable comparison.

### Copy constraints for Content

- Fair and dated. Re-check agentcn live before locking rows.
- No star-count brag (agentcn 405★ in STATE 11/08 is research-only, not page copy).
- No community overclaim (catalog still small / mostly mono-author).
- No raw DB install totals. No `eve add https://...`. No URL install as hero.
- No em dashes. Link evex.sh pages, not only the repo.
- Last updated visible via existing `dateModified`.

---

## 3. Split of work

| Who | What |
|-----|------|
| **Content** | Finalize docs intro summary + "What is an Eve agent registry?" heading copy. Draft the full `LearnPage` copy (summary, sections, FAQs, decisionRows, table cells) in a markdown file. Verify agentcn live. Do not open a PR. |
| **SEO** | This spec. Review Content's draft against extractability (40-60w leads, table, FAQs, command consistency). |
| **Soft Eng** | After copy is approved: (1) `getAgentDefinitionBlock` + agent page `<p>` slot; (2) optional `comparisonRows` + HTML table on learn template; (3) add the learn page object; (4) docs-content copy. Tests for helper word-count/command. No new registry schema field. |
| **Out of scope** | OKF, paid AI tools, per-agent `seoLead` field, HowTo (that is PR-A). |

## 4. Honest bar

This page will not create Eve demand. It exists so that when someone asks an assistant "evex vs agentcn" or "eve agent registry", the answer can name inspect-before-install, publish-via-PR, and the correct shadcn command.

---

## 5. Placement lock (2026-08-13, after Content copy pack)

Content draft: `gtm/ai-seo-pr-b-copy-2026-08-13.md`. Copy is approved with the nits below. Still no PR.

### Agent pages

**URL:** `/agents/[slug]` (existing).

**Insert** after the H1 row, **before** `<AgentDescription>` and before the Install card, so the definition is the first body copy:

1. `<h2>What is {name}?</h2>`
2. One `<p>` using Content’s template (45–60 words).
3. Canonical command as inline `<code>npx shadcn@latest add @evex/{slug}</code>` (not a second `InstallCommand` copy widget). North-star copy stays on the existing Install card.

Keep author/files meta and the markdown description. Soft Eng fills `{job}` / `{who}` from cleaned registry description + category (8–12 words each; total paragraph ≤60). No per-agent hand-copy required in v1. No new JSON-LD for this block (SoftwareApplication + FAQPage already on the page).

### Docs intro

**URL:** `/docs` (introduction). Copy-only in `docs-content.ts`.

- `summary` = Content’s 56-word “What is an Eve agent registry?” paragraph (renders under H1 today).
- Rename first section heading to `What is an Eve agent registry?`
- Do **not** paste the 56 words again as the first section body. Keep the existing three paragraphs as expansion.
- Schema: keep TechArticle + BreadcrumbList. Do **not** add FAQPage (no FAQ on this page).

### Comparison page

**URL:** `/learn/evex-vs-agentcn` (not docs, not the long slug). Cluster `comparisons`. Matches `langgraph-vs-crewai`. Title already carries the category query.

Map Content’s markdown onto `LearnPage`:

| LearnPage field | Content pack |
|-----------------|--------------|
| title | Eve agent registries: evex vs agentcn |
| description | Meta description (the 13 Aug 2026 line) |
| summary | The 56-word “What is an Eve agent registry?” paragraph (short-version card). Do not use the preamble as summary. |
| comparisonRows | The glance table (Soft Eng HTML `<table>`) |
| sections | Preamble as “Why this comparison”; What they share; Where they differ (inspect / publish / Eve-only vs multi-framework); How to install; Who should use which |
| decisionRows | evex / agentcn / copy-paste from GitHub |
| faqs | The four FAQs + add marketplace (“Is evex a marketplace?” → No) |
| examples | Two short ones (evex inspect-then-install; agentcn mixed-framework recipes) |
| dates | 2026-08-13 |

**Schema:** existing learn JSON-LD only: `Article` + `FAQPage` + `BreadcrumbList`. Author already in Article. HTML table is the vs extract. No Review/AggregateRating. No HowTo here (PR-A owns HowTo on `/docs/installation`).

### Copy nits still on Content (then Soft Eng can PR)

1. Cap `{job}`+`{who}` so the agent paragraph stays ≤60 words.
2. Add the marketplace FAQ.
3. Supply two `examples` lines and three `decisionRows` if not already implied (Who should use which + copy-paste as third choice).
4. Confirm agentcn install example `@agentcn/eve/deep-search` is still live (they stated it; keep the hedge on “live previews”).

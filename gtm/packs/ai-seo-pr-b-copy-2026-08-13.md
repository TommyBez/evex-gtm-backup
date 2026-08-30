# AI-SEO PR-B copy pack, mapped to SEO spec (2026-08-13)

**From:** Content
**File:** `gtm/ai-seo-pr-b-copy-2026-08-13.md`
**Status:** copy only. No PR. Mapped to `gtm/ai-seo-prb-spec-2026-08-13.md`.
**Install:** `npx shadcn@latest add @evex/<slug>` only. Never `eve add`. Never a URL install as hero.

This file is the Soft Eng paste source. Fields match `docs-content.ts` and `LearnPage` in `learn-content.ts` (same shape as `langgraph-vs-crewai`).

---

## Spec map

| Spec slot | Where it lands | Copy below |
|---|---|---|
| Agent definition: H2 `What is {name}?` + 45-60w `<p>` + inline `<code>` command | After H1, before markdown description and Install card. `getAgentDefinitionBlock`. No new registry field. Install card stays the CTA. | Section 1 |
| Docs intro | `DOCS_PAGES` introduction: expand `summary`; rename first H2. Keep existing three body paragraphs. | Section 2 |
| Comparison page | New `LEARN_PAGES` object, slug `evex-vs-agentcn`, cluster `comparisons`. Optional `comparisonRows` for the HTML table. | Section 3 |

---

## 1. Agent definition (`/agents/[slug]`)

Insert after the H1 row, **before** the markdown description and the Install card. First body copy. Install card stays the north-star CTA. No new registry field. Soft Eng fills `{job}` / `{who}` from cleaned registry description + category. Do not hand-write all 11 agents.

Markup:

1. `<h2>What is {name}?</h2>`
2. One `<p>` (45-60 words) with the canonical command as inline `<code>npx shadcn@latest add @evex/{slug}</code>` inside the paragraph. Not a second InstallCommand copy widget.

Compose the `<p>`:

1. `{Name} is an Eve agent that {job}.`
2. `It is for {who}.`
3. `Preview every file on this page, then install with <code>npx shadcn@latest add @evex/{slug}</code>.`

**Cap so the paragraph stays at most 60 words:**

- `{job}`: cleaned first sentence of the registry description, conjugated if needed. **Max 12 words.** Truncate at a word boundary.
- `{who}`: `Eve developers` or a short category clause (coding, marketing, data). **Max 8 words.**
- After compose, if total words > 60: set `{who}` to `Eve developers`. If still > 60: shorten `{job}` until the paragraph is ≤60.
- If total words < 45: append one clause from `docs.overview[0]` when present, then stop at 60.
- Strip markdown with the same cleaner as the #56 SERP helper. Visible without JS.

**Worked example** from live `registry/code-reviewer` (`{job}` 12 words, `{who}` 7 words, paragraph **46 words**, under the cap):

```
What is Code Reviewer?

Code Reviewer is an Eve agent that reviews GitHub pull requests from a native GitHub App channel. It is for Eve developers who want inline review comments. Preview every file on this page, then install with npx shadcn@latest add @evex/code-reviewer. After install you own the files.
```

`{job}` = `reviews GitHub pull requests from a native GitHub App channel` (12). `{who}` = `Eve developers who want inline review comments` (7). The longer "without wiring the App by hand" clause is dropped so job+who stay inside the cap. The last sentence is the under-45 overview append ("After install you own the files.").

---

## 2. Docs intro (`apps/web/lib/docs-content.ts`, slug `introduction`)

### `summary` (45 words)

Answers "What is an Eve agent registry?" Names who (Eve developers) and the canonical command.

```
An Eve agent registry is a catalog of reusable agents for Eve developers. You inspect files, then install them as source with npx shadcn@latest add @evex/<slug>, instead of copying folders. evex is that registry. After install you own the files. There is no hosted runtime.
```

### First section `heading`

Rename `What evex is` to:

```
What is an Eve agent registry?
```

Keep the existing three `body` paragraphs as expansion. Do not paste the summary again as section body. No FAQPage on docs (keep TechArticle + BreadcrumbList).

---

## 3. LearnPage `evex-vs-agentcn`

Same fields as `langgraph-vs-crewai`. Dates 2026-08-13. Related pages: `/learn/agent-registry`, `/learn/shadcn-registry-for-agents`. Also `/docs`, `/docs/installation`, `/docs/publishing`.

### Live agentcn column (checked 2026-08-13; reconfirmed later the same day)

Sources: https://www.agentcn.run/llms.txt, /docs, /docs/installation, /docs/agents/eve/deep-search, GitHub README.

- Install (live, reconfirmed): recipe page still shows `npx shadcn@latest add @agentcn/eve/deep-search` (also `@agentcn/<framework>/<recipe>`). Keep the hedge on live previews (docs claim them; we did not re-run a preview).
- Inspect: Composition file tree + Manual source + optional live preview on recipe docs. Not a catalog page with files + deps + GitHub-verified author + command.
- Author identity: not surfaced as GitHub-verified profiles.
- Publish: README says fork + PR. llms.txt has Introduction, Installation, Registry, MCP, Changelog, Agents. **No first-party publishing docs.**
- Catalog extras: agent list + changelog. No leaderboard, favorites, or author pages in the public docs index.
- After install: installation docs say you own the copied files.
- Hosted runtime: no.
- Price: GitHub lists MIT. No paid tier on agentcn.run.
- No star counts. No install totals.

### Front matter

- `slug`: `evex-vs-agentcn`
- `title`: Eve agent registries: evex vs agentcn
- `shortTitle`: evex vs agentcn
- `description`: Fair, dated comparison of evex and agentcn as Eve agent registries. Both use the shadcn CLI. evex adds inspect-before-install and publish via pull request.
- `cluster`: `comparisons`
- `datePublished` / `dateModified`: `2026-08-13`
- `primaryKeyword`: evex vs agentcn
- `relatedKeywords`: eve agent registry, agentcn alternative, install eve agent, shadcn eve registry

### `summary` (55 words)

The short-version card. Must name both products (vs query). Docs `summary` stays the registry-only definition.

```
Eve agent registries let Eve developers install reusable agents as source files instead of copying folders. evex and agentcn both use the shadcn CLI. evex is the browse, inspect, install, and publish loop: file preview on every agent page, GitHub-verified authors, and publish via pull request. Choose on inspectability and the publish path, not popularity.
```

### `sections` (six H2s, spec order)

**1. heading:** `What an Eve agent registry is`

body[0] (47 words):

```
An Eve agent registry is a catalog of reusable agents for Eve developers. You browse an agent, inspect the files it will write into agent/, then install it with a shadcn command. It is not an awesome-list of GitHub links. It is not a hosted agent runtime.
```

body[1]: The job is distribution. Framework docs help you start an Eve project. A registry helps the next person install a known-good agent without copying a folder by hand.

body[2]: evex is one Eve agent registry. Inspect files on the agent page first. Then install with `npx shadcn@latest add @evex/<slug>`. After install you own the files. See [/docs](/docs) and [/learn/agent-registry](/learn/agent-registry).

**2. heading:** `Same install mechanic, different product`

body[0] (50 words):

```
evex and agentcn both install agents with the shadcn CLI. That is the shared mechanic, not proof they are the same product. evex is Eve-native and built around browse, inspect, install, and publish. agentcn is a multi-framework recipe registry (Eve, Flue, Mastra, LangGraph) with the same class of CLI install.
```

body[1]: On evex the canonical command is always `npx shadcn@latest add @evex/<slug>`. On agentcn, recipe pages (checked 13 Aug 2026) show `npx shadcn@latest add @agentcn/eve/deep-search`, and the same pattern with `@agentcn/<framework>/<recipe>`.

body[2]: Do not treat star counts as quality. Pick the loop you need: inspect-before-install and a documented PR publish path, or a recipe catalog that already spans more than Eve. See [/learn/shadcn-registry-for-agents](/learn/shadcn-registry-for-agents).

**3. heading:** `Inspect before you install`

body[0] (40 words):

```
On evex, every agent page shows the files, dependencies, GitHub-verified author, and the install command. That is the trust surface. You see what lands under agent/ in the repo before you run the CLI. Inspect those files first, then install.
```

body[1]: agentcn recipe docs (example: [Deep Search](https://www.agentcn.run/docs/agents/eve/deep-search)) show a Composition file tree, a Manual source tab, and an optional live preview (needs an API key). Files show on the recipe page. That is not an inspect-files UI on the catalog listing, and it does not surface GitHub-verified author identity and dependencies the same way as an evex agent page.

body[2]: If the question is "show me the files, the author, and the exact command before I install," that is the evex agent page.

**4. heading:** `How agents get into the catalog`

body[0] (40 words):

```
On evex, agents live under registry/<slug> in the public repo and enter the catalog through a reviewed pull request. The first-party path is /docs/publishing. Authors get a registry page and GitHub-tied identity. The catalog is code-owned, not an upload form.
```

body[1]: On agentcn, as of 13 August 2026, the GitHub README asks you to fork shadcn-labs/agentcn and open a pull request. The public docs index (llms.txt) lists Introduction, Installation, Registry, MCP, Changelog, and Agents. There is no first-party publishing guide on agentcn.run comparable to evex `/docs/publishing`.

body[2]: Both can take a GitHub PR. evex documents that path as part of the product. agentcn's live site documents install, registry config, and recipes, not a publish loop.

**5. heading:** `When to pick which`

body[0] (48 words):

```
Pick evex if you are on Eve and want to inspect files, then install, then publish through a reviewed PR. Pick agentcn if you already use that catalog or you need recipes across Eve, Flue, Mastra, or LangGraph. Copy-paste from GitHub is a third option, worse for repeatability.
```

body[1]: Copy-paste from GitHub is the third option. It works once. It fails at repeatability: no stable `@evex/<slug>` (or equivalent) command, easy to miss dependencies, nothing for the next teammate to browse.

body[2]: Using both is normal. They are not the same product with different logos. See the decision table below.

**6. heading:** `How to install from evex`

body[0]: Install from evex in an Eve project. Preview files first. Then run the canonical shadcn command.

bullets (numbered in the template, or body lines if the learn renderer has no ordered list):

1. Open an agent page on [evex.sh](https://evex.sh) and read the files it will write.
2. From your Eve project, run `npx shadcn@latest add @evex/<slug>`.
3. Review the generated files. Set any credentials the agent needs (see [/docs/installation](/docs/installation)).
4. The agent runs from your repo. There is no runtime dependency on evex.

Closing line: Never `eve add`. Never a URL install as the command you publish or paste into docs.

### `comparisonRows` (Soft Eng: optional field, HTML `<table>`)

Columns: Criterion | evex | agentcn. Left = evex, right = agentcn.

| criterion | left | right |
|---|---|---|
| Install | `npx shadcn@latest add @evex/<slug>` | Same shadcn CLI. Live Eve example (13 Aug 2026): `npx shadcn@latest add @agentcn/eve/deep-search` |
| Inspect files before install | Yes. Files, dependencies, author, and command on every agent page. | Recipe docs: Composition file tree, Manual source, optional live preview (needs an API key). Not an inspect-files UI on the catalog listing. |
| Author identity | GitHub-verified author profiles | Not surfaced as GitHub-verified author profiles on recipe pages (checked 13 Aug 2026) |
| Publish path | Reviewed pull request. First-party docs: [/docs/publishing](/docs/publishing) | GitHub README: fork and open a PR. No first-party publishing docs on agentcn.run as of 13 Aug 2026 |
| Catalog extras | Browse, search, leaderboard, favorites, publishing docs | Docs agent list and changelog. No leaderboard, favorites, or author pages in the public docs index |
| After install | You own the files. No runtime dependency on evex. | You own the copied files (stated on their installation docs). Same class of write-to-disk outcome. |
| Hosted agent runtime | No | No |
| Price | Free, MIT | Free. GitHub lists MIT. No paid tier on agentcn.run (checked 13 Aug 2026) |

**Bottom line after the table:** If you want inspect-before-install and a PR-owned catalog, use evex. If you already live in agentcn, the install mechanic is the same class of tool. Do not treat star count as quality.

### `decisionRows`

| choice | useWhen | avoidWhen |
|---|---|---|
| evex | You want file preview, GitHub-verified authors, and publish via PR on an Eve app. | You are not on Eve. |
| agentcn | You already use that catalog, or you need shadcn-installed recipes across Eve, Flue, Mastra, or LangGraph. | You need inspect-before-install, author pages, a leaderboard, or a documented first-party PR publish path. |
| Copy-paste from GitHub | A one-off experiment where you will own the copy yourself. | You need a repeatable `npx shadcn@latest add @evex/<slug>` (or equivalent) install. |

### `examples` (exactly two)

| label | body |
|---|---|
| evex inspect-then-install | Preview files on an agent page, then run `npx shadcn@latest add @evex/code-reviewer`. Review what landed under `agent/`. |
| agentcn mixed-framework | Same shadcn CLI across Eve, Flue, Mastra, and LangGraph. Live Eve example (reconfirmed 13 Aug 2026): `npx shadcn@latest add @agentcn/eve/deep-search`. |

### `faqs` (Article + FAQPage + BreadcrumbList only. No Review/AggregateRating. No HowTo.)

**What is the difference between evex and agentcn?**
Both are shadcn-compatible agent registries, not hosted runtimes. evex is Eve-native: inspect files on every agent page, GitHub-verified authors, and publish via reviewed pull request. agentcn uses the same CLI mechanic for recipes across Eve, Flue, Mastra, and LangGraph. Choose on inspectability and the publish path.

**How do I install an Eve agent from evex?**
From an Eve project, run `npx shadcn@latest add @evex/<slug>`. Example: `npx shadcn@latest add @evex/code-reviewer`. Preview the files on the agent page first, then follow [/docs/installation](/docs/installation).

**Is evex a marketplace?**
No. It is a community registry. There is no commerce.

**Can I publish my own agent on evex?**
Yes. Open a pull request that adds the agent under `registry/<slug>`. Follow [/docs/publishing](/docs/publishing).

**Does evex run the agent for me?**
No. After install the agent runs from files in your project. There is no runtime dependency on evex.

---

## Checklist (nits 2026-08-13)

- [x] Agent: H2 `What is {name}?` + 45-60w `<p>` + inline `<code>` command. `{job}` max 12 words, `{who}` max 8, paragraph ≤60
- [x] Docs `summary` under H1; first H2 renamed; existing three paragraphs kept; no FAQPage on docs
- [x] Learn `summary` = registry definition (not the preamble). URL `/learn/evex-vs-agentcn`
- [x] Marketplace FAQ present
- [x] Two `examples` (evex inspect-then-install; agentcn mixed-framework)
- [x] Three `decisionRows` (evex / agentcn / copy-paste from GitHub)
- [x] `@agentcn/eve/deep-search` reconfirmed live 2026-08-13
- [x] No em dashes, no star counts, no install totals, no community-size brag

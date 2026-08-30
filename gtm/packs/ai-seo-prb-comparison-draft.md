# PR-B copy draft (Content): docs intro + evex vs agentcn

**Status:** copy only. No PR. Three nits applied 2026-08-13. Soft Eng paste source. Hold is Tommy sign-off.
**Date:** 2026-08-13
**For:** SEO extractability pass, then Soft Eng (`docs-content.ts`, `learn-content.ts`)
**Skills:** ai-seo, copywriting, copy-editing, `.agents/product-marketing.md`, `gtm/ai-seo-prb-spec-2026-08-13.md`

Install in every evex example: `npx shadcn@latest add @evex/<slug>` only. Never `eve add`. Never a URL install as hero.

---

## Live verification (agentcn, 2026-08-13)

Checked https://www.agentcn.run/llms.txt, /docs, /docs/installation, /docs/agents/eve/deep-search, and the GitHub README.

| Claim | Live finding | Use on page |
|---|---|---|
| Install command | Recipe pages show `npx shadcn@latest add @agentcn/eve/deep-search` (also `@agentcn/<framework>/<recipe>` for Flue, Mastra, LangGraph) | Quote their command in the table only. Do not invent. |
| Inspect files | Recipe docs show a Composition file tree plus a Manual source tab. Optional live preview on the docs site. Not the same as evex agent pages (files, deps, GitHub-verified author, command on one catalog page). | Fair: they show composition + source. evex is the catalog inspect loop. |
| Author identity | No GitHub-verified author profiles on recipe pages or in llms.txt | Say they are not surfaced. Do not invent. |
| Publish path | README: fork + open a pull request. llms.txt docs: Introduction, Installation, Registry, MCP, Changelog, Agents. **No `/docs/publishing` or equivalent.** | "GitHub PR to shadcn-labs/agentcn. No first-party publishing docs on agentcn.run as of 2026-08-13." |
| Catalog extras | Agents list + changelog. No leaderboard, favorites, or author pages in the public docs index. | Thinner catalog surface. Still true. |
| After install | Installation docs: "The installed files are plain source. You own them." | Same class of outcome (write-to-disk). |
| Hosted runtime | No. Live preview is on their docs site, not a runtime for your app. | No / No |
| Price / license | GitHub repo license field: MIT. No paid tier on agentcn.run. | Free, MIT. |

No star counts. No catalog-size or install totals in copy.

Related learn pages to link: `/learn/agent-registry`, `/learn/shadcn-registry-for-agents`. Also `/docs`, `/docs/installation`, `/docs/publishing`.

---

## 1. Docs intro (`apps/web/lib/docs-content.ts`, introduction)

### `summary` (40-60 words)

**Word count: 45**

```
An Eve agent registry is a catalog of reusable agents for Eve developers. You inspect files, then install them as source with npx shadcn@latest add @evex/<slug>, instead of copying folders. evex is that registry. After install you own the files. There is no hosted runtime.
```

### First section heading

Rename `What evex is` → `What is an Eve agent registry?`

Keep the existing three body paragraphs. First paragraph already stands alone.

---

## 2. Learn page object (`LEARN_PAGES` in `apps/web/lib/learn-content.ts`)

Soft Eng: add optional `comparisonRows?: { criterion: string; left: string; right: string }[]` and render an HTML `<table>`. Until that lands, the table below is the cell copy.

```ts
{
  slug: 'evex-vs-agentcn',
  title: 'Eve agent registries: evex vs agentcn',
  shortTitle: 'evex vs agentcn',
  description:
    'Fair, dated comparison of evex and agentcn as Eve agent registries. Both use the shadcn CLI. evex adds inspect-before-install and publish via pull request.',
  cluster: 'comparisons',
  datePublished: '2026-08-13',
  dateModified: '2026-08-13',
  primaryKeyword: 'evex vs agentcn',
  relatedKeywords: [
    'eve agent registry',
    'agentcn alternative',
    'install eve agent',
    'shadcn eve registry',
  ],
```

### `summary` (definition block, 54 words)

```
Eve agent registries let Eve developers install reusable agents as source files instead of copying folders. evex and agentcn both use the shadcn CLI. evex is the browse, inspect, install, and publish loop: file preview on every agent page, GitHub-verified authors, and publish via pull request. Choose on inspectability and the publish path, not popularity.
```

### `sections`

#### H2: What an Eve agent registry is

**Lead (48 words):** An Eve agent registry is a catalog of reusable agents for Eve developers. You browse an agent, inspect the files it will write into `agent/`, then install it with a shadcn command. It is not an awesome-list of GitHub links. It is not a hosted agent runtime.

Body 2: The job is distribution. Framework docs help you start an Eve project. A registry helps the next person install a known-good agent without copying a folder by hand.

Body 3: evex is one Eve agent registry. Inspect files on the agent page first. Then install with `npx shadcn@latest add @evex/<slug>`. After install you own the files. See [/docs](/docs) and [/learn/agent-registry](/learn/agent-registry).

#### H2: Same install mechanic, different product

**Lead (52 words):** evex and agentcn both install agents with the shadcn CLI. That is the shared mechanic, not proof they are the same product. evex is Eve-native and built around browse, inspect, install, and publish. agentcn is a multi-framework recipe registry (Eve, Flue, Mastra, LangGraph) with the same class of CLI install.

Body 2: On evex the canonical command is always `npx shadcn@latest add @evex/<slug>`. On agentcn, recipe pages (checked 13 Aug 2026) show `npx shadcn@latest add @agentcn/eve/deep-search`, and the same pattern with `@agentcn/<framework>/<recipe>`.

Body 3: Do not treat star counts as quality. Pick the loop you need: inspect-before-install and a documented PR publish path, or a recipe catalog that already spans more than Eve. See [/learn/shadcn-registry-for-agents](/learn/shadcn-registry-for-agents).

#### H2: Inspect before you install

**Lead (51 words):** On evex, every agent page shows the files, dependencies, GitHub-verified author, and the install command. That is the trust surface. You see what lands in the repo before you run the CLI.

Body 2: agentcn recipe docs (example: [Deep Search](https://www.agentcn.run/docs/agents/eve/deep-search)) show a Composition file tree, a Manual source tab, and an optional live preview on the docs site. That is useful. It is still docs-page composition, not a catalog page that also surfaces author identity and dependencies the same way.

Body 3: If the question is “show me the files, the author, and the exact command before I install,” that is the evex agent page.

#### H2: How agents get into the catalog

**Lead (55 words):** On evex, agents live under `registry/<slug>` in the public repo and enter the catalog through a reviewed pull request. The first-party path is [/docs/publishing](/docs/publishing). Authors get a registry page and GitHub-tied identity.

Body 2: On agentcn, as of 13 August 2026, the GitHub README asks you to fork shadcn-labs/agentcn and open a pull request. The public docs index (llms.txt) lists Introduction, Installation, Registry, MCP, Changelog, and Agents. There is no first-party publishing guide on agentcn.run comparable to evex `/docs/publishing`.

Body 3: Both can take a GitHub PR. evex documents that path as part of the product. agentcn’s live site documents install, registry config, and recipes, not a publish loop.

#### H2: When to pick which

**Lead (44 words):** Pick evex if you are on Eve and want to inspect files, then install, then publish through a reviewed PR. Pick agentcn if you already use that catalog or you need recipes across Eve, Flue, Mastra, or LangGraph.

Body 2: Copy-paste from GitHub is the third option. It works once. It fails at repeatability: no stable `@evex/<slug>` (or equivalent) command, easy to miss dependencies, nothing for the next teammate to browse.

Body 3: Using both is normal. They are not the same product with different logos. See the decision table below.

#### H2: How to install from evex

**Lead (22 words, then steps):** Install from evex in an Eve project. Preview files first. Then run the canonical shadcn command.

1. Open an agent page on [evex.sh](https://evex.sh) and read the files it will write.
2. From your Eve project, run `npx shadcn@latest add @evex/<slug>`.
3. Review the generated files. Set any credentials the agent needs (see [/docs/installation](/docs/installation)).
4. The agent runs from your repo. There is no runtime dependency on evex.

Never `eve add`. Never a URL install as the command you publish or paste into docs.

### `comparisonRows` (Criterion | evex | agentcn)

Render as HTML `<table>`. Left = evex. Right = agentcn.

| criterion | left (evex) | right (agentcn) |
|---|---|---|
| Install | `npx shadcn@latest add @evex/<slug>` | Same shadcn CLI. Live Eve example (13 Aug 2026): `npx shadcn@latest add @agentcn/eve/deep-search` |
| Inspect files before install | Yes. Files, dependencies, author, and command on every agent page. | Recipe docs: Composition file tree + Manual source on the recipe page; optional live preview (needs an API key). Not a catalog listing with files + deps + GitHub-verified author |
| Author identity | GitHub-verified author profiles | Not surfaced as GitHub-verified author profiles on recipe pages (checked 13 Aug 2026) |
| Publish path | Reviewed pull request. First-party docs: [/docs/publishing](/docs/publishing) | GitHub README: fork and open a PR. No first-party publishing docs on agentcn.run as of 13 Aug 2026 |
| Catalog extras | Browse, search, leaderboard, favorites, publishing docs | Docs agent list and changelog. No leaderboard, favorites, or author pages in the public docs index |
| After install | You own the files. No runtime dependency on evex. | You own the copied files (stated on their installation docs). Same class of write-to-disk outcome. |
| Hosted agent runtime | No | No |
| Price | Free, MIT | Free. GitHub lists MIT. No paid tier on agentcn.run (checked 13 Aug 2026) |

**Bottom line (after the table):** If you want inspect-before-install and a PR-owned catalog, use evex. If you already live in agentcn, the install mechanic is the same class of tool. Do not treat star count as quality.

### `decisionRows`

| choice | useWhen | avoidWhen |
|---|---|---|
| evex | You want file preview, GitHub-verified authors, and publish via PR on an Eve app. | You are not on Eve. |
| agentcn | You already use that catalog, or you need shadcn-installed recipes across Eve, Flue, Mastra, or LangGraph. | You need inspect-before-install, author pages, a leaderboard, or a documented first-party PR publish path. |
| Copy-paste from GitHub | A one-off experiment where you will own the copy yourself. | You need a repeatable `npx shadcn@latest add @evex/<slug>` (or equivalent) install. |

### `examples`

- **Eve on evex:** Preview files on an agent page, then run `npx shadcn@latest add @evex/code-reviewer`. Review what landed under `agent/`. Publish your own later via [/docs/publishing](/docs/publishing).
- **Eve on agentcn:** From an Eve project, their docs show `npx shadcn@latest add @agentcn/eve/deep-search`. You own the copied recipe files.
- **Outside a registry:** Cloning a random GitHub `agent/` folder still works once. It is not a registry install.

### `faqs`

**What is the difference between evex and agentcn?**
Both are shadcn-compatible agent registries, not hosted runtimes. evex is Eve-native: inspect files on every agent page, GitHub-verified authors, and publish via reviewed pull request. agentcn uses the same CLI mechanic for recipes across Eve, Flue, Mastra, and LangGraph. Choose on inspectability and the publish path.

**How do I install an Eve agent from evex?**
From an Eve project, run `npx shadcn@latest add @evex/<slug>`. Example: `npx shadcn@latest add @evex/code-reviewer`. Preview the files on the agent page first, then follow [/docs/installation](/docs/installation).

**Is evex a marketplace?**
No. evex is a community registry. There is no commerce.

**Can I publish my own agent on evex?**
Yes. Open a pull request that adds the agent under `registry/<slug>`. Follow [/docs/publishing](/docs/publishing).

**Does evex run the agent for me?**
No. After install the agent runs from files in your project. There is no runtime dependency on evex.

---

## 3. Agent-page definition (Soft Eng helper)

Not a new registry field. One `<p>` under the H1, before the markdown description and the Install card. **No extra H2.** Canonical command as inline `<code>` inside that same paragraph, not a second copy widget. `{job}` max 12 words, `{who}` max 8, paragraph ≤60.

Tightened example (code-reviewer, 46 words):

```
Code Reviewer is an Eve agent that reviews GitHub pull requests from a native GitHub App channel. It is for Eve developers who want inline review comments without wiring the App by hand. Preview every file on this page, then install with `npx shadcn@latest add @evex/code-reviewer`.
```

If sentence 1 plus "It is for Eve developers." plus the install sentence is still over 60 words, drop clause 2 to that short form.

---

## Copy constraints checklist

- [x] Canonical install only for evex examples
- [x] No em dashes
- [x] No star counts, no install totals, no community-size brag
- [x] Fair, dated (2026-08-13), agentcn publish path verified not guessed
- [x] Links to `/docs/publishing` and `/docs/installation`
- [x] Learn shape: summary, sections, decisionRows, examples, faqs, plus comparisonRows for Soft Eng

# PR-B mapped copy (sign-off) — 2026-08-13

**From:** SEO  
**Status:** mapped onto LearnPage / docs / agent slots. No PR. Soft Eng blocked until Tommy/CoS signs.  
**Source copy:** `gtm/ai-seo-pr-b-copy-2026-08-13.md` (Content)  
**Placement:** `gtm/ai-seo-prb-spec-2026-08-13.md` §5  
**Install:** `npx shadcn@latest add @evex/<slug>` only  
**HowTo JSON-LD:** PR-A, not this file

---

## Live verify (agentcn, 13 Aug 2026)

| Claim | Result | Evidence |
|-------|--------|----------|
| Site https://www.agentcn.run | TRUE | 200. H1: "Production-ready agents, made simple." |
| shadcn CLI `@agentcn/<framework>/<recipe>` | TRUE | Home + install docs. Eve / Flue / Mastra / LangGraph examples. |
| `npx shadcn@latest add @agentcn/eve/deep-search` | TRUE | On home, `/docs/installation`, and `/docs/agents/eve/deep-search` (200). |
| Live previews | TRUE, different product | README: "Live previews — Run each agent right from its docs page." Install docs: optional, needs `ANTHROPIC_API_KEY`. Not a file tree on a registry listing. |
| Repo https://github.com/shadcn-labs/agentcn | TRUE | MIT. Generic "submit a PR" in README. No `/docs/publishing` (404). |
| Multi-framework Eve, Flue, Mastra, LangGraph/Dawn | TRUE | Home + install: "Eve, Flue, Mastra, or LangGraph (Dawn)". |
| Official shadcn index `@agentcn` | TRUE | `ui.shadcn.com/r/registries.json` name `@agentcn` (homepage there still `agentcn.vercel.app`; live site is agentcn.run). |
| You own files / not a hosted runtime | TRUE | Docs: "copy-paste recipes you can own, with zero lock-in." |
| Leaderboard / favorites / inspect-files UI | ABSENT | Do not claim they have evex's catalog loop. |
| Star counts | Research only | Do not put on the page. |

Paste source (CoS 13/08). Inspect row keeps recipe-page Composition file tree. Agent slot: H2 `What is {name}?` + one `<p>` with inline command (Content sign-off). Marketplace FAQ has no “licensing”. Learn summary names both products.

---

## A. Agent pages — `/agents/[slug]`

**Slot:** after H1, before markdown description and Install card. First body copy.

1. `<h2>What is {name}?</h2>`
2. One `<p>` (45–60 words) with the command as inline `<code>` inside that paragraph. Not a second copy widget.

Compose: `{Name} is an Eve agent that {job}. It is for {who}. Preview every file on this page, then install with npx shadcn@latest add @evex/{slug}.`
`{job}` max 12 words, `{who}` max 8. If over 60 words, drop `{who}` to `Eve developers`. Soft Eng fills from registry fields. No new JSON-LD.

**Example (code-reviewer, 46 words):**

```
What is Code Reviewer?

Code Reviewer is an Eve agent that reviews GitHub pull requests from a native GitHub App channel. It is for Eve developers who want inline review comments. Preview every file on this page, then install with npx shadcn@latest add @evex/code-reviewer. After install you own the files.
```

---

## B. Docs intro — `/docs`

Copy-only in `apps/web/lib/docs-content.ts` (introduction).

**`summary` (under H1):**

An Eve agent registry is a catalog of reusable agents for Vercel's Eve framework. You browse agents, inspect the files they will write into your project, then install them with one shadcn command. evex is an open registry of that kind: agents are code-owned, published by pull request, and added with `npx shadcn@latest add @evex/<slug>`.

**First section heading:** `What is an Eve agent registry?`  
**First section body:** keep the existing three paragraphs. Do not paste the summary again.  
**Schema:** TechArticle + BreadcrumbList only. No FAQPage.

---

## C. Learn page — `/learn/evex-vs-agentcn`

Not `/learn/eve-agent-registries-evex-vs-agentcn`. Not docs.

### LearnPage fields

- slug: `evex-vs-agentcn`
- cluster: `comparisons`
- title: `Eve agent registries: evex vs agentcn`
- shortTitle: `evex vs agentcn`
- description: `Compare evex and agentcn as Eve agent registries. Both install with the shadcn CLI. evex adds inspect-before-install and publish-via-PR. Updated 13 Aug 2026.`
- datePublished: `2026-08-13`
- dateModified: `2026-08-13`
- primaryKeyword: `evex vs agentcn`
- relatedKeywords: `eve agent registry`, `agentcn alternative`, `install eve agent`, `shadcn eve registry`
- summary (55 words, names both products): Eve agent registries let Eve developers install reusable agents as source files instead of copying folders. evex and agentcn both use the shadcn CLI. evex is the browse, inspect, install, and publish loop: file preview on every agent page, GitHub-verified authors, and publish via pull request. Choose on inspectability and the publish path, not popularity.

### comparisonRows (HTML `<table>`, Soft Eng slot)

| criterion | left (evex) | right (agentcn) |
|-----------|-------------|-----------------|
| What it is | Open registry for Eve agents | Open registry of agent recipes (Eve, Flue, Mastra, LangGraph/Dawn) |
| Site | https://evex.sh | https://www.agentcn.run |
| Install mechanic | shadcn CLI, `@evex/<slug>` | shadcn CLI, `@agentcn/<framework>/<recipe>` |
| Eve install example | `npx shadcn@latest add @evex/<slug>` | `npx shadcn@latest add @agentcn/eve/deep-search` |
| Inspect before install | Files, dependencies, author, and command on every agent page | Recipe docs: Composition file tree + Manual source on the recipe page; optional live preview (needs an API key). Not a catalog listing with files + deps + GitHub-verified author |
| Publish path | Reviewed pull request. Agents live in `registry/`. Docs: https://evex.sh/docs/publishing | Source-owned recipes in https://github.com/shadcn-labs/agentcn. README invites a GitHub PR. No first-party publishing docs |
| After install | You own the files. No runtime dependency on evex | You own the copied recipe files. Zero lock-in (their docs) |
| Scope | Eve-native | Multi-framework |
| Official shadcn index | `@evex` | `@agentcn` |
| Best for | Eve apps where you want to audit files, then install, then publish via PR | Teams that want the same shadcn mechanic across more than one agent framework |

**Bottom line (last paragraph of the table section):** Pick evex if you are on Eve and care about inspect-before-install plus a publish-via-PR catalog. Pick agentcn if you need recipes across Eve, Flue, Mastra, or LangGraph, not Eve only.

### sections

**Why this comparison**  
evex and agentcn are both shadcn-compatible registries for installing AI agents into your project. This page compares them as Eve agent registries: what they share, where the product loops differ, and which fit to pick. No star counts. Catalog size is still early on both sides, so this is about the loop, not a popularity score.

**What they share**  
Both treat agents as shadcn registry items, not hosted runtimes. You copy files into the project with `npx shadcn@latest add …`, then you own those files. Neither is a paid marketplace. Both are MIT / open source.  
If someone asks "is there a shadcn registry for Eve agents?", the honest answer is yes, more than one. evex and agentcn are the two with a full install path, not just an awesome-list.

**Inspect before install**  
evex puts the files, dependencies, GitHub-verified author, and the exact install command on every agent page. The point is trust before `npx`. You see what lands under `agent/` before you run the CLI.  
agentcn ships complete recipes through the same CLI and documents them on https://www.agentcn.run. Recipe pages show a Composition file tree, a Manual source tab, and an optional live preview (API key). That is docs-page composition, not a catalog page with files, dependencies, and a GitHub-verified author. If your question is "show me the files on the registry page," that is the evex loop.

**Publish via pull request**  
evex agents live in https://github.com/TommyBez/evex under `registry/`. New agents and updates enter the catalog through a reviewed pull request. Publishing docs: https://evex.sh/docs/publishing.  
agentcn recipes live in https://github.com/shadcn-labs/agentcn. Same idea of source-owned recipes, with a generic GitHub PR invite in their README. The evex product surface around that path is the public catalog loop: author profiles, favorites, leaderboard, and first-party publishing docs.

**Eve-only vs multi-framework**  
This is the clean split. evex is Eve-native. agentcn targets Eve plus Flue, Mastra, and LangGraph (Dawn). If you are not on Eve, evex is the wrong tool. If you are only on Eve and want the inspect → install → own → publish loop, evex is the tighter fit.

**How to install an evex agent**  
1. Open an agent page on https://evex.sh and read the files it will write.  
2. From an Eve project, run `npx shadcn@latest add @evex/<slug>`.  
3. Review the generated files and set any credentials the agent needs.  
4. The agent runs from your repo. evex is not in the runtime.  
Never use a URL install form, and never `eve add`. The canonical command is always `npx shadcn@latest add @evex/<slug>`.

**Who should use which**  
Use evex when you already have (or are starting) an Eve app, you want to inspect files before install, and you may publish an agent through a PR.  
Use agentcn when you want shadcn-installed recipes and your stack is mixed (Eve plus Flue, Mastra, or LangGraph), or you already work from the agentcn catalog.  
Using both is normal. They are not the same product with different logos.

### decisionRows

| choice | useWhen | avoidWhen |
|--------|---------|-----------|
| evex | You are on Eve and want file preview, GitHub-verified authors, and publish via PR | You are not using Eve |
| agentcn | You want the same shadcn mechanic across Eve, Flue, Mastra, or LangGraph, or you already use that catalog | You need inspect-before-install on the registry page and first-party publishing docs |
| Copy-paste from GitHub | A one-off experiment | You need a repeatable `npx shadcn@latest add @evex/<slug>` (or `@agentcn/…`) install |

### examples

| label | body |
|-------|------|
| evex | Open https://evex.sh/agents/code-reviewer, inspect the files, then run `npx shadcn@latest add @evex/code-reviewer`. |
| agentcn | From an Eve, Flue, Mastra, or LangGraph (Dawn) app, run `npx shadcn@latest add @agentcn/eve/deep-search` (or the matching framework path). |

### faqs

**What is the difference between evex and agentcn?**  
Both are shadcn-compatible agent registries. evex is Eve-native, with inspect-before-install on each agent page and a publish-via-PR catalog. agentcn is a multi-framework recipe registry (Eve, Flue, Mastra, LangGraph) using the same CLI mechanic.

**How do I install an Eve agent from evex?**  
Run `npx shadcn@latest add @evex/<slug>` in an Eve project. Example: `npx shadcn@latest add @evex/code-reviewer`. Inspect the files on the agent page first.

**Is evex a hosted agent platform?**  
No. evex is a registry. After install you own the files. There is no runtime dependency on evex.

**Is evex a marketplace?**  
No. It is a community registry. There is no commerce.

**Can I publish my own Eve agent on evex?**  
Yes. Open a pull request that adds the agent under `registry/<slug>`. Follow https://evex.sh/docs/publishing.

### Schema

Existing learn JSON-LD only: Article + FAQPage + BreadcrumbList. No HowTo (PR-A). No Review.

### Related

Link `agent-registry`, `shadcn-registry-for-agents`, `/docs`, `/docs/installation`, `/docs/publishing`.

---

## Sign-off ask

Tommy / CoS: approve this mapped copy as the PR-B source. Soft Eng implements slots in spec §5 from this file. Content can still tighten wording after sign-off; facts in the agentcn column are live-verified as of 13 Aug 2026.

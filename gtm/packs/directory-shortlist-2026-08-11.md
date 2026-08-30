# evex: directory and list submission shortlist

Date: 2026-08-11 (install-command correction 2026-08-14; P4-O/P4-P 2026-08-14; P1-B #588 2026-08-14; P1-C #2 MERGIATA 2026-08-15)
Scope: where to submit **evex the registry** (not individual agents). Research and drafts; P4-O AllShadcn FREE Starter submitted 14/08; P4-P caramaschiHG/awesome-ai-agents-2026 PR #502 opened 14/08; P1-B awesome-shadcn-ui PR #588 opened 14/08; P1-C doanbactam/awesome-eve nit follow-up PR #2 MERGIATA 15/08.

**Correction 2026-08-14:** every draft below now uses the canonical install command `npx shadcn@latest add @evex/<slug>`. The 11/08 drafts had `eve add https://www.evex.sh/r/<slug>.json`; that form is obsolete and must not appear in marketing copy, OG cards, or submissions.

---

## 1. Sommario

**The two candidates that looked like the obvious wins are already done.** evex is already listed in the official shadcn open source registry index (`@evex` in `https://ui.shadcn.com/r/registries.json`, with logo), and consequently already appears on registry.directory at `https://registry.directory/TommyBez/evex`. BlockDex also already indexes it organically at `https://blockdex.kynth.studio/registries/evex`. So the shadcn registry distribution layer is covered.

**The highest-value action left is not a submission at all.** BlockDex says verbatim on the evex page: *"This registry publishes no description of itself. Everything below was read from its own manifest."* That is because `https://evex.sh/r/registry.json` has `name` and `homepage` but no top level `description`. Every downstream index that reads the manifest (BlockDex today, others later) shows a blank where the pitch should be. Adding one field fixes the card everywhere, with no submission, no review, no waiting. That is item P1-A below.

**What is genuinely open:**
- `awesome-shadcn-ui` (birobirobiro) has a `Registries` section and does **not** list evex. Clean PR, clear contribution rules, strongest generic backlink available for this product.
- Three community "awesome eve" lists now exist. One of them (`doanbactam/awesome-eve`) has a Showcase section that literally says *"Your project here, open a pull request!"*. Zero friction, exactly on topic.
- `shadcn.io/awesome/registries` (commercial mirror of the awesome list, 30 registries, no evex) accepts submissions but behind a sign in.
- The official shadcn index entry for evex carries a description written before the current positioning. Worth a one line refresh PR.

**What is not worth it, honestly.** Generalist AI tool directories are a bad fit and mostly paid. There's An AI For That charges a **$347** one off submission fee. Toolify is free but with a 2 to 4 week queue, or **$99** to skip it. Both audiences are consumer AI tool browsers looking for a hosted product to click; evex is an shadcn registry with no hosted product to try. Expect near zero qualified traffic. Skip or defer to last.

**Realistic volume expectation.** evex is a niche developer product inside a framework that launched in June 2026. The entire addressable population is Eve users plus shadcn registry watchers. No list on this shortlist will send hundreds of visits a month. What these submissions actually buy: (a) presence in the corpus that LLMs read when someone asks "how do I install an Eve agent", (b) 3 to 5 dofollow backlinks from repos and sites with real crawl frequency, (c) being in the same table as agentcn, which is currently the better known competitor in this exact slot.

**Competitive note worth flagging.** evex is not alone anymore. `shadcn-labs/agentcn` (405 stars) is a shadcn registry of Eve agent recipes with the same install mechanic, `elie222/atom-eve` (44 stars) calls itself "Agent registry for Eve and Flue", `nolly-studio/eve-directory` (8 stars) calls itself "The open registry for Eve agents", and `bergside/awesome-eve-agents` (22 stars) fronts eveagents.dev with its own CLI. Two of the three "awesome eve" lists are effectively owned by competitors and currently list only their own agents. That affects both priority and expected acceptance rate below.

---

## 2. Shortlist prioritizzata

| # | Candidate | URL | What it lists | Submission mechanism | Requirements | Effort | Expected value | Priority |
|---|---|---|---|---|---|---|---|---|
| A | evex own `registry.json` description | https://evex.sh/r/registry.json | Source manifest read by every shadcn index | Self serve, commit to own repo | Valid registry schema | 10 min | Fixes the blank description on BlockDex and any future manifest reader. Highest leverage per minute on this list. | **P1** |
| B | awesome-shadcn-ui | https://github.com/birobirobiro/awesome-shadcn-ui | shadcn registries, libs, tools. Has a dedicated `Registries` section | PR to `README.md`, or the form at awesomeshadcn.dev which opens the PR for you | Free to use, about shadcn, working link, one sentence description, one resource per PR, no date cell | 20 min | Biggest generic backlink available here, high crawl frequency, mirrored by shadcn.io. evex is not listed. | **P1** PR opened |
| C | doanbactam/awesome-eve | https://github.com/doanbactam/awesome-eve | Eve ecosystem resources. Has an explicit `Showcase` section inviting PRs | PR to `README.md` | sindresorhus awesome contributing guidelines, one link per line | 15 min | Small list (3 stars) but it is the canonical `awesome-eve` name and the only Eve list not run by a competitor. Currently the Showcase has exactly one entry: agentcn. | **P1** MERGIATA |
| D | shadcn.io Component Registries | https://www.shadcn.io/awesome/registries | 30 shadcn registries, commercial mirror of the awesome list | Form at https://www.shadcn.io/awesome/submit, redirects to sign in | Account required | 15 min, owner must do it | Decent indexed surface, own pages per item, feeds "best shadcn registries" queries. Commercial site (Azencot LLC) with a Pro upsell, so treat the free listing as the whole prize. | **P2** |
| E | shadcn-ui/ui registry index description refresh | https://github.com/shadcn-ui/ui/blob/main/apps/v4/registry/directory.json | The official shadcn open source registry index | PR to shadcn-ui/ui, run `pnpm validate:registries` | Registry must stay open source, flat, schema valid, `files` without `content` | 20 min | evex is already in. This only updates the one line description that propagates to the CLI and to registry.directory. Small but the highest authority surface evex sits on. | **P2** |
| F | shadcn-labs/awesome-eve-agents | https://github.com/shadcn-labs/awesome-eve-agents | Individual Eve agents by category | PR, see `CONTRIBUTING.md` | Production ready Eve agent | 30 min for 3 to 4 entries | Agent level, not registry level. Run by the agentcn authors and every current entry points at agentcn docs. Real chance of a slow or declined review. Submit 3 strong agents, not all 11. | **P2** |
| G | vercel/eve GitHub Discussions, Show and tell | https://github.com/vercel/eve/discussions | Official Eve community surface | Post a discussion | GitHub account | 30 min | Not a directory, but it is the only official Eve community channel. The eve.dev `/resources` route permanently redirects to `/templates`, and `/templates` is Vercel curated with no public submission path. Discussions is the only door. | **P2** |
| H | bergside/awesome-eve-agents | https://github.com/bergside/awesome-eve-agents | Bergside's own 21 agents, fronting eveagents.dev | Open an issue (their stated process) | Reusable Eve agent | 15 min | Competitor catalog with its own CLI (`npx @bergside/eveagents install`). The only realistic slot is their `Related Projects` section. Low odds, low cost. | **P3** |
| I | Vercel Templates marketplace | https://vercel.com/templates/submit | Deployable Vercel templates | Form (confirmed live, HTTP 200) | Must be a deployable template repo | High | evex is a registry, not a deployable template. Only becomes relevant if you package an "Eve agent starter wired to @evex" template. Do not submit the registry itself. | **P3** |
| J | OpenAlternative | https://openalternative.co/submit | Open source alternatives to proprietary software | Form accepted, finalize paid only | Must be an alternative to a named proprietary product | 20 min | SKIP 2026-08-14: form accepted but finalize is paid ($97+), not paid. Draft remains. | **Skip** |
| K | e2b-dev/awesome-ai-agents | https://github.com/e2b-dev/awesome-ai-agents | AI agents and assistants, 29k stars | PR or Google Form | Must be an agent | 20 min | 29k stars is tempting, but the README states plainly: *"This list is only for AI assistants and agents."* evex is a registry. A registry level entry is off spec and likely rejected. Individual agents could technically qualify but the entry format is a long per project block. | **P3** |
| L | Toolify | https://www.toolify.ai | Consumer AI tools | Form. Free with a 2 to 4 week queue, or about $99 to be listed in 48h | Screenshots, video, long description | 30 min | Wrong audience. No hosted product to try. Free tier only, never pay. | **P3** |
| M | There's An AI For That | https://theresanaiforthat.com/get-featured/ | Consumer AI tools | Paid form | **$347 one off submission fee** | n/a | Do not submit. Paid, consumer audience, no product to click. | **Skip** |
| N | aitools.fyi and similar long tail AI directories | various | Consumer AI tools | Mostly forms, many paid | varies | varies | Same problem as L and M, with worse domain quality. Skip. | **Skip** |
| O | AllShadcn | https://allshadcn.com | shadcn tools / registries | Tally form https://tally.so/r/3XybbL | Cover 1600x900, free starter | 15 min | FREE Starter submitted 14/08. Listed within a couple of weeks. Paid Express $12 / Premium $49 / Elite $99 not used. | **P4** submitted |
| P | caramaschiHG/awesome-ai-agents-2026 | https://github.com/caramaschiHG/awesome-ai-agents-2026 | AI agents 2026 list | PR | GitHub PR | 15 min | PR #502 opened by Tommy 14/08 (Add evex to Agent Templates). | **P4** PR opened |

### Already done, no submission needed

| Surface | Status | Note |
|---|---|---|
| Official shadcn registry index | **Listed** as `@evex` with logo in `apps/v4/registry/directory.json` and served at https://ui.shadcn.com/r/registries.json | Only the description needs a refresh. See P2-E. |
| registry.directory | **Listed** at https://registry.directory/TommyBez/evex, shown as "21 stars, 11 items, updated 1mo ago" | Derives from the official index plus GitHub. No separate claim or edit route exists (`/add`, `/submit`, `/new` all return 404). Refreshing the official index description is what changes this card. |
| BlockDex | **Indexed** at https://blockdex.kynth.studio/registries/evex, all 11 items, all free, "Free, manifest served live" | No submission form. It reads the manifest nightly. The card is currently missing the registry description because the manifest has none. Fix via P1-A. |

---

## 3. Shared asset block

Reused across the drafts below. Per the playbook rule, the opening sentence and emphasis are varied per target so the same paragraph is not duplicated across surfaces.

- **Name:** evex
- **Namespace:** `@evex`
- **Canonical URL:** https://evex.sh
- **Repo:** https://github.com/TommyBez/evex
- **Docs:** https://evex.sh/docs
- **Publishing guide:** https://evex.sh/docs/publishing
- **Leaderboard:** https://evex.sh/leaderboard
- **Registry endpoint:** https://evex.sh/r/registry.json
- **Machine readable:** https://evex.sh/llms.txt
- **Install command (always this exact form):** `npx shadcn@latest add @evex/<slug>`
- **License and price:** open source, free
- **Catalog at time of writing:** 11 agents, 1 author, 1685 installs, 21 GitHub stars
- **Categories in use:** coding, marketing, data, research, productivity, general, support, devops
- **Tags:** eve, vercel eve, ai agents, agent registry, shadcn registry, open source, developer tools
- **Tagline (under 10 words):** Open registry for Eve agents, install with one command
- **Short description (about 60 chars):** Community registry of Eve agents, one command to install
- **Author contact:** GitHub @TommyBez, X @TommyBez85

**Copy constraints applied to every draft below:** English only, no em dash and no en dash, install command written only as `npx shadcn@latest add @evex/<slug>`, every description links to https://evex.sh or the repo.

---

## 4. Draft submissions

### P1-A. evex `registry.json`: add the top level description

**Type:** self serve change in your own repo. Not a submission.
**Why first:** BlockDex prints *"This registry publishes no description of itself"* on your page right now. The shadcn registry schema supports a top level `description`, your manifest does not set one. Every manifest reader that gets built after today will hit the same gap.

**Current manifest head:**

```json
{
  "$schema": "https://ui.shadcn.com/schema/registry.json",
  "name": "evex",
  "homepage": "https://evex.sh",
  "items": [ ... ]
}
```

**Proposed manifest head:**

```json
{
  "$schema": "https://ui.shadcn.com/schema/registry.json",
  "name": "evex",
  "homepage": "https://evex.sh",
  "description": "The open registry for agents built on eve, Vercel's agent framework. Browse every file before you install, add any agent with `npx shadcn@latest add @evex/<slug>`, and publish your own by pull request. Every agent is code owned and reviewed. Free and open source.",
  "items": [ ... ]
}
```

Find the generator source rather than editing the built artifact. In this repo the manifest is produced by `pnpm --filter @evex/agent-registry generate`, so the `description` belongs in whatever the generator reads, and the generated `registry.json` should be regenerated and committed.

**Secondary, optional:** BlockDex classifies all 11 items as kind "Other" because every item uses `"type": "registry:item"`. That is correct for agents and there is no better shadcn type today, so no action, but it explains the label if you wondered.

**Optional follow up, not required:** a short note to hello@kynth.studio letting them know the manifest now carries a description and asking whether they want anything else surfaced. Draft:

> Subject: evex registry now publishes a description in its manifest
>
> Hi, evex (https://evex.sh) is indexed on BlockDex at https://blockdex.kynth.studio/registries/evex. The page correctly noted that the registry published no description of itself. That is fixed: https://evex.sh/r/registry.json now carries a top level description. If there is any other field your crawler reads that we could populate, tell me and I will add it. evex is an open registry of agents for Eve, Vercel's agent framework, installed with npx shadcn@latest add @evex/<slug>. Repo: https://github.com/TommyBez/evex. Thanks for indexing it.

---

### P1-B. awesome-shadcn-ui, `Registries` section

**Target:** https://github.com/birobirobiro/awesome-shadcn-ui
**Status:** PR opened by Tommy 14/08 ~10:12 CEST. **PR #588 OPEN** — https://github.com/birobirobiro/awesome-shadcn-ui/pull/588 (Libs and Components, not Registries). Body has the same `<slug>` strip (`@evex/` empty).
**File:** `README.md`
**Section:** `## Registries`
**Mechanism:** either the form at https://awesomeshadcn.dev (recommended by their CONTRIBUTING, it opens the PR for you and rejects duplicates) or a direct PR using their PR template.
**Rules that matter:** one resource per PR, three columns only, **do not write the Date cell and do not leave a trailing `|  |`** (a workflow fills it on merge), description must be one concrete sentence in English, must be free to use, must be genuinely about shadcn.

**Placement:** the `Registries` table is alphabetical. `evex` goes between `efferd` and `interlace-ui`.

**Exact row to insert:**

```markdown
| evex | Open registry of installable agents for eve, Vercel's agent framework. Add any agent to an eve app with `npx shadcn@latest add @evex/<slug>`, preview every file first, and publish your own by pull request. | [Link](https://evex.sh) |
```

**Exact patch:**

```diff
 | efferd | ready-to-use shadcn blocks that just work — modern, responsive, and built for speed. | [Link](http://efferd.com/) | 2026-03-05T23:46:18.000Z |
+| evex | Open registry of installable agents for eve, Vercel's agent framework. Add any agent to an eve app with `npx shadcn@latest add @evex/<slug>`, preview every file first, and publish your own by pull request. | [Link](https://evex.sh) |
 | interlace-ui | Design-system registry for the Interlace docs sites: theme baseline, layout and accessibility primitives, and MDX components. Installable with the shadcn CLI. | [Link](https://ds.interlace.tools) | 2026-08-11T14:21:17.397Z |
```

**PR title:** `Add evex to Registries`

**PR body:**

> Adds evex to the Registries section.
>
> evex is an open source shadcn-compatible registry that distributes agents for eve, Vercel's agent framework. It serves a schema valid flat registry at https://evex.sh/r/registry.json and each agent installs with `npx shadcn@latest add @evex/<slug>`. It is also in the official shadcn open source registry index under the `@evex` namespace for protocol compatibility.
>
> - Site: https://evex.sh
> - Source: https://github.com/TommyBez/evex
> - Registry: https://evex.sh/r/registry.json
>
> Free and open source, no paid tier. Row inserted alphabetically between `efferd` and `interlace-ui`, with no Date cell per CONTRIBUTING.

---

### P1-C. doanbactam/awesome-eve, `Showcase` section

**Target:** https://github.com/doanbactam/awesome-eve
**Status:** Listing mergiata 14/08. Nit `<slug>` stripato; follow-up **PR #2 MERGIATA 15/08 ~03:40 CEST** da doanbactam — https://github.com/doanbactam/awesome-eve/pull/2 (Fix evex install command slug).
**File:** `README.md`
**Section:** `## Showcase` (its current content is one entry, agentcn, plus the placeholder line `_Your project here, open a pull request!_`)
**Mechanism:** PR.
**Rules:** sindresorhus awesome contributing guidelines, one link per line with a short description.

**Style conflict to decide, flagged not silently resolved.** This repo's house style separates the link from the description with an em dash. Your copy rules forbid em dashes. The line below uses a colon instead. It reads fine and stays consistent within the entry, but it will visually differ from its neighbours. Your call: keep the colon, or accept the repo's em dash for this one line only.

**Exact line to insert (colon version, respects your rule):**

```markdown
- [evex](https://evex.sh): The open registry for eve agents. Install any community agent with `npx shadcn@latest add @evex/<slug>`, preview every file before it lands, and publish your own by pull request.
```

**Exact patch:**

```diff
 ## Showcase
 
 Agents and projects built with eve. Open a PR to add yours.
 
 - [Agentcn](https://github.com/shadcn-labs/agentcn) — shadcn/ui, but for building agents. 🤖
+- [evex](https://evex.sh): The open registry for eve agents. Install any community agent with `npx shadcn@latest add @evex/<slug>`, preview every file before it lands, and publish your own by pull request.
 - _Your project here — open a pull request!_
```

**Optional second line, same PR or a follow up.** The `Official` section lists ecosystem entry points. A registry arguably belongs there too, but `Official` is reserved for Vercel owned links, so do not push it. Showcase is the correct home.

**PR title:** `Showcase: add evex, the open registry for eve agents`

**PR body:**

> Adds evex to the Showcase section.
>
> evex is an open source registry of agents for eve. Any eve app can add one with `npx shadcn@latest add @evex/<slug>`. Publishing is a pull request: each agent ships its own evals, a README, an `.env.example`, and a CODEOWNERS entry, and a human reviews it before merge.
>
> - Site: https://evex.sh
> - Source: https://github.com/TommyBez/evex
> - Publishing guide: https://evex.sh/docs/publishing
>
> 11 agents at time of writing, free and open source. Happy to reword the entry to match house style if you prefer.

---

### P2-D. shadcn.io, Component Registries

**Target:** https://www.shadcn.io/awesome/registries (30 resources, evex not listed)
**Mechanism:** form at https://www.shadcn.io/awesome/submit. It redirects to a sign in, so **this one needs the owner to do it manually**. No account was created.
**Note:** commercial site run by Azencot LLC, with a Pro plan and an affiliate program. The free listing is the whole value. Do not buy anything.

**Field by field draft:**

- **Name:** evex
- **Website:** https://evex.sh
- **Repository:** https://github.com/TommyBez/evex
- **Category:** Component Registries
- **Tagline:** The open registry for eve agents
- **Short description (60 chars):** Open registry of eve agents, installed with `npx shadcn@latest add @evex/<slug>`
- **Long description (about 140 words):**

> evex is a shadcn-compatible registry that distributes agents instead of UI components. Each item is a complete agent for eve, Vercel's open source agent framework: instructions, typed tools, an eval suite, a README, and an `.env.example`. You add one to an eve app with `npx shadcn@latest add @evex/<slug>`, and the CLI writes real source files into your project that you own and can edit. Nothing is hidden behind a runtime.
>
> The catalog is public at https://evex.sh, and every file is previewable on the agent page before you install. Publishing works the same way the rest of the ecosystem does: open a pull request, pass schema validation and the eval suite, and get reviewed by a human. Every agent has a CODEOWNERS entry, so someone is accountable for it after merge. Free and open source: https://github.com/TommyBez/evex

- **Tags:** shadcn registry, ai agents, eve, vercel, agent registry, open source, developer tools
- **Install command to display:** `npx shadcn@latest add @evex/code-reviewer`
- **Pricing:** Free
- **Open source:** Yes

---

### P2-E. shadcn-ui/ui, refresh the `@evex` index description

**Target:** https://github.com/shadcn-ui/ui
**File:** `apps/v4/registry/directory.json`
**Status:** evex is **already listed**. This is an edit, not an addition.

**Current entry:**

```json
{
  "name": "@evex",
  "homepage": "https://evex.sh",
  "url": "https://evex.sh/r/{name}.json",
  "description": "Installable AI agent recipes for Eve apps, including PR review, data analysis, and workflow automation agents.",
  "logo": "<svg ...>"
}
```

**Proposed description (keep `name`, `homepage`, `url` and `logo` exactly as they are, change only the one string):**

```json
"description": "Open registry of community agents for eve, Vercel's agent framework. Preview every file, install with `npx shadcn@latest add @evex/<slug>`, and publish your own by pull request."
```

**Why change it:** the current line reads as a vendor catalog ("agent recipes for Eve apps") and buries the two things that differentiate evex from agentcn and the other Eve catalogs: it is community publishable, and you see the source before it lands. This string is what registry clients and registry.directory render, so it is worth the 20 minutes.

**Before opening the PR, per their docs:** run `pnpm validate:registries`. Confirm the requirements still hold: registry open source and publicly accessible, valid against the registry schema, flat with `/registry.json` and `/{name}.json` at the root, and no `content` property inside `files`. All four currently hold for evex.

**PR title:** `chore(registry): update @evex description`

**PR body:**

> Updates the one line description for the `@evex` entry in the open source registry index. No change to `name`, `homepage`, `url` or `logo`.
>
> The previous wording described evex as a set of agent recipes. It is a community registry: anyone can publish an agent by pull request, every agent is code owned and reviewed, and every file is previewable before install. The new string says that.
>
> Registry: https://evex.sh/r/registry.json
> Site: https://evex.sh
> Source: https://github.com/TommyBez/evex
>
> `pnpm validate:registries` passes.

---

### P2-F. shadcn-labs/awesome-eve-agents, individual agent entries

**Target:** https://github.com/shadcn-labs/awesome-eve-agents
**Mechanism:** PR, see their `CONTRIBUTING.md`.
**Read the room first.** This list is maintained by shadcn-labs, the authors of agentcn, and every single one of its ~19 entries currently links to `agentcn.vercel.app`. Submitting the whole evex catalog will read as a takeover. Submit **three** agents that fill categories agentcn covers thinly or not at all, and be explicit in the PR body that you are the author. If it is declined, that is information, not a loss.

**Same em dash conflict as P1-C.** House style is `- **[Name](url)** — Description`. Colon versions below; decide whether to match house style for these lines.

**Three lines, placed alphabetically inside their existing sections:**

`## Data & Databases` (agentcn has one text to SQL agent, evex has two production Slack analysts):

```markdown
- **[Postgres Data Analyst](https://evex.sh/agents/postgres-data-analyst)**: Slack native analyst for a single Postgres database. Answers mentions and DMs, inspects schema metadata, and runs bounded read only SQL through authored tools. Install with `npx shadcn@latest add @evex/postgres-data-analyst`.
- **[Supabase Data Analyst](https://evex.sh/agents/supabase-data-analyst)**: Slack native analyst for a single Supabase project, restricted to read only SQL. Exposes only `supabase__list_tables` and `supabase__execute_sql` over the hosted Supabase MCP server. Install with `npx shadcn@latest add @evex/supabase-data-analyst`.
```

`## Developer Tools` (agentcn has one PR review agent that returns feedback, evex has one that publishes an actual GitHub review):

```markdown
- **[Code Reviewer](https://evex.sh/agents/code-reviewer)**: Reviews pull requests from a native GitHub App channel. Mention `@code-reviewer` on a PR and it publishes a GitHub review with inline comments, optional suggestion blocks, and Upstash backed rate limiting for public repos. Install with `npx shadcn@latest add @evex/code-reviewer`.
```

**PR title:** `Add three agents from the evex registry`

**PR body:**

> Adds three agents from evex (https://evex.sh), an open registry of eve agents. Disclosure: I am the author of these agents and of the registry.
>
> - Postgres Data Analyst and Supabase Data Analyst under Data & Databases: both are Slack native and read only by construction, which is a different shape from a text to SQL agent.
> - Code Reviewer under Developer Tools: it publishes a real GitHub review with inline comments through a native GitHub App channel, rather than returning review text to the caller.
>
> Each ships with an eval suite, a README written for the person running it, and an `.env.example` covering every variable the code reads. Install is `npx shadcn@latest add @evex/<slug>`.
>
> Source: https://github.com/TommyBez/evex. Happy to trim this to one entry, reword to match house style, or drop it entirely if the list is meant to stay agentcn only.

---

### P2-G. vercel/eve GitHub Discussions, Show and tell

**Target:** https://github.com/vercel/eve/discussions
**Mechanism:** post a discussion. Not a directory, but it is the only official Eve community surface that accepts community input.
**Checked and ruled out:** `eve.dev/resources` is a `permanentRedirect` to `/templates` (see `apps/docs/app/[lang]/resources/page.tsx` in vercel/eve), and `eve.dev/templates` is a Vercel curated gallery of nine `vercel-labs` templates with no public submission path. There is no community resources page in the vercel/eve repo to PR into. The README points at Discussions and nothing else.

**Draft post:**

> **Title:** evex: an open registry for eve agents, installable with the shadcn CLI
>
> **Category:** Show and tell
>
> I have been building evex (https://evex.sh), an open registry for agents built on eve.
>
> The install path is the shadcn CLI. Adding an agent to an eve app is `npx shadcn@latest add @evex/code-reviewer`, and the CLI writes the agent source into your project: instructions, typed tools, config. You own the files afterwards and can edit them like anything else in the repo. The agent page shows every file before you install, so nothing arrives unseen.
>
> Publishing is a pull request against https://github.com/TommyBez/evex. An agent has to ship an eval suite, a README written for whoever runs it, and an `.env.example` that covers every environment variable the code reads. A generator validates the manifest against a schema and checks that the declared file list matches disk, that dependencies are in sync, and that every agent pins the same eve version. Each merged agent gets a CODEOWNERS entry, so it has an owner after merge rather than becoming unmaintained catalog filler.
>
> There are 11 agents in the catalog today, all mine, which is the part I would most like to change. Categories so far: code review, data analysis over Postgres and Supabase from Slack, Linear operations, scheduled X and email digests, generative UI, brand and SEO asset generation, and an agent that builds other eve agents.
>
> The publishing guide is at https://evex.sh/docs/publishing. Feedback on the packaging contract is welcome, especially from anyone who has tried to share an eve agent and found the current options awkward.


### P3-J. OpenAlternative, AI Agent Platforms

**Target:** https://openalternative.co/submit
**Status:** SKIP 2026-08-14 (paid finalize). Form filled and submitted; landed on paid packages only (Standard $97+). Not paid. Draft remains.
**Category page:** https://openalternative.co/categories/ai-agent-platforms
**Mechanism:** form at https://openalternative.co/submit (sign-in required). Finalize is paid only; no free queue.

**Pairing notes:**
- Lindy is already a named OpenAlternative target: https://openalternative.co/alternatives/lindy (typed as AI personal assistant; only Inbox Zero listed). Lindy the product also sells Slack / Linear / GitHub hosted agents.
- Relevance AI is NOT a named OA target. If the form rejects a custom name, use Lindy only.
- CodeRabbit pairing rejected: https://openalternative.co/alternatives/coderabbit already has Continue, Kodus, Pullfrog, Roomote. A registry with one reviewer loses.

**Install command in this draft:** `npx shadcn@latest add @evex/{slug}` (curly braces, not `<slug>`). GitHub markdown ate `<slug>` on the awesome-eve listing. On the OA web form either form is fine; keep `{slug}` for safety.

**Field by field draft:**

- **Name:** evex
- **Website:** https://evex.sh
- **Repo:** https://github.com/TommyBez/evex
- **Tagline:** Open registry of Eve agents you install with the shadcn CLI
- **Alternative to:** Lindy, Relevance AI (if the form accepts a custom name)
- **Category:** AI Agent Platforms

**Description** (plain English, no em dash, no eve add):

> evex is an open registry for Eve agents. Preview every file before it lands, install any agent with `npx shadcn@latest add @evex/{slug}`, and publish your own by pull request.
>
> Lindy and Relevance AI sell hosted agents that automate Slack, Linear, and GitHub behind a subscription. evex covers the same jobs as source you own: a code reviewer, a Linear ops agent, Slack-native Postgres and Supabase analysts, X drafts, and more. You run them in your Eve app.


### P4-O. AllShadcn, FREE Starter

**Target:** https://allshadcn.com
**Form:** https://tally.so/r/3XybbL
**Status:** SUBMITTED 2026-08-14 ~13:00 CEST (FREE Starter). Paid plans (Express $12 / Premium $49 / Elite $99) not used.
**Confirmation:** listed on allshadcn.com within a couple of weeks. Contact hello@themeselection.com.

**Fields submitted:**

- **Email:** tommaso.carnemolla@gmail.com
- **Category:** Tool
- **Name:** evex
- **URL:** https://evex.sh
- **Demo URL:** https://evex.sh
- **Description:** evex is an open registry for Eve agents. Preview every file before it lands, install any agent with `npx shadcn@latest add @evex/{slug}`, and publish your own by pull request.
- **Cover image:** required; generated 1600x900 cover uploaded.

---

### P4-P. caramaschiHG/awesome-ai-agents-2026, Agent Templates

**Target:** https://github.com/caramaschiHG/awesome-ai-agents-2026
**Status:** PR opened by Tommy 14/08. **PR #502** — https://github.com/caramaschiHG/awesome-ai-agents-2026/pull/502
**Title:** Add evex to Agent Templates
**Compare:** https://github.com/caramaschiHG/awesome-ai-agents-2026/compare/main...TommyBez:awesome-ai-agents-2026:add-evex?expand=1
**Author / branch:** TommyBez / `add-evex`

---

## 5. Notes and open questions

**Candidates that do not exist or turned out paid**

- **There's An AI For That:** exists, but submission costs **$347** one off. Consumer AI tool audience. Do not submit.
- **Toolify:** exists, free tier real but with a 2 to 4 week queue, **$99** to skip the queue. Paid does not improve organic rank on their own ranking. If you ever submit, submit free.
- **registry.directory `/add`, `/submit`, `/new`:** all return 404. The homepage shows an "Add your Registry" card, but there is no public self serve route. In practice the site is populated from the official shadcn index plus GitHub metadata, which is why evex already appears without ever having submitted.
- **awesomeshadcn.dev `/submit` and `/submit-resource`:** both 404. The submission form is reachable from the site UI, not from a guessable path. The CONTRIBUTING.md PR route works regardless and is what the drafts above use.
- **eve.dev `/resources`:** effectively gone, it is a permanent redirect to `/templates`. Any older reference to an Eve "community resources" page is stale.
- **e2b-dev/awesome-ai-agents CONTRIBUTING.md:** 404. Submission instructions live inline in the README (PR or a Google Form), and the README explicitly scopes the list to agents and assistants, not registries.

**Decisions the owner needs to make**

1. Em dash policy inside third party repos whose house style uses one (P1-C, P2-F). The drafts use colons and flag the divergence rather than quietly breaking either your rule or their style.
2. Whether to approach `shadcn-labs/awesome-eve-agents` at all, given the maintainers ship the closest competitor.
3. Whether shadcn.io is worth a sign in. It is the only P1 or P2 item that requires an account, and it is a commercial site.

**Sequence suggestion**

Do P1-A first and alone, because B, C, D and E all quote a description, and it is worth having one canonical string in the manifest before it gets copied into four external surfaces. Then B and C in the same sitting, they are both ten minute PRs. Then E. Then decide on D, F and G.

**What to check in 30 days**

- BlockDex regenerates nightly, so the evex card should show the new description within a day of P1-A landing. If it does not, the field name or the location is wrong.
- registry.directory should pick up the refreshed description after the shadcn-ui/ui PR merges.
- Referring domains: expect 2 to 4 new ones from this batch, not 30. That is the honest number for a niche developer registry.

---

## 6. Sources

- https://ui.shadcn.com/docs/registry/registry-index
- https://ui.shadcn.com/r/registries.json
- https://github.com/shadcn-ui/ui/blob/main/apps/v4/registry/directory.json
- https://registry.directory/ and https://registry.directory/TommyBez/evex
- https://blockdex.kynth.studio/registries/evex
- https://github.com/birobirobiro/awesome-shadcn-ui and its CONTRIBUTING.md
- https://www.shadcn.io/awesome/registries
- https://github.com/doanbactam/awesome-eve
- https://github.com/shadcn-labs/awesome-eve-agents
- https://github.com/bergside/awesome-eve-agents
- https://github.com/vercel/eve
- https://eve.dev/templates
- https://github.com/e2b-dev/awesome-ai-agents
- https://theresanaiforthat.com/get-featured/
- https://openalternative.co/submit
- https://allshadcn.com
- https://tally.so/r/3XybbL
- https://github.com/caramaschiHG/awesome-ai-agents-2026
- https://github.com/caramaschiHG/awesome-ai-agents-2026/pull/502
- https://vercel.com/templates/submit
- https://github.com/vercel/community/discussions/4554
- Playbook: https://github.com/coreyhaines31/marketingskills/blob/main/skills/directory-submissions/SKILL.md
- Product facts: https://evex.sh, https://evex.sh/docs/publishing, https://evex.sh/r/registry.json

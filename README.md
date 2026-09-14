# Best Weavy AI Alternatives After the Figma Acquisition (2026)

![Best Weavy AI Alternatives After the Figma Acquisition (2026)](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/hero.png?v=r5)

A maintained dataset of **weavy ai alternative** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

The tables below are generated from [`data/tools.json`](data/tools.json) by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed. Every tool on this list is a hosted product with no first-party open-source repo, so there are no star counts to report — the refresh re-stamps the check date and regenerates the tables from the data.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-09-14** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Figma Weave (formerly Weavy)](#2-figma-weave-formerly-weavy)
  - [Krea](#3-krea)
  - [Flora AI](#4-flora-ai)
  - [Comfy Cloud](#5-comfy-cloud)
  - [Freepik Spaces](#6-freepik-spaces)
- [What actually changed under Figma](#what-actually-changed-under-figma)
- [How to choose](#how-to-choose)
- [FAQ](#faq)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing |
|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | First-party hosted MCP (Streamable HTTP, OAuth) | Yes | Yes | Multi-model catalog across image, video and audio nodes | [pricing](https://www.wireflow.ai/pricing) |
| **[Figma Weave (formerly Weavy)](#2-figma-weave-formerly-weavy)** | No first-party MCP server documented for Weave | No | [check](https://weave.figma.com/pricing) | Third-party models inside the Weave canvas | [pricing](https://weave.figma.com/pricing) |
| **[Krea](#3-krea)** | No first-party MCP server documented | Yes | [check](https://www.krea.ai/pricing) | Krea’s hosted image and video models | [pricing](https://www.krea.ai/pricing) |
| **[Flora AI](#4-flora-ai)** | MCP and API documented by Flora at flora.ai/mcp | Yes | Yes | Third-party image, video and text models on one canvas | [pricing](https://flora.ai/pricing) |
| **[Comfy Cloud](#5-comfy-cloud)** | No first-party MCP server documented | Yes | Yes | Pre-loaded models and pre-installed custom nodes, run on hosted GPUs | [pricing](https://www.comfy.org/cloud/pricing) |
| **[Freepik Spaces](#6-freepik-spaces)** | No first-party MCP server documented for Spaces | Yes | Yes | Freepik’s hosted image, video and audio models | [pricing](https://www.freepik.com/pricing) |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts how many of the checks in [`data/tools.json`](data/tools.json) → `capabilityChecks` a tool passes. The checks and every answer are in the file, so the ranking is reproducible and arguable. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | Public API | Webhooks | Per-node cost visibility | Batch and array support | Claude Code skill | Score |
|------|---|---|---|---|---|-------|
| **[Wireflow](#1-wireflow)** | ✅ | ✅ | ✅ | ✅ | ✅ | **5/5** |
| **[Krea](#3-krea)** | ✅ | ✅ | ❌ | ❌ | ❌ | **2/5** |
| **[Flora AI](#4-flora-ai)** | ✅ | ✅ | ❌ | ❌ | ❌ | **2/5** |
| **[Comfy Cloud](#5-comfy-cloud)** | ✅ | ❌ | ❌ | ❌ | ❌ | **1/5** |
| **[Figma Weave (formerly Weavy)](#2-figma-weave-formerly-weavy)** | — | — | — | — | — | **0/5** |
| **[Freepik Spaces](#6-freepik-spaces)** | ❌ | ❌ | ❌ | ❌ | ❌ | **0/5** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. Wireflow

*Best Overall*

![Wireflow node canvas screenshot](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/screenshot-wireflow.png?v=r5)

- **What it is:** [Wireflow](https://www.wireflow.ai) is a hosted node-based AI canvas where you chain image, video, audio, and text models visually, then trigger the finished graph over HTTP from any app, script, or agent.
- **Best for:** creative and technical teams who want a visual canvas without giving up programmatic control.
- **Standout:** full REST API with webhooks, batch execution, and per-node cost visibility on every plan including free.
- **Links:**
  - [Homepage](https://www.wireflow.ai)
  - [Docs](https://www.wireflow.ai/docs/mcp)
  - [Pricing](https://www.wireflow.ai/pricing)
  - [REST endpoint](https://www.wireflow.ai/ai-workflow-api)
  - [node-based AI platform with an API](https://www.wireflow.ai/node-based-ai-platform-with-api)

Add the hosted MCP server to Claude Code, then approve the OAuth consent screen:
```bash
claude mcp add --transport http wireflow https://www.wireflow.ai/api/mcp
```
In Claude Desktop or claude.ai, add the same URL as a custom connector. Read-only tools (`list_workflows`, `list_models`, `get_execution`) cost nothing; `run_workflow` is the only one that spends credits.
```text
https://www.wireflow.ai/api/mcp
```

### 2. Figma Weave (formerly Weavy)

*the incumbent canvas, now billed separately from Figma seats*

![Figma Weave homepage screenshot](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/screenshot-figma-weave.png?v=r5)

- **What it is:** a node-based AI creation canvas owned by Figma, with strong editing nodes and a wide model catalog.
- **Limits:** no public API on any self-serve plan. The Enterprise tier lists "Run workflows through API" as coming soon with no announced timeline as of 2026, and Weave credits are still separate from Figma seats, so there is no bundling to plan around yet.
- **Note:** Checked 2026-09-01: weavy.ai redirects to weave.figma.com and the site states "Weavy is now Figma Weave." No public Weave API or developer docs are published; the trial is marked "eligible plans only".
- **Links:**
  - [Homepage](https://weave.figma.com)
  - [Docs](https://help.figma.com)
  - [Pricing](https://weave.figma.com/pricing)

**Getting started:** no public CLI or SDK to install — start from the [docs](https://help.figma.com).

### 3. Krea

*broad model catalog with a public API and Node Apps execution*

![Krea homepage screenshot](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/screenshot-krea.png?v=r5)

- **What it is:** a creative AI suite with a broad model API plus programmatic execution of node apps built in its editor.
- **Limits:** no per-node cost visibility and no documented batch or array endpoints, so large fan-out runs become your own orchestration problem. For [cost-transparent batch pipelines](https://www.wireflow.ai/batch-image-generation-api), Krea leaves the production layer to you.
- **Links:**
  - [Homepage](https://www.krea.ai)
  - [Docs](https://www.krea.ai/docs/)
  - [Pricing](https://www.krea.ai/pricing)
  - [cost-transparent batch pipelines](https://www.wireflow.ai/batch-image-generation-api)

**Getting started:** no public CLI or SDK to install — start from the [docs](https://www.krea.ai/docs/).

### 4. Flora AI

*design studio canvas with a technique execution API*

![Flora AI homepage screenshot](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/screenshot-flora.png?v=r5)

- **What it is:** a design-oriented AI canvas with a technique execution API and signed per-run webhooks.
- **Limits:** the API executes techniques and canvas actions rather than arbitrary node chains, with no batch endpoints and no per-node cost visibility. Seat pricing also means no programmatic access on a free plan.
- **Note:** Checked 2026-09-01: florafauna.ai now redirects to flora.ai. Flora’s own homepage CTA is "Get started for free".
- **Links:**
  - [Homepage](https://flora.ai)
  - [Docs](https://docs.flora.ai)
  - [Pricing](https://flora.ai/pricing)
  - [Flora AI](https://www.florafauna.ai)

**Getting started:** no public CLI or SDK to install — start from the [docs](https://docs.flora.ai).

### 5. Comfy Cloud

*managed hosting for the open-source ComfyUI graph*

![Comfy Cloud homepage screenshot](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/screenshot-comfy-cloud.png?v=r5)

- **What it is:** official managed hosting for ComfyUI graphs, compatible with the local server API.
- **Limits:** the ecosystem still assumes engineering time. Custom node compatibility, model management, and version drift are your problem, and there is no built-in cost accounting. If you want a [hosted canvas without the GPU and DevOps overhead](https://www.wireflow.ai/comfyui-alternative-no-gpu), that tradeoff is the whole decision.
- **Note:** Comfy states plainly: "Build and edit workflows for free — credits are consumed only when the GPU runs."
- **Links:**
  - [Homepage](https://www.comfy.org/cloud)
  - [Docs](https://docs.comfy.org)
  - [Pricing](https://www.comfy.org/cloud/pricing)
  - [hosted canvas without the GPU and DevOps overhead](https://www.wireflow.ai/comfyui-alternative-no-gpu)

**Getting started:** no public CLI or SDK to install — start from the [docs](https://docs.comfy.org).

### 6. Freepik Spaces

*stock library and brand assets wired into a canvas*

![Freepik Spaces screenshot](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/screenshot-freepik-spaces.webp?v=r5)

- **What it is:** a visual AI canvas bundled with a large stock library and brand and approval tooling.
- **Limits:** no public API for canvas workflows on self-serve plans, and canvas execution is enterprise-gated at best. Freepik's separate image generation API does not run Spaces canvases.
- **Note:** Freepik’s own Spaces docs state a free user can create up to 3 Spaces. Checked 2026-09-01: the developer API docs at docs.freepik.com now redirect to docs.magnific.com, Freepik’s API brand.
- **Links:**
  - [Homepage](https://www.freepik.com/spaces)
  - [Docs](https://www.freepik.com/ai/docs)
  - [Pricing](https://www.freepik.com/pricing)
  - [Freepik Spaces](https://www.freepik.com)

**Getting started:** no public CLI or SDK to install — start from the [docs](https://www.freepik.com/ai/docs).

## What actually changed under Figma

Roadmap ownership moved. Weavy chased creative power users as an independent startup; Figma Weave now ships against Figma's platform strategy.

Billing sits in a standalone credit system that is not part of a Figma seat as of 2026, which is the kind of thing that gets restructured once an acquisition settles.

The API stayed where it was, which is to say unavailable.

![Vintage suitcase with leather straps on a stone floor](https://assets.wireflow.ai/linkedin/weavy-ai-alternatives-figma-acquisition/vp3.png)

## How to choose

- **If you need workflows callable from your own code with cost visibility** → [Wireflow](https://www.wireflow.ai/weavy-alternative-with-api)
- **If your team is happy in the editor and does not need programmatic runs** → Figma Weave
- **If you mainly want the widest model catalog behind one API key** → Krea
- **If art direction and studio-grade output matter more than orchestration** → Flora AI
- **If portability of the workflow file is your top concern** → Comfy Cloud
- **If licensed stock assets need to sit inside the canvas** → Freepik Spaces

## FAQ

<details>
<summary><strong>Is Weavy still available after the Figma acquisition?</strong></summary>

Yes, as Figma Weave. Figma acquired Weavy on October 30, 2025, and as of 2026 weavy.ai redirects to weave.figma.com with its own standalone credit plans separate from Figma seats.

</details>

<details>
<summary><strong>Does Figma Weave have an API yet?</strong></summary>

No. As of 2026 there is no public API on any self-serve plan. The Enterprise tier lists workflow execution through an API as coming soon, with no published timeline or documentation.

</details>

<details>
<summary><strong>Which Weavy AI alternative is easiest to migrate to?</strong></summary>

[Wireflow](https://www.wireflow.ai/features/visual-node-editor) maps most closely, since it is also a visual node canvas with chained model nodes. The difference is that every finished graph also exposes a REST endpoint you can call.

</details>

<details>
<summary><strong>Will Figma Weave pricing change?</strong></summary>

No pricing merge with Figma seats has been announced as of 2026. Current standalone plans run from a free 150-credit tier up to Team at $60 per user per month, with top-ups at $10 per 1,200 credits.

</details>

<details>
<summary><strong>Can I export my Weavy workflows elsewhere?</strong></summary>

Not as a portable standard. Proprietary canvases store graphs in their own format, which is why teams worried about lock-in favour either an open graph format or a platform whose workflows are callable by API.

</details>

<details>
<summary><strong>What should I check before committing to any AI canvas?</strong></summary>

Check whether workflows run without a human in the editor, whether pricing is per seat or per usage, and whether costs are visible per step. Those three answers predict most migration pain later.

</details>

## The short version

The Figma acquisition did not break Weavy. It changed who decides what the product becomes, and it left the one gap that mattered to teams building on top of it still open as of 2026.

If your work only ever happens inside an editor, Figma Weave remains a strong canvas and staying is reasonable. If your workflows need to run on a schedule, inside an app, or across hundreds of inputs, the canvas has to be callable.

That is where Wireflow lands: full REST API on every tier, webhooks, batch execution, per-node cost visibility, and video assembly in the same graph. [Try Wireflow free](https://www.wireflow.ai) and port one workflow across.

## How this list is maintained

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run — edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE) — public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).

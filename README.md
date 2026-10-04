# AWESOME-Agentic-Policy

A curated collection of the latest papers and resources on **agentic policies** for robotics — work where an AI agent (an LLM, a VLM, or a coding agent) sits in the loop of *producing* or *running* a robot policy: planning and orchestrating skills, writing the policy as code, authoring the rewards, priors and simulations a policy is trained on, and reflecting on the results to improve it.

> 🔎 **[Interactive filterable version »](https://xyc0212.github.io/AWESOME-Agentic-Policy/)** — live search and tag filters (Plan / Code / Rew / Sim / Tool / Mem / Refl / Fnd). Requires GitHub Pages to be enabled (Settings → Pages → deploy from branch → `/docs`).

## Categories

Each paper is tagged across the following themes:

- **Plan** — Planning & orchestration: the agent decomposes a task and sequences skills at run time
- **Code** — Code as policy: the agent writes executable programs that act as the policy
- **Rew** — Reward & objective design: the agent authors the rewards, costs or priors a policy is trained on
- **Sim** — Simulation & data authoring: the agent builds tasks, scenes or assets, tunes simulator parameters, or generates training data
- **Tool** — Tool & skill use: the agent calls learned low-level policies (VLAs, RL skills), perception models or other tools, or grows a skill library
- **Mem** — Memory: experience stored and retrieved across steps or episodes
- **Refl** — Reflection & self-improvement: failure detection, self-correction, closed-loop refinement from feedback
- **Fnd** — Foundation paper: seminal earlier work the current literature builds on

## Papers

<!-- markdownlint-disable MD060 -->

| # | Title | Venue | Year | Affiliation | Plan | Code | Rew | Sim | Tool | Mem | Refl | Fnd | Links |
|---|-------|-------|------|-------------|:----:|:----:|:---:|:---:|:----:|:---:|:----:|:---:|-------|

<!-- markdownlint-enable MD060 -->

## Contributing

Contributions are welcome! To add a paper, append a new row to the table above with:

- The **title** in the Title column, with all links in the **Links** column.
- The **venue** (e.g. CoRL, ICRA, RSS, NeurIPS, arXiv) and **year**.
- A `✅` in each theme column that genuinely applies (`Plan`, `Code`, `Rew`, `Sim`, `Tool`, `Mem`, `Refl`, `Fnd`).
- Links in the format `[Paper](url) · [Project](url) · [Code](url)` (include only the ones that exist).

Please keep the table sorted with the newest papers first.

The README table is the single source of truth. After editing it, regenerate the interactive page with:

```bash
python3 scripts/gen_site.py
```

and commit the updated `docs/index.html`.

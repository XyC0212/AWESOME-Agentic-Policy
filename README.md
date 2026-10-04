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
| 1 | Generalizing Manipulation Skills with a Local Coding Agent | arXiv | 2026 | Ghent University – imec |  | ✅ |  |  |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.26499) · [Project](https://rtalwar2.github.io/agentic-coding-for-robot-manipulation/) |
| 2 | Coding Agents with an Obstacle-Aware Harness for Safe Robot Manipulation | arXiv | 2026 | USC | ✅ | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.20822) |
| 3 | Agent as Policy for Robotic Manipulation | arXiv | 2026 | University of Notre Dame | ✅ | ✅ |  |  |  | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2609.12541) · [Project](https://agent-as-policy-2026.github.io/) · [Code](https://github.com/agent-as-policy-2026/agent-as-policy) |
| 4 | Revisiting the "Push-T" Robot Manipulation Task with Agentic Robotics | arXiv | 2026 | UC Berkeley |  | ✅ |  | ✅ |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2608.18227) |
| 5 | ENPIRE: Agentic Robot Policy Self-Improvement in the Real World | CoRL | 2026 | NVIDIA |  |  | ✅ |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2606.19980) · [Project](https://research.nvidia.com/labs/gear/enpire) · [Code](https://github.com/NVlabs/ENPIRE) |
| 6 | Playful Agentic Robot Learning | arXiv | 2026 | UC Berkeley | ✅ | ✅ |  |  | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2606.19419) · [Project](https://playful-rats.github.io/) · [Code](https://github.com/Playful-RATs/rats) |
| 7 | RHO: Your Coding Agent is Secretly a Roboticist | arXiv | 2026 | UC Berkeley |  | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2606.16458) · [Project](https://rho-robotics.github.io) · [Code](https://github.com/KE7/HELIX) |
| 8 | RoboClaw: An Agentic Framework for Scalable Long-Horizon Robotic Tasks | arXiv | 2026 | AgiBot | ✅ |  |  | ✅ | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2603.11558) · [Project](https://roboclaw-agibot.github.io/) · [Code](https://github.com/RoboClaw-Robotics/RoboClaw) |

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

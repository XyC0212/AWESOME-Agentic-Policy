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
| 1 | Reconstruct, Practice, Go Real: Guided Self-Improvement for Embodied Agents | arXiv | 2026 | UC Berkeley |  | ✅ |  | ✅ | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2610.02204) · [Project](https://rpg-robot.github.io) |
| 2 | SimEX: Simulation-Integrated Robotics AutoResearch | arXiv | 2026 | Amazon FAR |  | ✅ |  | ✅ | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2609.38982) · [Project](https://robo-simex.github.io/) |
| 3 | Find Something You Can't Do: Agentic Real-World Reinforcement Learning for Self-Improving VLA Models | arXiv | 2026 | TU Darmstadt |  |  | ✅ |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.32069) · [Project](https://fangyzzz.github.io/FIND.github.io/) |
| 4 | RAPID: Robot Agentic Programming from Demonstrations | arXiv | 2026 | MIT |  | ✅ |  | ✅ | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.30249) · [Project](https://yuyaoliu.me/projects/rapid) |
| 5 | Generalizing Manipulation Skills with a Local Coding Agent | arXiv | 2026 | Ghent University – imec |  | ✅ |  |  |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.26499) · [Project](https://rtalwar2.github.io/agentic-coding-for-robot-manipulation/) |
| 6 | Coding Agents with an Obstacle-Aware Harness for Safe Robot Manipulation | arXiv | 2026 | USC | ✅ | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.20822) |
| 7 | Agent as Policy for Robotic Manipulation | arXiv | 2026 | University of Notre Dame | ✅ | ✅ |  |  |  | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2609.12541) · [Project](https://agent-as-policy-2026.github.io/) · [Code](https://github.com/agent-as-policy-2026/agent-as-policy) |
| 8 | Show-Harness: Just a VLM Agent Can Play Robots | arXiv | 2026 | NUS | ✅ |  |  |  |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2609.10522) · [Project](https://showlab.github.io/Show-Harness) · [Code](https://github.com/showlab/Show-Harness) |
| 9 | Revisiting the "Push-T" Robot Manipulation Task with Agentic Robotics | arXiv | 2026 | UC Berkeley |  | ✅ |  | ✅ |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2608.18227) |
| 10 | Addressing the Orchestration Gap in Generalist Robots via Physical Agency | arXiv | 2026 | Princeton University | ✅ |  |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2607.21725) · [Project](https://lianegalanti.github.io/Pigey/) · [Code](https://github.com/lianegalanti/Pigey) |
| 11 | Agentic Real2Sim: Physics-based World Modeling with Vision-Language Agents | arXiv | 2026 | University of British Columbia |  |  |  | ✅ | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2607.19190) · [Project](https://agentic-real2sim.github.io) · [Code](https://github.com/agentic-real2sim/agentic_real2sim) |
| 12 | RoboHarness: Memory-Driven Orchestration of Heterogeneous Robot Policies for Long-Horizon Planning | ECCV Workshop | 2026 | Huawei Noah's Ark Lab | ✅ |  |  |  | ✅ | ✅ |  |  | [Paper](https://arxiv.org/abs/2607.18060) |
| 13 | VIA: Visual Interface Agent for Robot Control | arXiv | 2026 | Stanford University | ✅ |  |  |  |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2607.11119) |
| 14 | Harness VLA: Steering Frozen VLAs into Reliable Manipulation Primitives via Memory-Guided Agents | arXiv | 2026 | Tsinghua University | ✅ |  |  |  | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2607.08448) · [Project](https://harnessvla.github.io/) · [Code](https://github.com/RLinf/RPent) |
| 15 | GaP: A Graph-as-Policy Multi-Agent Self-Learning Harness For Variational Automation Tasks | arXiv | 2026 | UC Berkeley |  | ✅ |  | ✅ | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2607.05369) · [Project](https://graph-robots.github.io/gap) · [Code](https://github.com/graph-robots/graph-as-policy) |
| 16 | ASPIRE: Agentic /Skills Discovery for Robotics | arXiv | 2026 | NVIDIA |  | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2607.00272) · [Project](https://research.nvidia.com/labs/gear/aspire/) · [Code](https://github.com/NVlabs/ASPIRE) |
| 17 | ENPIRE: Agentic Robot Policy Self-Improvement in the Real World | CoRL | 2026 | NVIDIA |  |  | ✅ |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2606.19980) · [Project](https://research.nvidia.com/labs/gear/enpire) · [Code](https://github.com/NVlabs/ENPIRE) |
| 18 | Playful Agentic Robot Learning | arXiv | 2026 | UC Berkeley | ✅ | ✅ |  |  | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2606.19419) · [Project](https://playful-rats.github.io/) · [Code](https://github.com/Playful-RATs/rats) |
| 19 | Guava: Distilling Frontier VLMs into a Compact Agent through a Robotic Manipulation Harness | arXiv | 2026 | University of Maryland | ✅ |  |  | ✅ | ✅ |  |  |  | [Paper](https://arxiv.org/abs/2606.18363) · [Project](https://guava-harness.github.io) · [Code](https://github.com/hdacnw/guava-release) |
| 20 | RHO: Your Coding Agent is Secretly a Roboticist | arXiv | 2026 | UC Berkeley |  | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2606.16458) · [Project](https://rho-robotics.github.io) · [Code](https://github.com/KE7/HELIX) |
| 21 | What Matters in Orchestrating Robot Policies: A Systematic Study of Hierarchical VLA Agents | arXiv | 2026 | Google DeepMind | ✅ |  |  |  | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2606.10267) · [Project](https://jiahenghu.github.io/hi-vla) |
| 22 | HARBOR: A Harness Framework for Agentic Robot Reinforcement Learning | arXiv | 2026 | TU Darmstadt |  |  | ✅ | ✅ |  | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2606.08610) |
| 23 | VoLo: A Physical Orchestrator for Open-Vocabulary Long-Horizon Manipulation | CoRL | 2026 | NVIDIA | ✅ |  |  |  | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2606.07723) · [Project](https://chicychen.github.io/VoLo/) · [Code](https://github.com/NVlabs/VoLoAgent) |
| 24 | RDA: Reward Design Agent for Reinforcement Learning | RLC | 2026 | Meta |  |  | ✅ |  |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2606.01672) · [Project](https://nitinkamra1992.github.io/reward-design-agent) |
| 25 | From Reaction to Anticipation: Proactive Failure Recovery through Agentic Task Graph for Robotic Manipulation | RSS | 2026 | CUHK-Shenzhen | ✅ | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2605.11951) · [Project](https://shengxu.net/AgentChord/) · [Code](https://github.com/EDEM-AI/AgentChord) |
| 26 | CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation | ICML | 2026 | NVIDIA |  | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2603.22435) · [Project](https://capgym.github.io) · [Code](https://github.com/capgym/cap-x) |
| 27 | RoboClaw: An Agentic Framework for Scalable Long-Horizon Robotic Tasks | arXiv | 2026 | AgiBot | ✅ |  |  | ✅ | ✅ | ✅ | ✅ |  | [Paper](https://arxiv.org/abs/2603.11558) · [Project](https://roboclaw-agibot.github.io/) · [Code](https://github.com/RoboClaw-Robotics/RoboClaw) |
| 28 | Uni-Skill: Building Self-Evolving Skill Repository for Generalizable Robotic Manipulation | ICRA | 2026 | ICT, Chinese Academy of Sciences | ✅ | ✅ |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2603.02623) |
| 29 | SceneSmith: Agentic Generation of Simulation-Ready Indoor Scenes | ICML | 2026 | MIT |  |  |  | ✅ | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2602.09153) · [Project](https://scenesmith.github.io/) · [Code](https://github.com/nepfaff/scenesmith) |
| 30 | VLS: Steering Pretrained Robot Policies via Vision-Language Models | CoRL | 2026 | University of Washington |  |  | ✅ |  | ✅ |  |  |  | [Paper](https://arxiv.org/abs/2602.03973) · [Project](https://vision-language-steering.github.io/webpage/) · [Code](https://github.com/Vision-Language-Steering/code) |
| 31 | Towards Reliable Code-as-Policies: A Neuro-Symbolic Framework for Embodied Task Planning | NeurIPS | 2025 | Sungkyunkwan University | ✅ | ✅ |  |  |  |  | ✅ |  | [Paper](https://arxiv.org/abs/2510.21302) |
| 32 | Gemini Robotics 1.5: Pushing the Frontier of Generalist Robots with Advanced Embodied Reasoning, Thinking, and Motion Transfer | arXiv | 2025 | Google DeepMind | ✅ |  |  |  | ✅ |  | ✅ |  | [Paper](https://arxiv.org/abs/2510.03342) |
| 33 | HumanoidGen: Data Generation for Bimanual Dexterous Manipulation via LLM Reasoning | NeurIPS | 2025 | TeleAI, China Telecom |  | ✅ |  | ✅ |  |  |  |  | [Paper](https://arxiv.org/abs/2507.00833) · [Project](https://openhumanoidgen.github.io) · [Code](https://github.com/TeleHuman/HumanoidGen) |

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

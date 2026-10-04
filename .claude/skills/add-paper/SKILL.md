---
name: add-paper
description: Catalogue an agentic-policy paper into this repo. Use this WHENEVER the user provides a paper to add — an arXiv link, any URL, a title, or a PDF/file. It reads the paper, assigns theme labels (Plan/Code/Rew/Sim/Tool/Mem/Refl/Fnd), adds a row to the README table, writes a short plain-language summary to SUMMARIES.md for later retrieval, regenerates the GitHub Pages site, and commits.
---

# Add a paper to AWESOME-Agentic-Policy

When the user gives you a paper, run this end-to-end. The README table is the single
source of truth; everything else is derived from it.

## Labels

Assign **every** label that genuinely applies (a paper often has several). Do not add a
label that doesn't truly apply. If none fits, tell the user rather than forcing one.

- **Plan** — Planning & orchestration: the agent decomposes a task and sequences skills at
  run time
- **Code** — Code as policy: the agent writes executable programs that act as the policy
- **Rew** — Reward & objective design: the agent authors the rewards, costs or priors a
  policy is trained on
- **Sim** — Simulation & data authoring: the agent builds tasks, scenes or assets, tunes
  simulator parameters, or generates training data
- **Tool** — Tool & skill use: the agent calls learned low-level policies (VLAs, RL
  skills), perception models or other tools, or grows a skill library
- **Mem** — Memory: experience stored and retrieved across steps or episodes
- **Refl** — Reflection & self-improvement: failure detection, self-correction,
  closed-loop refinement from feedback
- **Fnd** — Foundation paper: seminal earlier work the current literature builds on

The label set is defined in three places that must stay in step: the `TAGS` list in
[scripts/gen_site.py](../../../scripts/gen_site.py), the Categories list and table header
in [README.md](../../../README.md), and the list above.

## Steps

1. **Read the paper.** Fetch the source (WebFetch for a URL; for arXiv use the
   `/abs/<id>` page for metadata and `/html/<id>` or the PDF for content; Read for a local
   file). Extract:
   - exact **title**
   - **venue** (publication venue, or `arXiv` if unpublished) and **year**
   - **primary (first) affiliation** only — unless the user asks to list more
   - **links**: a `Paper` link (prefer `https://arxiv.org/abs/...`), plus `Project` and
     `Code` links **only if they genuinely exist** (verify; never invent a URL)
   Read enough of the abstract/method to assign labels and write the summary.

2. **Determine the labels** from the list above.

3. **Update the README table** ([README.md](../../../README.md)). Insert a new row in the
   correct sorted position (**newest year first**; new same-year papers go at the top of
   that year). Row format (14 columns):

   ```
   | <#> | <Title> | <Venue> | <Year> | <Primary Affiliation> | <Plan> | <Code> | <Rew> | <Sim> | <Tool> | <Mem> | <Refl> | <Fnd> | <Links> |
   ```

   Put `✅` in each applicable label column, leave the others blank. Links column:
   `[Paper](url) · [Project](url) · [Code](url)` (only the ones that exist). The `#` value
   doesn't matter at insert time — step 5 renumbers.

4. **Write the summary** by adding one bullet to the top of the list in
   [SUMMARIES.md](../../../SUMMARIES.md), directly below the intro paragraph (newest
   first, matching the table). Format:

   ```text
   - **<Title>** ([paper](<url>)) — <what the method does, then the key result>.
   ```

   **One or two sentences, never more.** Write for a researcher who knows robot learning
   but has only a little background in LLM agents: the first sentence says what the paper
   does and how, in plain language; the second (optional) gives the headline result or
   the one thing that makes the paper notable. Clarity beats completeness — a reader
   skimming this file should grasp the idea without opening the paper.

   - Prefer plain wording over the paper's branded names. If a coined term is worth
     keeping, say what it does in a few words rather than dropping it in bare.
   - Expand an acronym on first use unless it is everyday vocabulary here (LLM, VLM, VLA,
     RL, IL, sim-to-real are fine as-is).
   - Say what the agent actually does: what it reads, what it writes, and whether it runs
     while the robot acts or only before training.
   - Keep a number only when it carries the claim (a headline success rate, a dataset
     size). Drop per-task breakdowns and ablation detail.
   - No stacked clauses. If a sentence needs a second "and ... while ...", split it or
     cut it.

   Good:

   ```text
   - **Eureka: ...** ([paper](...)) — Has a large language model write the reward
     function as code, trains an RL policy with each candidate, and feeds the training
     statistics back so the model can rewrite the reward over several rounds. The
     resulting rewards beat human-written ones on 83% of 29 simulated tasks.
   ```

   Too dense (one run-on, branded terms unexplained — avoid this):

   ```text
   - **Eureka: ...** ([paper](...)) — Eureka performs in-context evolutionary
     optimization over GPT-4-generated reward code with environment-as-context and reward
     reflection, zero-shot producing executable rewards without task-specific prompts,
     outperforming expert rewards on 83% of 29 environments across 10 morphologies with a
     52% average normalized improvement and enabling pen spinning on a Shadow Hand via
     curriculum learning.
   ```

   This file is the retrieval index; do not duplicate labels/venue/year/affiliation here —
   those live in the README table.

   Then create an empty **notes stub** at `notes/<slug>.md` for the user to fill in their
   own opinion. `<slug>` is lowercase and hyphen-separated: the paper's short name
   followed by the key words of its title (e.g.
   `eureka-human-level-reward-design-coding-llms`). Template:

   ```markdown
   # <Title>

   > [Paper](<url>) · [Project](<url>) · metadata in [README](../README.md) · summary in [SUMMARIES.md](../SUMMARIES.md)

   ## My take

   _Your opinion here — strengths, weaknesses, relevance to your work, ideas to borrow._

   ## Notes

   -
   ```

   Include only the links that exist. Never overwrite a notes file that already exists.

5. **Renumber and regenerate**, from the repo root:

   ```bash
   python3 scripts/renumber.py && python3 scripts/gen_site.py
   ```

6. **Commit.** Stage and commit all changes with a message like
   `Add <short title> to the table`. Then push (`git push`) when the repo has an `origin`
   remote, so new papers go live on the GitHub Pages site. If you are unsure whether to
   push, ask.

7. **Push to the user's Zotero (auto, best-effort).** For an arXiv paper, run from the
   repo root:

   ```bash
   python3 scripts/zotero_lib.py <arxiv-id> --best-effort
   ```

   This creates a Zotero item in the **"Agentic Policy"** collection and uploads the PDF
   via the Zotero Web API (needs network, so allow it). `--best-effort` means it exits 0
   and just prints a notice if Zotero is not configured (`scripts/zotero_secrets.json` /
   env vars) or `pyzotero` is missing — never let this block the flow. Tell the user the
   result: added + PDF, already-in-library, or the setup notice. Skip this step for
   non-arXiv papers.

8. **Report** to the user: the new table row, the chosen labels, the summary, the summary
   file path, and the Zotero push result.

## Retrieval

When the user later asks you to find / recall a paper ("which paper had an LLM write the
reward function?", "the one that tunes the simulator from real rollouts", "the paper I
liked for its memory design"), read [SUMMARIES.md](../../../SUMMARIES.md) for the
summaries, the [README table](../../../README.md) for labels/year/affiliation, and the
[notes/](../../../notes/) files for the user's own opinions (`## My take`). Answer from the
matching entry, citing the paper link.

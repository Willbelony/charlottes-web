# Charlotte's WEB

## What it is

Charlotte's WEB is my personal AI office, built step by step on Claude Code. **Charlotte** is the assistant I talk to; **Charlotte's WEB** is the whole system around it (WEB is a nod to my initials). Instead of one chatbot that forgets everything, it's a small team of named agents with written rules, file-based memory, and tested boundaries — documented here as it actually happens, including the surprises.

## What I want it for

Saving time and executing real projects: things like building a Roblox game, helping run a YouTube channel, or researching income opportunities. I approve goals; the team handles the routine work inside them and comes back to me only for decisions that are actually mine — publishing, spending, messaging anyone, or changing what I'll receive.

## What works today

- **Memory.** One authoritative home per fact, in plain files. Tested: a fresh session recovered the goal, status, and next action from a single read of `progress.md`.
- **Boundaries.** Every claimed protection was probed with dummy files — reads, writes, and network access outside the project are blocked or ask first, and the results are recorded honestly as BLOCKED / ASKED / UNTESTED.
- **The first two agents, on paper and in practice:**
  - **Alpha** — the manager. Assigns work inside approved goals, checks quality against written criteria, works around routine blockers, and flags opportunities I might miss.
  - **Beta** — the researcher. Every claim in a Beta brief carries a source and a confidence tag (*verified*, *single-source*, or *inference*), with a hard budget of sources per task. What Beta can't support, it reports as unknown instead of guessing.
- **A real handoff.** Alpha launched a separate agent to act as Beta, gave it its first small job — summarize the access-test results saved in `plan.md` — checked the finished work, and caught an outdated detail during review. The full story is in the [build log](build-log.md).

## What's planned

- **"The Office"** — a visual space where I can walk in, ask "what's going on?", and see my team: open Beta's research lab and see its current assignment, findings, or idle status for example.
- **Beta as a reusable, on-demand researcher**, with **Gemini Deep Research** as the first external engine to test (not yet tried). When we test it, the result goes in the build log — and this README gets updated if Beta's model changes.
- **More agents** (working names Charlie and Delta) once their jobs are defined; models chosen per job by how well they do it.

## How I’m building it

- **Project memory.** I save decisions and next steps in plain files so Charlotte can pick up where we left off.
- **Access checks.** I test what Charlotte can read, write, and access online, then record what happened.
- **Agent responsibilities.** I define each agent’s job, walk through an example, and test it on a small task before giving it more responsibility.
- **Usage limits.** Agents run when there’s a job to do. Beta gets a research budget and asks before going over it.

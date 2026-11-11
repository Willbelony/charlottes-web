# Build log

## 001 — Stage 1: a foundation you can poke (2026-11-10)

Before any agents, the boring parts had to be real. Stage 1 built and tested the foundation on my Mac:

- **A project home** — plain Markdown files with one authoritative home per fact: permanent rules, a milestone plan, a current-state file (`progress.md`), and dated notes for decisions and findings.
- **Memory, proven.** The acceptance test: open a completely fresh session and type only "Resume Charlotte." It recovered the goal, status, and next action from a single read of `progress.md` — one file read, zero failed attempts, about 8 seconds.
- **Access tests.** I ran seven checks using dummy files. The attempts I tested to read or change files outside the project were blocked. A network request from Charlotte's shell was blocked, and its web tool asked for permission. **The surprise was that Charlotte's shell couldn't run Git inside the project either. My workaround is to run Git myself in Mac Terminal.**
- **Git and backups.** I saved the first version of the project with Git and made a backup. To check that I could recover it, I restored the backup into a new folder and confirmed that the saved version and all nine tracked files were there.

The principle Stage 1 set: nothing gets called "secure" or "working" until it's been tested, and the test results live in the files, not in anyone's memory.

## 002 — The first real handoff (2026-11-10)

With the foundation proven, Alpha and Beta's rules were designed on paper, approved, and walked through in a simulated example... **Then came the first real work!**

For the first job, I kept it small. Alpha, my manager, launched a separate Claude agent to act as Beta, my researcher. It asked Beta to read the earlier access-test results saved in `plan.md` and write a short summary explaining what passed and what was still unknown. Beta saved that summary in the project, with references to the results it used.

**Alpha caught something during review.** Beta's summary said I still needed to decide how to handle Git. I'd already decided to run it myself in Terminal, but the older notes Beta read hadn't caught up. Alpha spotted the mismatch and added a correction. That showed me why the review matters: a summary can accurately repeat its source and still miss a decision made since.

What this proved:
- Alpha could give a separate agent a job and receive its finished work.
- Beta could read a project file on my Mac and save a summary with supporting references.
- Alpha's review caught an outdated detail before it became my next action.

Next, I'm making Beta a researcher I can call on for different assignments without explaining its role each time. Then I'll test Gemini Deep Research for that job and document how it goes. The Office comes later: a visual space where I can see the team's real assignments, progress, and results.

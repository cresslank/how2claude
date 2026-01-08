# how2claude

**A starter kit and guide for non-programmers using AI coding tools**

This repository is a template plus a guide for learning to use Claude Code, Codex, and
similar tools. The guide is split into short docs in the `guide_docs/` folder.

> **Note:** These tools evolve quickly. Commands, features, and interfaces may change.
> If you find something outdated or incorrect, please [open an issue](../../issues) or
> submit a pull request. Last verified: January 2026.

## Where to Start

If you are brand new, start with "I have not installed anything" and work down.

| You are here... | Start here |
|----------------|------------|
| I have not installed anything | [Getting Started](guide_docs/getting-started.md) |
| I need a checklist for Mac, Windows, or Linux | [Choose Your OS Path](guide_docs/getting-started.md#choose-your-operating-system) |
| The terminal feels intimidating | [Terminal Basics](guide_docs/getting-started.md#terminal-basics) |
| I have tools installed but no project | [Create Your Project](guide_docs/project-setup.md) |
| I have a project and want to start coding | [Your First AI Session](guide_docs/first-session.md) |
| I need Git basics | [Git Foundation](guide_docs/git-foundation.md) |
| I am stuck or got an error | [Troubleshooting](guide_docs/troubleshooting.md) |
| I just want the commands | [Quick Reference](guide_docs/quick-reference.md) |

## Why This Setup

Many non-technical people use ChatGPT and Claude like a search engine: ask a question, get
an answer. But these tools can do much more - they can make your computer do things, not
just answer questions. This project exists to help people bridge that gap.

The browser and mobile apps hit a wall. Chat interfaces are great for questions, but they
cannot see your files, run anything on your computer, and forget a lot between sessions.
You end up copy-pasting constantly and explaining context over and over.

Tools like Claude Code, Codex, and Droid can read everything in a folder on your computer,
create and modify files, run commands, and iterate based on what happens. The value is not
what happens the first time - it is what happens the hundredth time. Over time you can
build tools that you and your AI can use over and over again, without needing to explain
yourself at length each time.

Git is your save and undo button. When you are experimenting with AI that can modify things
on your computer, you need a safety net.

The setup is a one-time cost. Yes, there is friction upfront. But once you have done it once,
starting new projects gets easier.

### What can you actually do?

Here are concrete examples. None of these require you to know how to code.

**Research and synthesis**

You have 15 PDFs of research papers on a topic. Instead of reading them all yourself:
- "Read all the PDFs in this folder and create a summary document listing the key findings,
  grouped by theme. Note where sources disagree."
- "Which of these papers discusses [specific topic]? Pull the relevant quotes."
- "Create an annotated bibliography from these sources."

**Writing workflows**

You are writing a memo or report:
- "Here is my rough outline. Turn it into a first draft, keeping my voice."
- "Read draft.md and suggest structural improvements. Do not rewrite - just tell me what
  to consider."
- "Create three different versions of the executive summary - one for technical readers,
  one for executives, one for external stakeholders."

**Data and documents**

You have messy files that need organizing:
- "There are 200 files in this folder with inconsistent names. Rename them to follow the
  pattern YYYY-MM-DD_description.ext and create a log of what changed."
- "Read all the CSVs in data/ and tell me what columns they have in common. Then merge
  them into one file."
- "Convert all the .docx files in this folder to markdown."

**Automation**

You do the same thing repeatedly:
- "Write a script that takes a markdown file and uploads it to my Google Drive folder."
- "Every file in inbox/ should be renamed with today's date and moved to archive/."
- "Create a script that checks this website daily and emails me if the price drops below $X."

The key insight: these tools can see and manipulate your actual files. The browser-based
chat cannot. That is the difference.

### The mindset

You are not trying to become a programmer. You are learning to collaborate with a very fast,
very literal assistant that happens to write code.

The AI is like an eager junior employee: technically capable, but needs clear direction. Your
job is to:

1. Know what you want (roughly)
2. Communicate it clearly
3. Review the work
4. Course-correct as needed

Start small. Build something trivial. Break it. Fix it. The confidence comes from doing, not
from reading guides like this one.

## About This Template

| File/Folder | Purpose |
|-------------|---------|
| `README.md` | Index for this guide |
| `guide_docs/` | The guide content (split into short docs) |
| `CLAUDE.md` | Instructions for AI tools - customize for your project |
| `AGENTS.md` | Points other AI tools to CLAUDE.md |
| `.gitignore` | Tells Git which files to ignore |
| `scripts/` | Utility scripts and automation |
| `docs/` | Documentation and notes |
| `projects/` | Your project code |

## Contributing

Found something wrong or outdated? Want to improve the guide?

- **Report issues:** [Open an issue](../../issues) describing what is wrong or confusing
- **Fix it yourself:** Fork the repository (make your own copy), make changes, and submit a pull request
- **Suggest improvements:** Open an issue with your idea

This guide tries to stay simple and practical. When contributing, keep in mind:
- The audience is non-technical people who are new to all of this
- Prefer concrete examples over abstract explanations
- Do not assume knowledge of programming concepts
- Keep it short - people can always learn more later

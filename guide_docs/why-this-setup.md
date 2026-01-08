# Why This Setup

## Why bother with all this?

If you are not technical, you might be wondering:
"Can't I just use ChatGPT in my browser? Why do I need terminals and Git and all this stuff?"

You can absolutely start with just the browser. But here is why this setup pays off:

The browser hits a wall. Chat interfaces are great for questions, but they cannot see your
files, cannot run anything, and forget everything between sessions. You end up copy-pasting
constantly, explaining context over and over, and manually applying every change.

These tools work with your actual files. Claude Code, Codex, and Droid can read everything
in a folder, create and modify files, run commands, and iterate based on what happens - all
without you playing middleman.

Git is your undo button. When you are experimenting with AI that can modify your code, you need
a safety net. Git lets you checkpoint your work and roll back when things go sideways. This is
non-negotiable.

The setup is a one-time cost. Yes, there is friction upfront. But once you have done it once,
starting new projects takes minutes.

If you are still skeptical, try one small thing with this setup.

## What can you actually do?

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

## The mindset

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

---
<!-- nav -->
Next: [Getting Started](getting-started.md)

# Why This Setup

## Why bother with all this?

If you are not technical, you might be wondering:
"Can't I just use ChatGPT in my browser? Why do I need terminals and Git and all this stuff?"

You can absolutely start with just the browser or the mobile app. But here is why this
setup pays off:

The browser and mobile apps hit a wall. They will likely continue to hit a wall for some
time, even as AI gets smarter and chat interfaces get better. Chat interfaces are great
for questions, but they generally cannot see your files, run anything on your computer,
and forget a lot between sessions. You end up copy-pasting constantly, explaining context
over and over, and fighting with integrations.

Tools like Claude Code, Codex, and Droid can read everything in a folder on your computer,
create and modify files, run commands, and iterate based on what happens. The value is not
what happens the first time - it is what happens the hundredth time. Over time you can
build your work environment so you have tools that you and your AI can use over and over
again. The goal for most people should be to build tools with AI that enable you to do
more things without needing to explain yourself at length each time. When you login to
your email client, you (thankfully!) do not need to explain to your email that you would
like to send an email, that you want it to go to this person and so on. Instead, you have
some buttons that you can press. Buttons are great! That is the goal here - to work with
AI to give yourself a button that does something you need without needing to talk to anyone.

Git is your save and undo button. When you are experimenting with AI that can modify things
on your computer, you need a safety net. This is, for lots of reasons, not foolproof at all.
However, using Git lets you checkpoint your work in a folder, save your progress so you can
access it elsewhere, and roll back when things go sideways. To be explicit - Git is what we are
doing here on github.com.

The setup is a one-time cost. Yes, there is friction upfront. But once you have done it once,
starting new projects gets easier - and as you build on what you have created before, you
will be able to do things better and faster than you were able to previously.

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

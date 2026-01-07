# how2claude

**A starter kit and guide for non-programmers using AI coding tools**

---

## You're Here! Now What?

You've found (or been sent) this repo. Here's how to use it:

1. **Get an account** with one of these AI providers (you need one to use their coding tools):
   - [Claude](https://claude.ai) — Sign up for Claude Pro ($20/month) to use Claude Code
   - [ChatGPT](https://chatgpt.com) — Sign up for ChatGPT Plus ($20/month) to use Codex
   - [Factory](https://factory.ai) — For Droid CLI (supports multiple models including open source)

   > **Note:** You do NOT need API keys for these tools. They use your regular subscription.

2. **Create your project** from this template (see below)

3. **Start building** using the guide included here

---

## Why Bother With All This?

If you're not technical, you might be wondering: *"Can't I just use ChatGPT in my browser? Why do I need terminals and Git and all this stuff?"*

You can absolutely start with just the browser. But here's why this setup pays off:

**The browser hits a wall.** Chat interfaces are great for questions and small scripts, but they can't see your files, run your code, or remember your project structure. You end up copy-pasting constantly, explaining context over and over, and manually applying every change.

**These tools work *with* your files.** Claude Code, Codex, and Droid can read your entire project, make changes across multiple files, run commands, and iterate based on errors—all without you playing middleman.

**Git is your undo button.** When you're experimenting with AI that can modify your code, you need a safety net. Git lets you checkpoint your work and roll back when things go sideways. This is non-negotiable.

**The setup is a one-time cost.** Yes, there's friction upfront. But once you've done it once, starting new projects takes minutes. And you'll be dramatically more productive than browser-only workflows.

If you're still skeptical, try building one small thing with this setup. The difference becomes obvious fast.

---

## Quick Navigation

Jump to where you need:

| I need to... | Go to |
|--------------|-------|
| Understand why this is worth the setup | [Why Bother?](#why-bother-with-all-this) |
| Set up everything from scratch | [Part 1: Environment Setup](#part-1-setting-up-your-environment) |
| Learn Git basics | [Part 2: The GitHub Foundation](#part-2-the-github-foundation) |
| Create my project from this template | [Create Your Project](#create-your-project) |
| Start my first AI session | [Part 3: Your First Session](#part-3-your-first-ai-coding-session) |
| Understand the template files | [What's In This Repo](#whats-in-this-repo) |
| Fix something that's broken | [Troubleshooting](#troubleshooting) |
| Just see the commands | [Quick Reference](#quick-reference) |

---

## Create Your Project

This is a **template repository**. Instead of cloning it directly, you'll create your own copy:

1. Click the green **"Use this template"** button at the top of this page
2. Select **"Create a new repository"**
3. Name your repo (e.g., `scratch` for a playground, or something descriptive for a real project)
4. Click **"Create repository"**

Now clone YOUR new repo to your computer:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

Then customize the `CLAUDE.md` (for Claude Code) or `AGENTS.md` (for other tools) with your project details.

If you don't have Git yet, start with [Part 1](#part-1-setting-up-your-environment).

---

## What's In This Repo

| File/Folder | Purpose |
|-------------|---------|
| `README.md` | This guide |
| `CLAUDE.md` | Template for Claude Code — customize for your project |
| `AGENTS.md` | Template for other AI tools (Codex, Droid, Cursor, etc.) |
| `.gitignore` | Tells Git which files to ignore |
| `scripts/` | Utility scripts and automation |
| `docs/` | Documentation and notes |
| `projects/` | Your project code |

---

## The Philosophy

These tools let you describe what you want in plain English and have AI write the code. The key insight: **you're not learning to code—you're learning to collaborate with something that codes.**

This guide avoids "always do XYZ" prescriptions. Instead, it teaches you the mental models and gives you the vocabulary to figure things out as you go.

---

## Part 1: Setting Up Your Environment

### What's a terminal?

The terminal is a text-based way to talk to your computer. Instead of clicking icons, you type commands. Every computer has one built in:

- **Mac**: Search for "Terminal" in Spotlight (Cmd + Space)
- **Windows**: Search for "PowerShell" (recommended over Command Prompt—more modern and the examples in this guide work better)
- **Linux**: You probably already know

The terminal feels like a black box at first. That's normal. You'll get comfortable.

### Pick a terminal (optional upgrade)

The built-in terminal works fine, but nicer options exist:

| If you want... | Try |
|----------------|-----|
| Something approachable with AI features | [Warp](https://www.warp.dev/) |
| Something fast and minimal | [Ghostty](https://ghostty.org/) |
| To skip the terminal entirely | Use an IDE (see below) |

**You don't need a fancy terminal to start.** The default works. Upgrade later if you want.

### Consider an IDE instead of (or alongside) the terminal

An IDE (Integrated Development Environment) shows your files, lets you edit them, and has a terminal built in—all in one window. Many people find this less intimidating than a standalone terminal.

Options:
- [VS Code](https://code.visualstudio.com/) — Free, popular, solid default
- [Cursor](https://cursor.com/) — VS Code fork with AI features baked in
- [Windsurf](https://codeium.com/windsurf) — Another AI-focused option

**Why this matters:** In an IDE, you can see your file structure, preview documents, and watch what the AI is doing. In a standalone terminal, you're typing into a void.

### Install the tool

**Claude Code** (Anthropic):
```bash
npm install -g @anthropic-ai/claude-code
```

**Codex CLI** (OpenAI):
```bash
npm install -g @openai/codex
```

**Droid CLI** ([Factory](https://factory.ai)):
See [factory.ai](https://factory.ai) for install instructions. Droid makes it easy to experiment with different models, including open source ones.

If `npm` doesn't work, you need Node.js first. Download it from [nodejs.org](https://nodejs.org/) (get the LTS version), install it, then try the command again.

> **A note on models:** Model performance is constantly changing, and benchmarks don't tell the whole story. The best way to figure out what works for you is to try them yourself. Don't assume one tool is "best"—experiment and see what clicks.

> **Don't use `sudo`** with npm install commands, even if you get permission errors. It causes more problems than it solves. If you hit permission issues, search "npm permission error fix" for your OS.

---

## Part 2: The GitHub Foundation

### Why GitHub matters

Git is version control—a way to save checkpoints of your work that you can return to. GitHub is where those checkpoints live online.

Think of it like this: **every time you save a checkpoint, you create an "undo" button you can press days or weeks later.**

When working with AI coding tools, this is essential. The AI will sometimes break things. You need a safety net.

### Get set up

1. Create a [GitHub account](https://github.com/) if you don't have one
2. Install Git on your computer:
   - **Mac**: It's probably already there. Type `git --version` in terminal to check.
   - **Windows**: Download from [git-scm.com](https://git-scm.com/)
3. Configure Git with your identity:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

### Create your first project

Use this template to create a playground repository:

1. Go to [github.com/cresslank/how2claude](https://github.com/cresslank/how2claude)
2. Click the green **"Use this template"** button
3. Name it `scratch` (or whatever you want)
4. Click **"Create repository"**

### Clone it to your computer

"Cloning" downloads the repo to your machine so you can work on it locally.

```bash
# Mac/Linux
cd ~/Desktop
git clone https://github.com/YOUR-USERNAME/scratch.git
cd scratch

# Windows (PowerShell)
cd ~\Desktop
git clone https://github.com/YOUR-USERNAME/scratch.git
cd scratch
```

Now you have a folder on your computer that's connected to GitHub, with all the starter files ready to go.

### The five Git commands you actually need

These handle 90% of what you'll do:

| Command | What it does |
|---------|--------------|
| `git status` | Shows what's changed since your last checkpoint |
| `git add .` | Stages all changes for the next checkpoint |
| `git commit -m "description"` | Creates the checkpoint with a message |
| `git push` | Uploads your checkpoints to GitHub |
| `git pull` | Downloads any changes from GitHub |

**The habit to build:** Before asking the AI to do something significant, run `git add .` and `git commit -m "before AI changes"`. This gives you an instant undo button.

---

## Part 3: Your First AI Coding Session

### Start the tool

Navigate to your project folder and launch:

```bash
# Mac/Linux
cd ~/Desktop/scratch

# Windows (PowerShell)
cd ~\Desktop\scratch
```

Then launch your tool:
```bash
claude        # for Claude Code
codex         # for Codex CLI
droid         # for Droid CLI
```

The first time, you'll authenticate—follow the prompts.

### The core workflow

1. **Describe what you want** in plain English
2. **Watch** what the AI does
3. **Review** the changes
4. **Commit** if you're happy (or ask it to undo)
5. **Repeat**

That's it. The rest is refinement.

### Give context, not just commands

The most common mistake isn't being too vague—it's not giving the AI enough context to make good decisions.

**Weak prompt:**
> "Make a script that scrapes websites"

**Better prompt:**
> "I want to scrape product prices from e-commerce sites to track price changes over time. I'm thinking Python. Store the data in a CSV for now. It should handle basic errors like timeouts."

You're not writing specs—you're explaining your intent and constraints.

### Plan before you code

The more time you spend planning with the AI, the better the results.

Most AI coding tools have a "plan mode" where the AI thinks through the approach without writing code yet. Use it:

- **Claude Code**: Press `Shift+Tab` to cycle to plan mode
- **Codex**: Use "Ask" mode instead of "Code" mode
- **Droid**: Check the tool's documentation for planning features

Ask it to explain its approach. If you don't like the plan, redirect before it writes anything.

### Clear context between tasks

Each conversation accumulates context. When you switch to a new task, that old context can confuse things.

- **Claude Code**: `/clear` wipes the conversation
- **Codex / Droid**: Start a new session

**Rule of thumb:** One task per conversation. Clear when done.

---

## Part 4: The CLAUDE.md / AGENTS.md File

### What it is

Both tools look for a special markdown file in your project that tells them about your preferences, your project structure, and how you want them to behave.

- Claude Code looks for `CLAUDE.md`
- Codex looks for `AGENTS.md`

This file is your way of teaching the AI once so you don't have to repeat yourself.

### Create one

In your project folder, create the file:

```bash
touch CLAUDE.md  # or AGENTS.md for Codex
```

Or just ask the AI to create it:

> "Create a CLAUDE.md file for this project"

### What to put in it

Start minimal. Add things as you discover what you keep repeating.

```markdown
# Project Context

This is a [brief description of what you're building].

## About Me

I'm not a professional programmer. Please:
- Explain what you're doing and why
- Keep things simple when possible
- Ask clarifying questions before making big changes

## Commands

- `python main.py` - Run the main script
- `pip install -r requirements.txt` - Install dependencies

## Preferences

- Use Python 3.11+
- Prefer simple solutions over clever ones
- Write comments explaining non-obvious code
```

### The habit to build

Every time you explain something to the AI and think "I'll probably need to explain this again," add it to your CLAUDE.md. The file grows with you.

---

## Part 5: Project Structure

### Start with a folder per project

Don't dump everything into one place. Each thing you're building gets its own folder.

```
~/projects/
├── scratch/           # Your playground
├── budget-tracker/    # A real project
└── website-scraper/   # Another project
```

### Inside each project

A typical structure:

```
my-project/
├── CLAUDE.md          # AI instructions
├── README.md          # What this project is (for humans)
├── requirements.txt   # Python dependencies (if using Python)
├── .gitignore         # Files Git should ignore
└── src/               # Your actual code
    └── main.py
```

You don't need to create this manually. Ask the AI:

> "Set up a basic Python project structure for [what you're building]"

### The .gitignore file

Some files shouldn't be tracked by Git—things like:
- API keys and secrets
- Virtual environment folders
- Large data files
- System files (.DS_Store on Mac)

Create one:

```bash
touch .gitignore
```

Or ask the AI to generate one for your language/framework.

---

## Part 6: Python Specifics (if applicable)

Python is the most common language for beginners using AI coding tools. Here's the minimal setup.

### Virtual environments

A virtual environment keeps your project's dependencies separate from other projects. This prevents "it works on my machine" problems.

```bash
# Create a virtual environment
python -m venv venv

# Activate it
source venv/bin/activate      # Mac/Linux
# or
.\venv\Scripts\activate       # Windows

# Your prompt should now show (venv)
```

**Always activate your virtual environment before working on a project.**

### Requirements file

Track your dependencies so you (or someone else) can recreate the environment:

```bash
pip freeze > requirements.txt
```

To install from a requirements file:

```bash
pip install -r requirements.txt
```

### Ask the AI to handle this

You don't need to memorize this. Just tell the AI:

> "Set up a Python virtual environment and requirements.txt for this project"

---

## Part 7: Running and Testing

### Run your scripts

```bash
python main.py           # Run a Python script
node script.js           # Run a JavaScript file
```

### When things break

Copy the error message and paste it to the AI:

> "I got this error: [paste error]. What's wrong and how do I fix it?"

Error messages look scary but contain useful information. The AI is good at decoding them.

### Make a simple Makefile (optional)

If you find yourself typing the same commands repeatedly, a Makefile lets you create shortcuts.

```makefile
run:
	python main.py

install:
	pip install -r requirements.txt

test:
	python -m pytest
```

Then you just type `make run` instead of remembering the full command.

---

## Part 8: The Habits That Matter

### Before every AI request

1. Make sure you're in the right folder (`pwd` shows current directory)
2. Commit your current state: `git add . && git commit -m "checkpoint"`

### After the AI makes changes

1. Review what changed (use `git diff` or your IDE's diff viewer)
2. Test that it works
3. Commit if you're happy: `git add . && git commit -m "description of what changed"`

### When things go wrong

```bash
git checkout .           # Undo all uncommitted changes
# or
git reset --hard HEAD~1  # Undo the last commit entirely
```

### End of session

```bash
git push                 # Back up to GitHub
```

---

## Troubleshooting

### "command not found" errors

**`npm: command not found`**
You need Node.js. Download it from [nodejs.org](https://nodejs.org/) (get the LTS version), install it, restart your terminal, then try again.

**`git: command not found`**
- **Mac**: Run `xcode-select --install` in terminal
- **Windows**: Download from [git-scm.com](https://git-scm.com/) and install

**`claude: command not found`** (or codex/droid)
The tool didn't install correctly. Try:
```bash
npm install -g @anthropic-ai/claude-code
```
If that fails with permission errors, see below.

### Permission errors with npm

If you see `EACCES` or "permission denied" when installing:

**Don't use `sudo`.** It causes more problems than it solves.

Instead, fix npm's permissions:
```bash
mkdir -p ~/.npm-global
npm config set prefix '~/.npm-global'
```

Then add this to your shell config (`~/.zshrc` on Mac, `~/.bashrc` on Linux):
```bash
export PATH=~/.npm-global/bin:$PATH
```

Restart your terminal and try the install again.

**On Windows:** Run PowerShell as Administrator, or use [nvm-windows](https://github.com/coreybutler/nvm-windows) to manage Node.

### Git says "fatal: not a git repository"

You're not inside a Git project folder. Either:
- `cd` into your project folder first
- Or you forgot to clone/init a repo

### Git says "Please tell me who you are"

Git needs your identity for commits:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### The AI made a mess of my code

This is why we use Git. Undo everything since your last commit:
```bash
git checkout .
```

Or if you already committed the mess:
```bash
git reset --hard HEAD~1
```

### Authentication isn't working

- **Claude Code**: It opens a browser to authenticate. Make sure pop-ups aren't blocked. If stuck, try `claude logout` then `claude` again.
- **Codex/Droid**: Check that you're logged into the correct account in your browser.

### Something else is broken

1. Copy the exact error message
2. Paste it to the AI tool and ask what's wrong
3. Or search the error message online—someone else has hit it before

---

## Quick Reference

### Commands you'll use constantly

```bash
# Navigation
cd folder-name          # Enter a folder
cd ..                   # Go up one level
pwd                     # Show current location (Mac/Linux/PowerShell)
ls                      # List files (Mac/Linux)
dir                     # List files (Windows CMD)
ls                      # Also works in PowerShell

# Git
git status              # What's changed?
git add .               # Stage everything
git commit -m "msg"     # Create checkpoint
git push                # Upload to GitHub
git pull                # Download from GitHub

# AI tools
claude                  # Start Claude Code
codex                   # Start Codex CLI
droid                   # Start Droid CLI
/clear                  # Clear conversation (Claude Code)
/init                   # Generate CLAUDE.md from codebase
```

### Keyboard shortcuts (Claude Code)

| Shortcut | Action |
|----------|--------|
| `Shift+Tab` | Cycle between modes (plan/code) |
| `Escape` | Stop the AI mid-action |
| `Escape` (twice) | Jump back in conversation history |
| `Ctrl+V` | Paste images (not Cmd+V on Mac) |

---

## Resources

**Official docs:**
- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Codex Documentation](https://developers.openai.com/codex/)
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)

**Good guides:**
- [Anthropic's Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [Git for Vibe Coders](https://deepakness.com/blog/git-for-vibe-coders/)
- [Claude Code for Non-Technical Users](https://hannahstulberg.substack.com/p/skip-the-terminal-and-8-other-claude)

**Community:**
- [r/ClaudeAI](https://reddit.com/r/ClaudeAI)
- [ClaudeLog](https://claudelog.com/) — Community best practices

---

## The Mindset

You're not trying to become a programmer. You're learning to collaborate with a very fast, very literal assistant that happens to write code.

The AI is like an eager junior employee: technically capable, but needs clear direction. Your job is to:

1. Know what you want (roughly)
2. Communicate it clearly
3. Review the work
4. Course-correct as needed

Start small. Build something trivial. Break it. Fix it. The confidence comes from doing, not from reading guides like this one.

Now go create something.
# Getting Started

This doc gets you set up and comfortable with the terminal and tools.

## Find your terminal

The terminal is a text-based way to talk to your computer. Instead of clicking icons,
you type commands. Every computer has one built in.

### macOS

1. Press `Cmd + Space` to open Spotlight (a search bar appears in the center of your screen)
2. Type `Terminal`
3. Press Enter

A window will open with a blinking cursor. This is your terminal.

### Windows

1. Click the Start button (Windows icon in the bottom-left corner, or press the Windows key)
2. Type `PowerShell`
3. Click "Windows PowerShell" (not "Windows PowerShell ISE")

A blue window will open with a blinking cursor. This is your terminal. Use PowerShell,
not Command Prompt - the commands in this guide work better in PowerShell.

### Linux

Open your terminal application. If you are on Linux, you likely already know how to do this.
Common shortcuts: `Ctrl+Alt+T` on Ubuntu, or search for "Terminal" in your app menu.

---

The terminal feels like a black box at first. That is normal. You will get comfortable.

## Work computers: what you can and cannot install

If you are using a work computer, you may have restrictions on what software you can install.

**Check with your IT department first.** Many organizations have policies about:
- Installing software from the internet
- Running commands that modify system settings
- Using AI tools that may process company data

If you cannot install software freely, ask IT about:
- Getting an exception for developer tools (Node.js, Git, VS Code)
- Using a virtual machine or container where you have more control
- Whether there are pre-approved tools you can use

If you are experimenting and want to avoid any issues, **use a personal computer** until
you understand what you are doing and can have a conversation with IT about your needs.

## Terminal basics

Once you have a terminal open, here are five commands that do most of what you need:

```bash
pwd          # Show where you are (print working directory)
ls           # List files here
cd folder    # Move into a folder
cd ..        # Go up one folder
mkdir test   # Make a new folder called "test"
```

Use the quick reference when you need it:
[Quick Reference](quick-reference.md)

## If the terminal feels intimidating

The built-in terminal works fine, but friendlier options exist:

- [Warp](https://www.warp.dev/) - helpful UI and AI features (macOS, Linux)
- [Ghostty](https://ghostty.org/) - fast and minimal

These are nice-to-haves, not requirements. Start with the built-in terminal.

## Consider an IDE alongside the terminal

An IDE (Integrated Development Environment) shows your files, lets you edit them, and has
a terminal built in - all in one window. Many people find this less intimidating than a
standalone terminal.

Options:
- [VS Code](https://code.visualstudio.com/) (free, popular)
- [Cursor](https://cursor.com/) (VS Code with AI features)
- [Windsurf](https://codeium.com/windsurf) (AI-focused)

A common beginner setup is: IDE + terminal together. Use the terminal for commands and the
IDE to see and edit files.

## Choose your operating system

Short checklists by operating system. Pick the one that matches your computer.

### macOS quick path
1. Open Terminal (Spotlight -> "Terminal").
2. Check Git: `git --version` (install if prompted).
3. Install Node.js (LTS): [nodejs.org](https://nodejs.org/)
4. Check Python: `python3 --version`. If not installed, download from [python.org](https://www.python.org/downloads/)
5. Install your AI tool (see next section).
6. Create your project from this template: [Create Your Project](project-setup.md)

### Windows quick path
1. Open PowerShell.
2. Install Git: [git-scm.com](https://git-scm.com/)
3. Install Node.js (LTS): [nodejs.org](https://nodejs.org/)
4. Install Python: [python.org](https://www.python.org/downloads/) - check "Add Python to PATH" during install
5. Install your AI tool (see next section).
6. Create your project from this template: [Create Your Project](project-setup.md)

### Linux quick path
1. Open your terminal.
2. Install Git with your package manager (or check `git --version`).
3. Install Node.js (LTS) from [nodejs.org](https://nodejs.org/) or your package manager.
4. Check Python: `python3 --version`. Install via your package manager if needed.
5. Install your AI tool (see next section).
6. Create your project from this template: [Create Your Project](project-setup.md)

**After installing:** Close and reopen your terminal before continuing. New programs often
will not be recognized until you do this.

## Install the tool

Only install the tool you plan to use right now. You can add the others later.

The install commands below use `npm`, which is a package manager that comes with Node.js.
If you installed Node.js in the previous step, you have npm.

### Claude Code (Anthropic)

Requires a Claude Pro subscription ($20/month).

```bash
npm install -g @anthropic-ai/claude-code
```

### Codex CLI (OpenAI)

Requires a ChatGPT Plus subscription ($20/month).

```bash
npm install -g @openai/codex
```

### Droid CLI (Factory)

Has a **free tier** - good for experimenting before committing to a subscription.
Also supports multiple AI models including open source options.

**A note on `curl | sh`:** The command below downloads a script and runs it immediately.
This is common for developer tools but worth understanding: you are trusting the source
to not do anything harmful. For the tools in this guide, this is fine - they are from
known companies and the install scripts do standard things. But as you get more ambitious
and start running code from less familiar sources, the risk increases. When in doubt,
download the script first (`curl -fsSL https://example.com/script > install.sh`), read it,
then run it (`sh install.sh`).

```bash
# macOS/Linux
curl -fsSL https://app.factory.ai/cli | sh

# macOS (Homebrew)
brew install --cask droid

# Windows (PowerShell)
irm https://app.factory.ai/cli/windows | iex
```

Linux users also need: `sudo apt-get install xdg-utils`

### If npm does not work

You need Node.js first. Download the LTS version from [nodejs.org](https://nodejs.org/),
install it, restart your terminal, then try the install command again.

Do not use `sudo` with npm install commands. If you hit permission errors, see:
[Troubleshooting](troubleshooting.md)

### Note on models and pricing

Model performance changes often, and benchmarks do not tell the whole story. Try a few
and see what works for you.

If you want to experiment before paying for a subscription, start with Droid's free tier.

## Advanced: other options

This section is for people who want more control or want to avoid subscription costs.
**If you are just starting out, skip this section.** Come back when you are comfortable
with the basics.

**Other CLI tools:**
- [opencode](https://github.com/anomalyco/opencode) - open source alternative
- [aider](https://aider.chat/) - works with many AI providers

**Using APIs directly:**
If you have programming experience, you can use AI provider APIs directly. Many offer
free tiers or credits:
- Anthropic API (Claude)
- OpenAI API
- Google Gemini API
- Various open source models via Hugging Face, Ollama, etc.

**Local models:**
You can run AI models entirely on your own computer using tools like Ollama. This is
free but requires a capable machine and more technical setup.

These options give you more flexibility but require more configuration. The tools
recommended above (Claude Code, Codex, Droid) are designed to work out of the box.

---
<!-- nav -->
Next: [Create Your Project](project-setup.md)

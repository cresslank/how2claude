# Getting Started

This doc gets you set up and comfortable with the terminal and tools.

## Terminal basics (start here)

If the terminal is new or intimidating, start with these five commands:

```bash
pwd          # Show where you are
ls           # List files here
cd folder    # Move into a folder
cd ..        # Go up one folder
mkdir test   # Make a new folder called "test"
```

You do not need to memorize these. Use the quick reference when you need it:
[Quick Reference](quick-reference.md)

## If the terminal feels intimidating

You can stick with the built-in terminal, or try a friendlier one:

- [Warp](https://www.warp.dev/) - helpful UI and AI features (optional)
- [Ghostty](https://ghostty.org/) - fast and minimal (optional)

These are nice-to-haves, not requirements.

## What's a terminal?

The terminal is a text-based way to talk to your computer. Instead of clicking icons,
you type commands. Every computer has one built in:

- macOS: Search for "Terminal" in Spotlight (Cmd + Space)
- Windows: Search for "PowerShell" (recommended over Command Prompt)
- Linux: You probably already know

The terminal feels like a black box at first. That is normal. You will get comfortable.

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

## Choose your OS path

If you want a short, OS-specific checklist, use the one that matches your computer.

### macOS quick path
1. Open Terminal (Spotlight -> "Terminal").
2. Check Git: `git --version` (install if prompted).
3. Install Node.js (LTS): [nodejs.org](https://nodejs.org/)
4. Install your AI tool (see next section).
5. Create your project from this template: [Create Your Project](project-setup.md)

### Windows quick path
1. Open PowerShell.
2. Install Git: [git-scm.com](https://git-scm.com/)
3. Install Node.js (LTS): [nodejs.org](https://nodejs.org/)
4. Install your AI tool (see next section).
5. Create your project from this template: [Create Your Project](project-setup.md)

### Linux quick path
1. Open your terminal.
2. Install Git with your package manager (or check `git --version`).
3. Install Node.js (LTS) from [nodejs.org](https://nodejs.org/) or your package manager.
4. Install your AI tool (see next section).
5. Create your project from this template: [Create Your Project](project-setup.md)

## Install the tool

Only install the tool you plan to use right now. You can add the others later.

Claude Code (Anthropic):
```bash
npm install -g @anthropic-ai/claude-code
```

Codex CLI (OpenAI):
```bash
npm install -g @openai/codex
```

Droid CLI (Factory):
```bash
# macOS/Linux
curl -fsSL https://app.factory.ai/cli | sh

# macOS (Homebrew)
brew install --cask droid

# Windows (PowerShell)
irm https://app.factory.ai/cli/windows | iex
```

Linux users also need: `sudo apt-get install xdg-utils`

If `npm` does not work, you need Node.js first. Download the LTS version from
[nodejs.org](https://nodejs.org/), install it, then try the command again.

Note on models: Model performance changes often, and benchmarks do not tell the whole
story. Try a few models and see what works for you.

Do not use `sudo` with npm install commands. If you hit permission errors, see the
Troubleshooting guide: [Troubleshooting](troubleshooting.md)

---
<!-- nav -->
Previous: [Why This Setup](why-this-setup.md)
Next: [Create Your Project](project-setup.md)

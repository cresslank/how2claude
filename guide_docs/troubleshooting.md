# Troubleshooting

## "command not found" errors

`npm: command not found`
You need Node.js. Download the LTS version from [nodejs.org](https://nodejs.org/), install it, restart
your terminal, then try again.

`git: command not found`
- macOS: Run `xcode-select --install` in terminal
- Windows: Download from [git-scm.com](https://git-scm.com/)

`claude: command not found` (or codex/droid)
The tool did not install correctly. Try:
```bash
npm install -g @anthropic-ai/claude-code
```
If that fails with permission errors, see below.

## Permission errors with npm

If you see EACCES or "permission denied" when installing:

Do not use `sudo`. It causes more problems than it solves.

Instead, fix npm's permissions:
```bash
mkdir -p ~/.npm-global
npm config set prefix '~/.npm-global'
```

Then add this to your shell config (`~/.zshrc` on macOS, `~/.bashrc` on Linux):
```bash
export PATH=~/.npm-global/bin:$PATH
```

Restart your terminal and try the install again.

On Windows: Run PowerShell as Administrator, or use nvm-windows to manage Node.

## Git says "fatal: not a git repository"

You are not inside a Git project folder. Either:
- `cd` into your project folder first, or
- you forgot to clone or init a repo

## Git says "Please tell me who you are"

Git needs your identity for commits:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## The AI made a mess of my code

This is why we use Git. Undo everything since your last commit:
```bash
git checkout .           # This deletes uncommitted changes
```

Or if you already committed the mess:
```bash
git reset --hard HEAD~1  # This deletes that commit
```

If you want to keep a copy before undoing, ask the AI to help you make a backup first.

## Authentication isn't working

- Claude Code: It opens a browser to authenticate. Make sure pop-ups are not blocked. If stuck,
  try `claude logout` then `claude` again.
- Codex/Droid: Check that you are logged into the correct account in your browser.

## Something else is broken

1. Copy the exact error message.
2. Paste it to the AI tool and ask what is wrong.
3. Or search the error message online - someone else has hit it before.

---
<!-- nav -->
Previous: [Running and Testing](running-testing.md)
Next: [Quick Reference](quick-reference.md)

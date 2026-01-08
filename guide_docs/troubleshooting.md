# Troubleshooting

## When you are stuck

If something is not working and you are not sure why, try these steps in order:

### 1. Start fresh

Open a new terminal window or tab. Sometimes the current session is in a weird state
(wrong folder, environment variables not loaded, etc.). A fresh terminal resets this.

In the new terminal, navigate to your project folder:
```bash
cd ~/Desktop/your-project-name
```

### 2. Start a new AI session

If the AI seems confused or is giving strange responses, start over:

- **Claude Code**: Type `/clear` to wipe the conversation, or quit (`Ctrl+D`) and restart
- **Codex / Droid**: Quit and start a new session

The AI can get confused by long conversations or accumulated context. A fresh session
often helps.

### 3. Describe what happened

If things are still broken, explain the problem to the AI:

```
I tried to [what you were trying to do].
I ran [the command you ran].
I got this error: [paste the full error message].
What went wrong?
```

Copy the full error message - the whole thing, not just the last line. Error messages
often contain useful information earlier in the output.

### 4. Check where you are

Many problems come from being in the wrong folder. Check your location:

```bash
pwd                     # Shows current folder
ls                      # Shows files here
```

If you do not see your project files, you are in the wrong place. Navigate to your project:

```bash
cd ~/Desktop/your-project-name
```

---

## Common confusion

### "I ran a command but nothing happened"

This often means it worked. Many commands produce no output on success - silence means
everything is fine. Check for results:

- If you ran a Python script: look for new files, or check if it printed anything
- If you ran a git command: run `git status` to see what changed
- If you ran an install command: try the thing you were installing

### "The AI created a file but I cannot find it"

The file is in your current project folder. Check:

```bash
ls                      # List all files in current folder
ls -la                  # Include hidden files
```

If you are using an IDE, the file browser might not auto-refresh. Click the refresh icon
or look in Finder/Explorer directly.

### "Where is my project folder?"

When you cloned the repo, it created a folder wherever you were at the time. Common
locations:

- `~/Desktop/your-project-name` (if you were on the Desktop)
- `~/your-project-name` (if you were in your home folder)
- `~/Documents/your-project-name`

Use Finder (macOS) or Explorer (Windows) to search for the folder name.

### "The AI keeps making the same mistake"

The AI might be stuck in a pattern. Try:

1. Clear the conversation (`/clear` in Claude Code, or start a new session)
2. Be more explicit about what is wrong: "Do not do X. Instead do Y."
3. Add the instruction to your CLAUDE.md so it remembers next time

---

## Specific errors

### "command not found"

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

### Permission errors with npm

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

### Git says "fatal: not a git repository"

You are not inside a Git project folder. Either:
- `cd` into your project folder first, or
- you forgot to clone or init a repo

### Git says "Please tell me who you are"

Git needs your identity for commits:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### The AI made a mess of my code

This is why we use Git. Undo everything since your last commit:
```bash
git checkout .           # This deletes uncommitted changes
```

Or if you already committed the mess:
```bash
git reset --hard HEAD~1  # This deletes that commit
```

If you want to keep a copy before undoing, ask the AI to help you make a backup first.

### Authentication is not working

- Claude Code: It opens a browser to authenticate. Make sure pop-ups are not blocked. If stuck,
  try `claude logout` then `claude` again.
- Codex/Droid: Check that you are logged into the correct account in your browser.

### Something else is broken

1. Copy the exact error message.
2. Paste it to the AI tool and ask what is wrong.
3. Or search the error message online - someone else has hit it before.

---
<!-- nav -->
Previous: [Running and Testing](running-testing.md)
Next: [Quick Reference](quick-reference.md)

# Quick Reference

## Navigation commands by platform

| Action | macOS / Linux | Windows PowerShell | Windows CMD |
|--------|---------------|-------------------|-------------|
| Show current location | `pwd` | `pwd` | `cd` (no args) |
| List files | `ls` | `ls` or `dir` | `dir` |
| Enter folder | `cd folder` | `cd folder` | `cd folder` |
| Go up one level | `cd ..` | `cd ..` | `cd ..` |

## Git commands

| Command | What it does |
|---------|--------------|
| `git status` | What changed? |
| `git add .` | Stage everything |
| `git commit -m "msg"` | Create checkpoint |
| `git push` | Upload to GitHub |
| `git pull` | Download from GitHub |

## AI tool commands

| Command | What it does |
|---------|--------------|
| `claude` | Start Claude Code |
| `codex` | Start Codex CLI |
| `droid` | Start Droid CLI |
| `/clear` | Clear conversation (Claude Code) |
| `/init` | Generate CLAUDE.md from codebase |

## Keyboard shortcuts (Claude Code)

| Shortcut | Action |
|----------|--------|
| `Ctrl+C` | Cancel current generation |
| `Ctrl+D` | Exit Claude Code |
| `Ctrl+L` | Clear terminal screen (keeps conversation) |
| `Ctrl+O` | Toggle verbose output |
| `Ctrl+R` | Reverse search command history |
| `Ctrl+V` (macOS/Linux) or `Alt+V` (Windows) | Paste image from clipboard |
| `Up/Down` arrows | Navigate command history |
| `Esc` twice | Rewind conversation to previous point |
| `Shift+Tab` | Cycle permission modes (Auto-Accept / Plan / Normal) |
| `Option+P` (macOS) or `Alt+P` (Windows/Linux) | Switch model without clearing prompt |
| `Ctrl+B` | Move Bash command to background |
| `\ + Enter` | Multiline input (works in all terminals) |

## Prefix shortcuts

| Prefix | Action |
|--------|--------|
| `/` | Slash commands (e.g., `/clear`, `/init`) |
| `!` | Bash mode (run shell command directly) |
| `@` | File path autocomplete |

---

## Level up: terminal navigation

This section is optional. The basics above are enough to get started. Come back here
when you want more fluency.

### See more with ls

```bash
ls -la              # Show all files (including hidden) with details
ls -lah             # Same, but with human-readable file sizes
ls *.py             # List only Python files
ls -lt              # Sort by modification time (newest first)
```

### Visualize your file tree

The `tree` command shows your folder structure visually. It is not installed by default.

```bash
# Install tree
brew install tree          # macOS
sudo apt install tree      # Ubuntu/Debian

# Use it
tree                       # Show entire tree
tree -L 2                  # Only go 2 levels deep
tree -L 2 -I node_modules  # Ignore node_modules folder
```

**eza** is a modern replacement for `ls` and `tree` with better defaults and colors:

```bash
# Install eza
brew install eza           # macOS
sudo apt install eza       # Ubuntu/Debian (newer versions)

# Use it
eza                        # Better ls
eza -la                    # All files with details
eza -T                     # Tree view
eza -TL 2                  # Tree view, 2 levels deep
eza -TL 2 --git-ignore     # Tree view, respecting .gitignore
```

### Keyboard tricks that save time

| Trick | What it does |
|-------|--------------|
| `Tab` | Autocomplete file/folder names (press twice to see options) |
| `Up arrow` | Previous command |
| `Ctrl+R` | Search command history (type to search, Enter to run) |
| `Ctrl+C` | Cancel current command |
| `Ctrl+L` | Clear screen (keeps history) |
| `cd -` | Go back to previous folder |
| `cd ~` | Go to home folder |

### Useful aliases

If you find yourself typing the same commands repeatedly, you can create shortcuts.
Add these to your shell config file (`~/.zshrc` on macOS, `~/.bashrc` on Linux):

```bash
alias ll='ls -la'
alias la='ls -la'
alias ..='cd ..'
alias ...='cd ../..'
```

After editing, run `source ~/.zshrc` (or restart your terminal) to apply.

---
<!-- nav -->
Previous: [Troubleshooting](troubleshooting.md)
Next: [Resources](resources.md)

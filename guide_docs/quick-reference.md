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
<!-- nav -->
Previous: [Troubleshooting](troubleshooting.md)
Next: [Resources](resources.md)

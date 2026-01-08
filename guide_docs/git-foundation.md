# The GitHub Foundation

## Why GitHub matters

Git is version control - a way to save checkpoints of your work that you can return to.
GitHub is where those checkpoints live online.

Think of it like this: every time you save a checkpoint, you create an "undo" button you
can press days or weeks later.

When working with AI coding tools, this is essential. The AI will sometimes break things.
You need a safety net.

## Get set up

1. Create a GitHub account: [github.com](https://github.com/)
2. Install Git:
   - macOS: It is probably already there. Type `git --version` in terminal to check.
   - Windows: Download from [git-scm.com](https://git-scm.com/)
3. Configure Git with your identity:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

## Create your first project

Use the template instructions here:
[Create Your Project](project-setup.md)

## The five Git commands you actually need

These handle 90 percent of what you will do:

| Command | What it does |
|---------|--------------|
| `git status` | Shows what has changed since your last checkpoint |
| `git add .` | Stages all changes for the next checkpoint |
| `git commit -m "description"` | Creates the checkpoint with a message |
| `git push` | Uploads your checkpoints to GitHub |
| `git pull` | Downloads any changes from GitHub |

Habit to build: Before asking the AI to do something significant, run
`git add .` and `git commit -m "before AI changes"`. This gives you an instant undo button.

## First-time `git push` authentication (common blocker)

When you run `git push` for the first time, GitHub will ask you to authenticate. Short walkthrough:

1. Run `git push`.
2. If prompted to sign in, choose one of these options:
   - GitHub Desktop (most beginner-friendly): [desktop.github.com](https://desktop.github.com/)
   - GitHub CLI: install `gh`, then run `gh auth login` - [cli.github.com](https://cli.github.com/)
   - Personal Access Token (PAT): create a token and use it as your password when prompted -
     [github.com/settings/tokens](https://github.com/settings/tokens)
3. Run `git push` again.

If you get stuck, paste the exact error into your AI tool and ask for help.

---
<!-- nav -->
Previous: [Create Your Project](project-setup.md)
Next: [Project Structure and Instructions](project-structure.md)

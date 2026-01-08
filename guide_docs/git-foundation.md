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

## Keep your repo private and safe

When you create a repo on GitHub, you can choose **Public** or **Private**.

**Make it private by default.** Unless you specifically want to share your code with the
world, private repos keep your work visible only to you. You can always make it public later.

**Never commit sensitive information**, even to private repos:
- Passwords and API keys
- Social security numbers, credit card numbers, personal data
- `.env` files with secrets
- Private keys and certificates

If you accidentally commit something sensitive, deleting it in a later commit is not enough -
it remains in the git history. Contact GitHub support or use tools like `git filter-branch`
to remove it properly. Better to never commit it in the first place.

The `.gitignore` file in this template already excludes common sensitive files (`.env`,
`*.pem`, `secrets/`, etc.). Check it before committing.

## GitHub enables more than backup

GitHub is not just for saving your work. Once your code is on GitHub, you can:

**Work from anywhere.** Start a project on your laptop, push to GitHub, then pull it down
on another computer and continue. Your terminal, your IDE, your files - all in sync.

**Use Claude on the web or mobile.** Claude Code can sync conversations between your local
terminal and claude.ai. Start a conversation locally, push your code to GitHub, then continue
the conversation on your phone or in a browser. The AI can see your repo and understand what
you were working on.

To enable this:
1. Push your code to GitHub (`git push`)
2. Go to claude.ai and start a new conversation
3. Mention your GitHub repo or connect it when prompted

This is why GitHub matters beyond just backup - it is the bridge between your local work
and everywhere else you might want to continue.

## Advanced: branches and pull requests

This section is for when you are comfortable with the basics and want more control.
**Skip this if you are just starting out.**

So far, you have been pushing directly to `main` - the default branch. This works fine
for solo projects. But branches let you:

- Experiment without affecting your working code
- Work on multiple features at once
- Review changes before merging them

### Create a branch

```bash
git checkout -b my-experiment      # Create and switch to a new branch
# ... make changes ...
git add .
git commit -m "Try a new approach"
git push -u origin my-experiment   # Push the branch to GitHub
```

### Merge back to main

When you are happy with the changes:

```bash
git checkout main                  # Switch back to main
git merge my-experiment            # Merge your branch into main
git push                           # Push the updated main
git branch -d my-experiment        # Delete the branch (optional)
```

### Pull requests

On GitHub, you can create a **pull request** instead of merging directly. This lets you:
- Review the changes in a web interface
- Add comments and discussion
- Have others review before merging (useful for teams)

To create a pull request:
1. Push your branch to GitHub
2. Go to your repo on github.com
3. Click "Compare & pull request"
4. Review the changes and click "Create pull request"
5. When ready, click "Merge pull request"

For solo work, merging directly is fine. Pull requests are more useful when collaborating
or when you want a clear record of why changes were made.

---
<!-- nav -->
Previous: [Create Your Project](project-setup.md)
Next: [Project Structure and Instructions](project-structure.md)

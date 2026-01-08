# Project Structure and Instructions

## The CLAUDE.md file

AI coding tools look for a special markdown file in your project that tells them about your
preferences, your project structure, and how you want them to behave.

- Claude Code looks for `CLAUDE.md`
- Other tools (Codex, Cursor, Windsurf) look for `AGENTS.md`

This template uses `CLAUDE.md` as the main instructions file. The `AGENTS.md` file simply
points to `CLAUDE.md`, so you only need to maintain one file.

### Edit CLAUDE.md for your project

The template includes a `CLAUDE.md` with starter content. Edit it to describe what you are
building and how you want the AI to behave.

You do not need to touch `AGENTS.md` - it automatically redirects other tools to `CLAUDE.md`.

### The key sections

**About This Project** - What you are building, in a sentence or two.

**About Me** - Your context. Are you a beginner? Do you have preferences about languages
or frameworks?

**What I Want Claude to Do** - Things that work well for you. Add to this when the AI does
something helpful that you want it to keep doing. For example:
- Explain what you are doing and why
- Tell me when a request is more complex than it sounds
- Ask questions before starting large tasks

**What I Don't Want Claude to Do** - Things that annoy you. Add to this when the AI does
something you dislike. For example:
- Don't comment out code - delete it instead
- Don't create extra markdown files unless I ask
- Don't over-engineer or add features I didn't request

**Notes** - Project-specific things to remember, like API limits or file locations.

### The habit to build

Start with the template as-is. Then:
- Every time the AI does something you like, add it to "What I Want."
- Every time the AI does something annoying, add it to "What I Don't Want."
- Every time you explain something and think "I'll probably say this again," add it to Notes.

The file becomes a record of your preferences and grows with you.

## Start with a folder per project

Do not dump everything into one place. Each thing you are building gets its own folder.

```
~/projects/
|-- scratch/           # Your playground
|-- budget-tracker/    # A real project
`-- website-scraper/   # Another project
```

## Inside each project

A typical structure:

```
my-project/
|-- CLAUDE.md          # AI instructions (edit this one)
|-- AGENTS.md          # Points other tools to CLAUDE.md
|-- README.md          # What this project is (for humans)
|-- requirements.txt   # Python dependencies (if using Python)
|-- .gitignore         # Files Git should ignore
`-- src/               # Your actual code
    `-- main.py
```

You do not need to create this manually. Ask the AI:
"Set up a basic Python project structure for [what you're building]"

## The .gitignore file

Some files should not be tracked by Git - things like:
- API keys and secrets
- Virtual environment folders
- Large data files
- System files (.DS_Store on Mac)

This template already includes a `.gitignore`. Edit it if you need to add more exclusions.

## The habits that matter

Before every AI request:
1. Make sure you are in the right folder (`pwd` shows current directory).
2. Commit your current state: `git add . && git commit -m "checkpoint"`

After the AI makes changes:
1. Review what changed (use `git diff` or your IDE's diff viewer).
2. Test that it works.
3. Commit if you are happy: `git add . && git commit -m "description of what changed"`

End of session:
```bash
git push  # Back up to GitHub
```

---
<!-- nav -->
Previous: [The GitHub Foundation](git-foundation.md)
Next: [Your First AI Session](first-session.md)

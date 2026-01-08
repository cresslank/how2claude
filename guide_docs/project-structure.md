# Project Structure and Instructions

## The CLAUDE.md file

AI coding tools look for a special markdown file in your project that tells them about your
preferences, your project structure, and how you want them to behave.

- Claude Code looks for `CLAUDE.md`
- Other tools (Codex, Cursor, Windsurf) look for `AGENTS.md`

This template uses `CLAUDE.md` as the main instructions file. The `AGENTS.md` file simply
points to `CLAUDE.md`, so you only need to maintain one file.

### Edit CLAUDE.md

This template already includes `CLAUDE.md` with a starter template. Edit it to describe
your project, your preferences, and any notes you want the AI to remember.

You do not need to touch `AGENTS.md` - it automatically redirects other tools to `CLAUDE.md`.

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

Every time you explain something to the AI and think "I'll probably need to explain this again,"
add it to your CLAUDE.md. The file grows with you.

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

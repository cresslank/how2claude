# Python Basics (if applicable)

Python is the most common language for beginners using AI coding tools. Here is the minimal setup.

## Virtual environments

A virtual environment keeps your project's dependencies (other packages your code needs
to run) separate from other projects. This prevents "it works on my machine" problems.

```bash
# Create a virtual environment
python -m venv venv

# Activate it
source venv/bin/activate      # macOS/Linux
# or
.\venv\Scripts\activate       # Windows

# Your prompt should now show (venv)
```

Always activate your virtual environment before working on a project.

## Requirements file

Track your dependencies so you (or someone else) can recreate the environment:

```bash
pip freeze > requirements.txt
```

To install from a requirements file:

```bash
pip install -r requirements.txt
```

## Ask the AI to handle this

Just tell the AI:
"Set up a Python virtual environment and requirements.txt for this project"

---
<!-- nav -->
Previous: [Your First AI Session](first-session.md)
Next: [Running and Testing](running-testing.md)

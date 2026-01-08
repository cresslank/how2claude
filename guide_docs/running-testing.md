# Running and Testing

## Run your scripts

```bash
python main.py           # Run a Python script
node script.js           # Run a JavaScript file
```

## When things break

Copy the error message and paste it to the AI:
"I got this error: [paste error]. What's wrong and how do I fix it?"

Error messages look scary but contain useful information. The AI is good at decoding them.

## Make a simple Makefile (optional)

If you find yourself typing the same commands repeatedly, a Makefile lets you create shortcuts.

```makefile
run:
	python main.py

install:
	pip install -r requirements.txt

test:
	python -m pytest
```

Then you just type `make run` instead of remembering the full command.

Note: `make` is not installed by default on Windows. If you are on Windows, you can skip
this or use WSL.

---
<!-- nav -->
Previous: [Python Basics](python-basics.md)
Next: [Troubleshooting](troubleshooting.md)

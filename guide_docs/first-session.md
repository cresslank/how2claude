# Your First AI Coding Session

## Start the tool

Navigate to your project folder and launch:

```bash
# macOS/Linux
cd ~/Desktop/your-project-name   # Use whatever you named your repo

# Windows (PowerShell)
cd ~\Desktop\your-project-name   # Use whatever you named your repo
```

Then launch your tool:
```bash
claude        # for Claude Code
codex         # for Codex CLI
droid         # for Droid CLI
```

The first time, you will authenticate - follow the prompts.

## The core workflow

1. Describe what you want in plain English.
2. Watch what the AI does.
3. Review the changes.
4. Commit if you are happy (or ask it to undo).
5. Repeat.

## Give context, not just commands

The most common mistake is not giving the AI enough context.

Weak prompt:
"Make a script that scrapes websites"

Better prompt:
"I want to scrape product prices from e-commerce sites to track price changes over time.
I'm thinking Python. Store the data in a CSV for now. It should handle basic errors like timeouts."

You are not writing specs - you are explaining your intent and constraints.

## Plan before you code

The more time you spend planning with the AI, the better the results.

Most AI coding tools have a plan mode where the AI thinks through the approach without
writing code yet. Use it:

- Claude Code: Press `Shift+Tab` to cycle to plan mode
- Codex: Use "Ask" mode instead of "Code" mode
- Droid: Check the tool's documentation for planning features

Ask it to explain its approach. If you do not like the plan, redirect before it writes anything.

## Clear context between tasks

Each conversation accumulates context. When you switch to a new task, that old context
can confuse things.

- Claude Code: `/clear` wipes the conversation
- Codex / Droid: Start a new session

Rule of thumb: One task per conversation. Clear when done.

## A first exercise: inflation data

This walkthrough takes you through a complete cycle: ask the AI to build something, save your
work, and run it. There are many ways to do each step. This is one path that works.

**A note on where you type things:** There are two places you will type during this exercise:
- **The AI chat** - where you talk to Claude/Codex/Droid (prompts and questions go here)
- **The terminal** - where you run commands like `python` or `git` (commands go here)

If you are using an IDE, you likely have both visible: the AI tool in one panel, the terminal
in another. If not, you can switch between them.

### Step 1: Ask for something real

In the AI chat, type this prompt:

```
Download US inflation data from FRED (the Federal Reserve's public data) and create
a chart showing how inflation has changed over time. Save the chart as a PNG file.
Use Python. Keep it simple.
```

FRED provides free CSV downloads without an API key. The AI will likely use the Consumer
Price Index (CPI) dataset.

### Step 2: Watch and check

The AI will start working. Watch for these things:

1. **What file is it creating?** Look for something like "Creating `inflation_chart.py`" or
   similar. Remember this filename - you will need it to run the script.

2. **What libraries is it using?** You might see `matplotlib`, `pandas`, `requests`, etc.
   These are Python libraries. If you do not have them installed, Step 4 will fail - that
   is fine, you will fix it then.

3. **Where is it getting the data?** Look for a URL. It should be something like
   `fred.stlouisfed.org`. This is real government data.

**If something looks wrong, say so now.** For example:
- "Wait, I want this to show monthly data, not yearly"
- "Can you explain what that library does before using it?"
- "I'd rather use a bar chart instead of a line chart"

You can interrupt and redirect at any point. The AI will adjust.

### Step 3: Save your work

Before running anything, save a checkpoint. This way you can undo if something breaks.

**Option A: Ask the AI to commit** (easiest)

In the AI chat, type:
```
Commit these changes with a message describing what we built.
```

The AI will run the git commands for you.

**Option B: Use git commands directly**

In the terminal (not the AI chat), type:
```bash
git add .
git commit -m "Add inflation chart script"
```

**Option C: Use your IDE**

If you are using VS Code, Cursor, or similar: look for a Source Control icon in the left
sidebar (it looks like a branching line). Click it, type a message like "Add inflation
chart script", and click the checkmark to commit.

All three options do the same thing: create a checkpoint you can return to later.

### Step 4: Run the script

Now run what the AI created. In the terminal (not the AI chat), type:

```bash
python inflation_chart.py
```

(Use whatever filename the AI created in Step 2.)

**What to look for:**

- **If it works:** You will see either no output (silent success) or maybe some status
  messages. A new file called `inflation_chart.png` (or similar) should appear in your folder.

- **If it fails with "No module named X":** You are missing a library. Copy the entire
  error message, go back to the AI chat, and paste it:
  ```
  I got this error when running the script:
  [paste the error here]
  ```
  The AI will tell you how to install the missing library (usually `pip install X`).
  Then try running the script again.

- **If it fails with a different error:** Same process. Paste the error to the AI, let it
  fix the code, then run again.

This back-and-forth is normal. Most scripts do not work on the first try.

### Step 5: Check your results

Once the script runs without errors, find the chart it created. In the terminal:

```bash
# macOS
open inflation_chart.png

# Windows
start inflation_chart.png

# Linux
xdg-open inflation_chart.png
```

Or just look in your project folder using Finder/Explorer or your IDE's file browser.

**Look at the chart with skepticism:**

- Does the date range make sense? Does it start when you expected?
- Does the Y-axis look right? Is it showing percentages or raw index numbers?
- Do the numbers match what you have heard about inflation? (For example, 2022-2023 had
  notably high inflation - does the chart show that?)
- Is anything confusing or unlabeled?

If something looks off, you will address it in the next step.

### Step 6: Question and iterate

This is where it gets interesting. Go back to the AI chat and ask follow-up questions.
After each change, run the script again (`python inflation_chart.py`) to see the result.

**Understand the data:**
```
Show me the first and last 10 rows of the raw data. What date range does this cover?
```

**Challenge what you see:**
```
I'm skeptical of this chart. The Y-axis shows raw CPI index values, which don't mean
much to me. Can you show year-over-year percentage change instead? That's what people
usually mean by "inflation rate."
```

**Add useful context:**
```
Add a horizontal line showing the Fed's 2% inflation target so I can see when we were
above or below it.
```

**Do something practical:**
```
What would $100 from January 1990 be worth today in inflation-adjusted dollars?
Print that calculation and add it as a text annotation on the chart.
```

**Make it presentable:**
```
Make the chart look more polished. Add a title, label the axes clearly, and use a
color scheme that would work in a presentation.
```

After each change:
1. Run the script again: `python inflation_chart.py`
2. Look at the new chart
3. Decide if you want to change anything else

**Save periodically.** If you have made several changes and things are working, commit again:
```
Commit these changes. We refined the chart to show percentage change and added the Fed target line.
```

This is the real power: you can interrogate the data, change how it is presented, add new
calculations, and keep refining until you have something useful. Each question builds on
what you already have. The AI can see your existing code and modify it - you are not starting
over each time.

### Why this matters

You just:
- Downloaded real government data
- Analyzed it
- Created a visualization
- Saved your work with version control
- (Optionally) refined it through follow-up questions

None of this required you to write code yourself. You described what you wanted, reviewed
what the AI built, questioned the results, and iterated.

This is the core loop. Everything else is refinement.

### A note on complexity

Each step above has depth you can explore later: git has dozens of commands, Python has
thousands of libraries, data visualization is its own field. You do not need to learn any
of that right now. This one path works. Start here, and learn more as you need it.

---
<!-- nav -->
Previous: [Project Structure and Instructions](project-structure.md)
Next: [Python Basics](python-basics.md)

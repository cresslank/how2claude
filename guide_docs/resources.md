# Resources

## Insider perspectives

These are from people who built Claude Code or use it professionally at scale.

- [Boris Cherny's workflow thread](https://x.com/bcherny/status/2007179832300581177) - The creator of Claude Code showing his actual setup: running 5 parallel sessions, plan mode first, CLAUDE.md for team memory, verification loops
- [Anthropic's Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices) - Official guide covering CLAUDE.md, slash commands, headless mode, and the "explore, plan, code, commit" workflow
- [How Anthropic Teams Use Claude Code](https://claude.com/blog/how-anthropic-teams-use-claude-code) - Internal workflows from the people who make it

## Workflow breakdowns

- [How I Use Every Claude Code Feature](https://blog.sshh.io/p/how-i-use-every-claude-code-feature) (Shrivu Shankar) - Systematic walkthrough: CLAUDE.md as "constitution", when to use plan mode, context management strategies, hooks, and subagents
- [How I Use LLMs to Help Me Write Code](https://simonw.substack.com/p/how-i-use-llms-to-help-me-write-code) (Simon Willison) - Realistic about what works and what doesn't. Includes actual session transcripts.
- [31 Days with Claude Code](https://www.hung-truong.com/blog/2025/08/01/31-days-with-claude-code-what-i-learned/) - Honest month-long experience. Covers context poisoning (and how to avoid it), when to /clear, what tasks Claude handles well vs poorly.
- [Claude Code Gotchas](https://www.dolthub.com/blog/2025-06-30-claude-code-gotchas/) (DoltHub) - Eight specific problems from heavy production use: context compaction issues, Claude giving up on large tasks, test modification traps. Each with workarounds.

## Non-programmer perspectives

If you're not a developer, these show what's actually possible.

- [Claude Code for Everyday Tasks](https://every.to/source-code/how-to-use-claude-code-for-everyday-tasks-no-programming-required) (Every) - Expense tracking, content analysis, customer research. Concrete workflows from non-technical users.
- [Everyone Should Be Using Claude Code More](https://www.lennysnewsletter.com/p/everyone-should-be-using-claude-code) (Lenny Rachitsky) - 50 real examples from readers: file organization, image enhancement, meeting analysis, domain brainstorming
- [Claude Code is About So Much More Than Coding](https://www.transformernews.ai/p/claude-code-is-about-so-much-more) - Tax prep, booking tickets, vacation planning. What's possible with zero coding background.

## Practical resources

- [Slash command collection](https://github.com/wshobson/commands) - 57 production-ready commands: /commit, /review, /test-coverage, security scans. Drop into your .claude/commands/ folder.
- [Token optimization workflow](https://gist.github.com/artemgetmann/74f28d2958b53baf50597b669d4bce43) - Practical system for managing context: when to /compact, how to structure CLAUDE.md, modular documentation patterns
- [Writing a Good CLAUDE.md](https://www.humanlayer.dev/blog/writing-a-good-claude-md) - The "less is more" principle. Their production CLAUDE.md is under 60 lines.

## Official documentation

- [Claude Code Overview](https://code.claude.com/docs/en/overview)
- [Slash Commands](https://code.claude.com/docs/en/slash-commands)
- [MCP Integration](https://code.claude.com/docs/en/mcp)
- [Codex CLI](https://developers.openai.com/codex/cli/)
- [Codex AGENTS.md](https://developers.openai.com/codex/guides/agents-md/)

## Free courses

- [Claude Code in Action](https://anthropic.skilljar.com/claude-code-in-action) - Anthropic's official free course
- [Claude Code: A Highly Agentic Coding Assistant](https://learn.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant/) - DeepLearning.AI course built with Anthropic

## What's possible

- [Jaana Dogan's distributed systems tweet](https://x.com/rakyll/status/2007239758158975130) - Google principal engineer: "I gave Claude Code a description of the problem, it generated what we built last year in an hour."

---
<!-- nav -->
Previous: [Quick Reference](quick-reference.md)

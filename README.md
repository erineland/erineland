# Hi, I'm Erin 👋

I'm a software engineer in London with ten years of shipping web products at scale: **Microsoft**, **Booking.com**, **Apple**, and now **Feeld**.

These days most of my building happens *around* the code: I design AI agent systems that do real work, safely. I run a personal Claude Code setup every day with dozens of skills, my own MCP servers, hooks and scheduled jobs. It handles my mail, calendar, budgeting checks, smart home and admin, and it's built so that it **can't** do the dangerous things by accident.

## 🛡️ Safe agents for real life

The repos below are pulled out of that system and made generic. The common thread: **give an agent real access, but make the risky paths fail closed.**

| Repo | What it does | The safety idea |
|---|---|---|
| [**claude-code-guardrails**](https://github.com/erineland/claude-code-guardrails) | `PreToolUse` hooks for Claude Code, plus a width-aware status line | Every write to money or mail becomes a plain-English permission prompt; secrets stay out of the transcript; unparseable input still asks |
| [**whatsapp-readonly-mcp**](https://github.com/erineland/whatsapp-readonly-mcp) | MCP server that reads WhatsApp Desktop's local database | Designed against prompt injection: no send capability, network blocked, every read audit-logged, chats can be walled off |
| [**icloud-drive-mcp**](https://github.com/erineland/icloud-drive-mcp) | Spotlight-backed search and reading of iCloud Drive, including PDF text | Zero dependencies; fast search over millions of files without walking the tree |

## 🧭 How I like to build

- **Least privilege first.** Read-only by default; writes go through a guard a human approves.
- **Treat untrusted text as data, never instructions.** Messages and emails can't steer the agent.
- **Fail closed.** If a guard can't understand a request, it asks rather than allows.
- **Small, boring, auditable.** Plain Python and standard library where possible, so anyone can read what it does.

## 📫 Say hi

Find me on [LinkedIn](https://www.linkedin.com/in/erineland/), or open an issue on any repo.

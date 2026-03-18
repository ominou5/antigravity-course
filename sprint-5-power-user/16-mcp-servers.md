# Lesson 16: MCP Servers — Connecting Antigravity to Everything

---

## What Is MCP?

**MCP** stands for Model Context Protocol. It's the system that allows Antigravity to connect to external services and tools — going beyond your local files and into the broader world of APIs, databases, platforms, and services.

In plain English: MCP servers are connections that let Antigravity talk to other apps on your behalf.

---

## What Can MCP Servers Do?

Antigravity comes with a set of built-in MCP servers, including:

| MCP Server | What it connects to | What you can do |
|---|---|---|
| **GitHub** | Your GitHub repos | Browse repos, read commits, create PRs, manage issues |
| **Firebase** | Google's app platform | Manage Firestore data, auth users, deploy to Firebase |
| **Cloudflare** | Cloudflare services | Deploy workers, manage DNS, access R2 storage |

Beyond those, there are **community MCP servers** you can add — these are built by the community and cover a huge range of services:

| MCP Server | What it connects to | What you can do |
|---|---|---|
| **ClickUp** | Project management | Create tasks, update statuses, manage projects |
| **Context7** | Documentation | Pull live documentation for any library |
| *…and hundreds more* | Databases, APIs, SaaS tools | Varies by server |

MCP is an open standard — anyone can build and publish an MCP server. The ecosystem grows constantly.

---

## How to Use an MCP Server

You don't need to configure anything complicated. Just use it in natural language:

```
Using the GitHub MCP, show me the last 5 commits on my habit-tracker repo 
and tell me what changed in each one.
```

Or:

```
Use the Cloudflare MCP to check the deployment status of my site.
```

Antigravity will invoke the appropriate MCP server, retrieve the information, and present it back to you in a readable format.

---

## Real Example: GitHub MCP

After pushing your Habit Tracker to GitHub, you can use the GitHub MCP to interact with it without opening a browser:

```
Use the GitHub MCP to:
1. Show me my habit-tracker repository's details
2. List all open issues (if any)
3. Tell me when the last commit was and what it changed
```

Then try creating an Issue to track future work:

```
Use GitHub MCP to create an issue on my habit-tracker repo titled 
"Add daily habit reset at midnight" with a description explaining 
that habits should automatically uncheck each day.
```

---

## Real Example: Context7 (Documentation Lookup)

The Context7 MCP is extremely useful while coding. Instead of Antigravity guessing how a library works, it can pull the actual, current documentation:

```
Using Context7, look up the latest Supabase JavaScript client documentation 
for how to handle real-time subscriptions. Then show me how to add 
real-time habit updates to my app.
```

This ensures Antigravity is working from accurate, up-to-date library documentation — not its training data, which might be months or years old.

---

## The Broader Picture: Why MCP Matters

Traditional software requires you to switch between apps constantly. You check GitHub in the browser, you update ClickUp in another tab, you deploy in the terminal.

With MCP, Antigravity becomes a control center. You describe what you want to happen across multiple services — in a single conversation — and it coordinates them for you.

**Example multi-MCP prompt:**
```
I just finished the user auth feature. 
Using GitHub MCP: commit and push all changes, then create a PR titled "Add user auth".
Using ClickUp MCP: update the task "User Authentication" to status "Done".
Then tell me what's left before this sprint is complete.
```

One prompt. Three actions across two platforms.

---

## Finding Available MCP Servers

Ask Antigravity what's currently connected:

```
What MCP servers do I have available? 
Give me a brief description of what each one can do.
```

---

## Try It Yourself

Pick one MCP server and explore it. Here are some starter prompts:

**GitHub:**
```
Use the GitHub MCP to look at my most recent commit and summarize 
the changes in plain English, as if explaining them to a non-technical teammate.
```

**Context7:**
```
Use Context7 to find the best way to implement a "remember me" 
feature using Supabase Auth, then implement it in my app.
```

**ClickUp (if you use it):**
```
Use the ClickUp MCP to create a new task list called "Habit Tracker Improvements" 
and add 3 feature ideas as tasks: daily reminders, streak visualization, and habit categories.
```

---

## Summary

- MCP servers are connections to external services — GitHub, Cloudflare, Firebase, and more
- You use them in natural language — no API keys or code required on your end
- They let Antigravity act across multiple platforms in a single conversation
- Context7 MCP gives Antigravity access to live documentation — great for accuracy
- Ask Antigravity what MCPs are available and explore them as your projects grow

**Next:** [Lesson 17 — Memory, Knowledge & Context](17-memory-knowledge-context.md)

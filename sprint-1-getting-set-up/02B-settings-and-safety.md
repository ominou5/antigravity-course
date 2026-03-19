# Lesson 02B: Settings & Safety — Before You Start Chatting

---

Before you send your first real message, take five minutes to look through Antigravity's settings. These aren't buried preferences — they directly control what the agent is allowed to do on your machine. Understanding them now prevents surprises later.

Open settings via the gear icon or **Settings** menu in Antigravity.

---

## The Security Section

### Strict Mode

> **Recommended for new users: Leave OFF to start, then consider turning ON.**

Strict Mode enforces a blanket of human review across all agent actions. When enabled, Antigravity cannot autonomously run commands or take actions — it must ask for your approval at every step.

Sounds good, right? The trade-off is speed and flow. Strict Mode is great if you're working on sensitive codebases or want zero surprises, but it can slow down creative sessions where you want to iterate quickly.

**Sam's setting:** OFF — but she uses "Request Review" on terminal commands instead (see below). That's the recommended starting point for this course.

> 📖 Full details at [antigravity.google/docs/strict-mode](https://antigravity.google/docs/strict-mode)

---

## The Artifact Section

### Review Policy

Artifacts are documents Antigravity creates to show you plans, summaries, and structured information. The Review Policy controls when Antigravity asks you to approve these before continuing.

| Option | What Happens | Risk Level |
|---|---|---|
| **Always Proceeds** | Agent never pauses for review | Highest — agent may act on content you haven't seen |
| **Agent Decides** | Agent uses judgment based on complexity | Medium — good balance for most users |
| **Asks for Review** | Agent always pauses for you to read artifacts | Lowest — safest for beginners |

**Sam's setting:** *Asks for Review* — the safest starting point. You can loosen this later once you trust how Antigravity presents plans.

> 💡 **For this course:** Keep it on **Asks for Review**. You'll see Antigravity show you plans before it acts — that's intentional and educational.

---

## The Terminal Section

This is the most important section from a machine-safety perspective. The terminal is where Antigravity runs commands that can install software, modify files, or change system configuration.

### Terminal Command Auto Execution

| Option | What Happens |
|---|---|
| **Always Proceed** | Agent runs commands without asking you first |
| **Request Review** | Agent always shows you the command and waits for your approval |

**Sam's setting:** *Request Review* — **this is strongly recommended for new users.**

> ⚠️ **Why this matters:** A terminal command can delete files, install packages you didn't want, or make network requests. With Request Review on, you see every command before it runs. You build an intuition for what's normal — and you catch anything unusual.

### Enable Shell Integration

When enabled, Antigravity hooks into VS Code's built-in shell so it can detect when commands finish and read their output — this makes it much smarter about debugging errors.

**Sam's setting:** ON — leave this on. It's a pure quality-of-life improvement.

### Allow List & Deny List

These are power-user features for when you're comfortable with the agent's behavior:

- **Allow List:** Commands that Antigravity can run *without asking*, even in Request Review mode.  
  *Example: you might add `git status` or `npm run dev` if you always want those to run automatically.*

- **Deny List:** Commands that Antigravity must *always* ask about, even in Always Proceed mode.  
  *Example: `rm -rf` or `sudo` — anything with irreversible consequences.*

**Sam's setting:** Both empty for now. You can configure these later as you develop your own workflow.

> 💡 **Tip:** The Deny List takes precedence over the Allow List. So if `rm` is on the Deny List and you also have `rm dist` on the Allow List, Antigravity will still ask.

---

## The File Access Section

### Agent Gitignore Access

When enabled, Antigravity can read and edit your `.gitignore` file automatically.

> ⚠️ **Caution:** If your `.gitignore` references sensitive files (e.g., `.env`, credential files), this setting gives the agent awareness of where those files are. It doesn't expose their contents — but be mindful.

**Sam's setting:** OFF.

### Agent Non-Workspace File Access

This controls whether Antigravity can read and edit *files outside of your current project folder*.

> ⚠️ **Caution:** This is the highest-risk file access setting. Leaving it on means the agent can potentially access configuration files, SSH keys, environment files, or anything else on your computer. It also opens a potential attack surface for **prompt injection** — where malicious content in a file could attempt to redirect the agent's behavior.

**Sam's setting:** OFF — **strongly recommended to keep this OFF** unless you have a specific reason to enable it.

### Auto-Open Edited Files

When Antigravity edits a file, it automatically opens it in the editor so you can see the change immediately.

**Sam's setting:** ON — great for beginners because you always see what changed.

---

## The Automation Section

### Agent Auto-Fix Lints

When enabled, Antigravity can see code quality warnings (called "lints") it caused and quietly fix them without prompting you.

**Sam's setting:** ON — this is a helpful quality-of-life setting that keeps your code clean. It's low risk because it's only fixing issues introduced by its own edits.

---

## The History Section

### Conversation History

When enabled, Antigravity can read past conversations to give you more contextually relevant responses. This is what makes it feel like it "remembers" things about your project over time.

**Sam's setting:** ON — definitely recommended. This makes Antigravity significantly more useful across sessions.

### Knowledge

When enabled, Antigravity builds a knowledge base in the background from your conversations — capturing patterns, decisions, and context about your project that it can use in future sessions.

**Sam's setting:** ON — also recommended. Think of it as long-term memory that makes the agent smarter about *your specific project* over time.

> 💡 Disabling Knowledge stops the agent from *accessing* the existing knowledge base, but doesn't delete it.

---

## The General Section

These settings are mostly personal preference, but here's what each one does:

| Setting | What It Does | Sam's Setting |
|---|---|---|
| **Explain and Fix in Current Conversation** | "Explain and Fix" actions continue in the active chat rather than opening a new one | OFF |
| **Open Agent on Reload** | The chat panel opens automatically when you reopen the window | ON |
| **Follow Along by Default** | The view scrolls to track the agent's current activity in new conversations | OFF |
| **Enable Sounds for Agent** | Plays a sound when Antigravity finishes generating | OFF |
| **Auto-Expand Changes Overview** | The Changes Overview toolbar expands automatically after each response | ON |
| **[Dev] GCP Project ID** | Advanced setting for cloud/enterprise features — leave blank unless you know what this is | Blank |

---

## Your Settings Checklist for This Course

Before moving on, set these up:

- [ ] **Strict Mode:** OFF (you'll rely on the per-feature controls instead)
- [ ] **Review Policy:** Asks for Review
- [ ] **Terminal Command Auto Execution:** Request Review
- [ ] **Enable Shell Integration:** ON
- [ ] **Agent Non-Workspace File Access:** OFF
- [ ] **Agent Gitignore Access:** OFF
- [ ] **Auto-Open Edited Files:** ON
- [ ] **Agent Auto-Fix Lints:** ON
- [ ] **Conversation History:** ON
- [ ] **Knowledge:** ON

This gives you a safe, educational setup where you see what Antigravity is doing at each step — without being so restrictive that it becomes frustrating.

---

## The Golden Rule

> **You are always the last line of defense.** Antigravity asks before acting in most cases, but it's only as safe as the settings you configure — and your habit of actually reading what it proposes before clicking "Yes."

No AI agent is infallible. Read the commands before you approve them. Read the file changes before you accept them. Over time you'll get fast at it — but start by actually looking.

---

## Summary

- **Security:** Strict Mode is optional; control safety through per-feature settings instead
- **Terminal:** Use "Request Review" as a new user — read every command before approving
- **File Access:** Keep Non-Workspace File Access OFF to protect your machine
- **History & Knowledge:** Turn both on so Antigravity gets smarter about your project over time
- **General:** Mostly personal preference — the defaults are fine

**Next:** [Lesson 03 — Your First Conversation](03-your-first-conversation.md)

# Lesson 07: Understanding the Workspace

---

## What Is the "Workspace"?

The workspace is the folder you opened in Antigravity. Everything inside it is what Antigravity can work with — files, folders, code, configuration.

But the workspace isn't just a folder. Antigravity adds a layer of intelligence: it understands the *context* of what you're building, tracks your progress across a session, and makes plans before it acts.

This lesson explains the things happening behind the scenes as Antigravity works.

---

## Tasks and Planning Mode

When you give Antigravity a substantial request — something that involves multiple steps — it doesn't just start coding immediately. It switches into **Planning Mode** first.

In Planning Mode, Antigravity:
- Breaks down what needs to be done
- Lists the steps in order
- Sometimes creates a plan document for you to review

You'll see something like:

```
Here's my plan for adding a database to your app:

1. Set up a Supabase project and copy the connection credentials
2. Add the Supabase client library to your project
3. Create a "habits" table in Supabase
4. Update app.js to read and write from the database instead of memory
5. Test that habits persist after refreshing the page

Does this look right? Any changes before I start?
```

This is **your chance to steer**. Read the plan. If something looks wrong or out of order, say so before Antigravity starts executing.

---

## Reviewing the Plan

When Antigravity shows you a plan, ask yourself:

- Does this match what I asked for?
- Is anything missing?
- Does the order make sense?

You can respond with:
- "Yes, that looks right — go ahead"
- "Step 3 should come before step 2"
- "Actually, skip the authentication part for now — I'll add that later"

This is one of the most powerful features of Antigravity: you're always a collaborator, not just a passive observer.

---

## Execution Mode

Once you approve the plan, Antigravity switches to **Execution Mode**. You'll see it working through the steps, creating and editing files, and reporting back as it goes.

You can watch the progress in the task panel — it shows what step it's on, what files it's touching, and what tools it's using.

---

## Tools Antigravity Uses

Behind the scenes, Antigravity has access to a set of tools it can use when needed. It tells you when it's using one:

| Tool | What it does |
|---|---|
| File reader | Reads files in your workspace |
| File writer | Creates or edits files |
| Terminal | Runs commands (installs packages, runs scripts, etc.) |
| Web search | Looks up documentation or answers online |
| Browser | Opens a page to check how it looks |

You will always know when a tool is being used. Antigravity doesn't operate silently.

---

## Artifacts

Sometimes Antigravity creates **artifacts** — special documents that aren't part of your app but exist to help you and Antigravity stay aligned.

Examples of artifacts:
- **Implementation plans** — a written plan for a big feature
- **Task checklists** — a list of steps to complete
- **Walkthroughs** — a summary of what was just built and how it was tested

You can read, edit, or reference artifacts. They're especially useful in longer projects where you want a clear record of what was decided and why.

---

## What Happens When Something Goes Wrong

If Antigravity hits a problem mid-task — an error, an unexpected file structure, something it doesn't know how to handle — it will stop and tell you. It doesn't silently push forward and hope for the best.

Common responses from Antigravity when something goes wrong:
- "I got an error when I tried to run that — here's what I see: [error]. How would you like me to proceed?"
- "I'm not sure which approach to take here — there are two options: [...]. Which do you prefer?"
- "Something unexpected happened. I stopped before making any further changes."

This is a good thing. Stopping and asking is almost always better than guessing.

---

## The Escape Hatch — Redirecting

If a session goes off the rails, you can always redirect:

```
Let's pause on this. I think we went in the wrong direction. 
Here's what I actually wanted: [explain clearly]. 
Can you undo what you just did and start over with this approach?
```

And if Antigravity made file changes you want to roll back:

```
Undo the last set of changes you made. 
Let's go back to where we were before you started that.
```

---

## Try It Yourself

**Exercise 1 — Trigger planning mode:**
```
I want to add a new page to my personal site from Lesson 06 — 
a "Projects" page that lists 3 projects I've worked on, 
each with a title, description, and a link. 
Before you build it, show me your plan.
```

Review the plan. Ask a clarifying question or request a change before approving.

**Exercise 2 — Inspect the workspace:**
```
Look at all the files in my current workspace and give me 
a plain-English summary of what this project does and what each file is for.
```

---

## Summary

- The workspace is your project folder — Antigravity works within it
- For bigger tasks, Antigravity plans before executing — review the plan
- Execution mode is when it's actively building — you can follow along
- Antigravity uses tools (file reader, terminal, browser, web search) transparently
- Artifacts are planning/summary documents that help you stay aligned
- When something goes wrong, Antigravity stops and asks — it doesn't guess

**Next:** [Lesson 07B — Want to Build Something Else?](../07B-choose-your-own-path.md)

*Or skip straight to Sprint 3:* [Lesson 08 — Planning Your App](../sprint-3-building-the-app/08-planning-your-app.md)

# Lesson 03: Your First Conversation

---

## How the Chat Works

The chat panel in Antigravity is where you communicate. You type a message and press **Enter** to send. Antigravity responds.

It's conversational — Antigravity remembers what you said earlier in the same session, so you can refer back to things without repeating yourself.

When you close Antigravity and reopen it later, the conversation history may reset depending on your settings — but your *files* always stay. The project is persistent; the conversation is a session.

---

## Your First Real Prompt

Type this and press Enter:

```
I'm just getting started with Antigravity. What are the most useful things I can ask you to do?
```

You'll get a summary of Antigravity's capabilities in plain English. Don't try to memorize it — just read through and notice the range. You'll use all of these by the end of this course.

---

## Reading Antigravity's Responses

Antigravity doesn't just reply with text. Depending on what you ask, it may also:

- **Propose file changes** — it shows you what it wants to edit before doing it
- **Run commands** — like starting a server or installing a package; it asks first
- **Use tools** — search the web, read files, run code; it shows you when it does this
- **Create a plan** — for bigger tasks, it lays out the steps before starting

This transparency is intentional. You're always supposed to know what's happening.

---

## Approving and Denying Actions

When Antigravity wants to make a file change or run a command, it will pause and show you what it plans to do. You'll see something like:

```
I'll create a file called hello.html with the following content:
[shows you the file preview]

Proceed? [Yes / No]
```

- Click **Yes** (or the equivalent button) to approve
- Click **No** to cancel — and then tell it why, so it can try differently

> **Tip:** Don't just click Yes automatically. Take a second to read what it's proposing. This habit will save you from unexpected surprises.

---

## A Back-and-Forth Example

Here's what a natural conversation with Antigravity looks like:

```
You: I want to build a simple webpage that says "Hello, World!"

Antigravity: I'll create an index.html file with a basic 
             Hello World page. [shows preview] Proceed?

You: Yes, but can you make "Hello, World!" bigger 
     and centered on the page?

Antigravity: I'll update the file with those changes. 
             [shows new preview] Proceed?

You: Yes. Now add a background color — something calm.

Antigravity: I'll add a soft blue background. [shows preview] 
             Proceed?

You: Perfect.
```

Notice: you never wrote a single line of HTML. You just had a conversation.

---

## Useful Things to Know Right Away

**Interrupt a response:**
If Antigravity is generating something long and you want it to stop, press **Escape** or click the stop button. It'll pause immediately.

**Start fresh:**
If the conversation has gone off track, you can tell it: *"Let's start over on this. Forget what we discussed and try again with this new approach..."*

**Ask for an explanation:**
At any point you can ask *"What did you just do and why?"* or *"Explain that last change in plain English."* Antigravity will always explain.

**Undo a change:**
If Antigravity made a file change you don't like, you can ask: *"Undo the last change you made to that file."* Even better — use Git (covered in Lesson 05B) so you always have a safety net.

---

## What Antigravity Can See

By default, Antigravity can see:
- The folder you opened (your workspace)
- Files you ask it to read
- Output from commands it runs (when you approve them)

It does **not** automatically read every file in your project on its own. You ask it to look at things, and it does.

---

## Try It Yourself

Run through this mini-exercise:

**Step 1:** Ask Antigravity a question:
```
What's the difference between a website and a web app? Explain like I've never coded before.
```

**Step 2:** Follow up:
```
Give me one real-world example of each.
```

**Step 3:** Ask it to create something:
```
Create a simple HTML file called hello.html that says "Hello, World!" in big, centered text. 
Save it in my current folder.
```

When it proposes the file, approve it. Then find `hello.html` in your file explorer and open it in your browser to see the result.

---

## Summary

- The chat panel is your primary interface — type your request, press Enter
- Antigravity remembers context within a session, but files always persist
- It shows you proposed actions before doing them — approve or deny
- You can ask for explanations at any time
- You can interrupt, undo, or redirect the conversation whenever you want

**Next:** [Lesson 04 — How to Give Great Prompts](../sprint-2-core-skills/04-how-to-give-great-prompts.md)

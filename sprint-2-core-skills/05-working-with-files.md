# Lesson 05: Working With Files & Projects

---

## How Antigravity Relates to Your Files

Antigravity works inside your **workspace** — the folder you opened when you launched it. Every file it creates, edits, or reads lives inside that folder (unless you specifically ask it to look elsewhere).

This is important: Antigravity is working with real files on your computer. When it creates `index.html`, that file actually exists on your hard drive. When it edits `app.js`, those changes are real.

---

## What Antigravity Does With Files

**Reading files:**
When you ask Antigravity to look at a file, it reads the contents and uses that information in its response. It won't read files unless you ask it to (or unless they're directly relevant to a task it's doing).

```
Read the file styles.css and tell me what it currently does.
```

**Creating files:**
Antigravity will show you the proposed file content before creating it. You approve, and the file appears in your workspace.

```
Create a file called about.html with a simple "About Me" page.
```

**Editing files:**
For edits, Antigravity shows you a **diff** — a before-and-after view of what's changing. Lines being removed are shown in red (or marked with `-`), lines being added in green (or `+`).

**Deleting files:**
Antigravity can delete files, but it will always tell you what it's deleting before doing so.

---

## Understanding Diffs

A diff is just a visual way of showing what changed. You'll see these a lot.

Example diff — changing a button color:

```diff
-  <button style="background: blue;">Add Habit</button>
+  <button style="background: green;">Add Habit</button>
```

The `-` line is being removed. The `+` line replaces it.

When you see a diff, the question to ask yourself is: *"Does this match what I asked for, and is it only changing what I expected it to change?"*

If Antigravity changes something you didn't ask it to change, notice that. You can tell it:

```
You changed the font size but I didn't ask for that. 
Please revert that part and only change the button color.
```

---

## File Explorer

The file explorer panel shows all the files and folders in your workspace. You can click on files to open them in the editor.

As Antigravity creates and edits files, you'll see them appear and change in real time.

If you don't see the file explorer, look for a folder/files icon in the sidebar, or check View settings.

---

## Project Structure — What Goes Where

When you're building a web project, the files tend to follow a predictable pattern:

```
my-project/
├── index.html       ← The main page
├── styles.css       ← How things look
├── app.js           ← How things behave
└── README.md        ← What this project is
```

As your project grows, you'll add more files and folders. Antigravity will suggest structure as you go — you don't need to plan this in advance.

---

## Working in a Project Over Multiple Sessions

Your files persist between sessions. When you close Antigravity and reopen it tomorrow, all your files are exactly where you left them.

What doesn't automatically persist is **conversation context**. If you were mid-task yesterday, start a new session by briefly catching Antigravity up:

```
We've been building a habit tracker app. The frontend is done (index.html, styles.css, app.js). 
Today I want to connect it to a Supabase database. Here's the current state of app.js: [paste or let it read the file]
```

Or better yet — use a briefing file (covered in Lesson 17). For now, a quick summary at the start of each session works fine.

---

## Try It Yourself

**Exercise 1 — Create and explore:**
```
Create three files for the start of a web project: 
index.html (with a basic page structure), 
styles.css (empty for now), 
and app.js (with a comment saying "JavaScript goes here").
```

After Antigravity creates them, find them in the file explorer and open each one.

**Exercise 2 — Read and summarize:**
```
Read index.html and explain what each part of the file does 
in plain English. Assume I don't know any HTML.
```

**Exercise 3 — Make a change:**
```
Edit index.html to change the page title (the text in the browser tab) 
to "My First Project". Show me the diff before making the change.
```

---

## Summary

- Antigravity works with real files in your workspace folder
- It shows proposed file changes (diffs) before applying them — read them
- The file explorer shows your project structure at a glance
- Files persist between sessions; conversation context does not
- Brief Antigravity at the start of each session on where you left off

**Next:** [Lesson 05B — Git Basics](05B-git-basics.md)

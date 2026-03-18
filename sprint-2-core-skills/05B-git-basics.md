# Lesson 05B: Git Basics — Let Antigravity Teach You

---

## Why This Lesson Exists

Before you start building a real app, you need a safety net.

That safety net is called **Git**. It's a system that tracks every change you make to your project, lets you go back in time if something breaks, and allows you to share your code with others (like GitHub).

You don't need to become a Git expert right now. You need to know enough to protect your work and upload it to GitHub. Antigravity will handle the rest — and walk you through everything interactively.

---

## What Is Git?

Git is a **version control system**. Here's an analogy:

Imagine you're writing a long document. Every time you finish a good section, you save a copy called "draft-v2," "draft-v3," and so on. If you accidentally delete something important, you open an earlier copy.

Git does this for code — automatically, precisely, and without eating up storage space. Each "save point" is called a **commit**.

---

## What Is GitHub?

Git and GitHub are not the same thing:

- **Git** is the tool that runs on your computer and tracks changes
- **GitHub** is a website that stores your Git repositories online (free)

Think of Git as the save system. GitHub is the cloud backup.

By the end of this lesson, you'll have your project saved locally with Git *and* backed up to GitHub.

---

## Step 1: Install Git

**Let Antigravity walk you through it.** Type this:

```
I've never used Git before. Check if Git is installed on my computer.
If it's not installed, give me step-by-step instructions to install it 
for my operating system, and let me know when I should come back to you.
```

Antigravity will check your system, tell you what to do, and wait for you to confirm before continuing.

---

## Step 2: Set Up Git With Your Name

Once Git is installed, run this in the Antigravity chat:

```
Git is now installed. Help me set my name and email for Git 
so my commits are attributed correctly. My name is [Your Name] 
and my email is [your-email@example.com].
```

Antigravity will run the configuration commands for you.

---

## Step 3: Create a GitHub Account

If you don't have a GitHub account yet:

1. Go to [github.com](https://github.com)
2. Click **Sign up** — it's free
3. Verify your email

Then tell Antigravity:
```
I now have a GitHub account with username [your-username]. 
What's next?
```

---

## Step 4: Initialize Git in Your Project

In your project folder, Antigravity will set up Git:

```
Initialize Git in my project folder. Create a .gitignore file 
appropriate for a web project (HTML, CSS, JavaScript).
```

This creates a hidden `.git` folder that Git uses to track changes, and a `.gitignore` file that lists files that *shouldn't* be tracked (like secret keys or temporary files).

---

## Step 5: Your First Commit

A **commit** is a named snapshot of your project at a moment in time.

```
Make my first Git commit. Add all the current files and use 
the commit message "Initial commit — project setup".
```

Antigravity will stage and commit your files. Congratulations — you've just saved your first snapshot.

---

## Step 6: Push to GitHub

**Create a new repo on GitHub:**
1. Go to [github.com/new](https://github.com/new)
2. Name it something like `habit-tracker`
3. Set it to **Public** (so you can deploy it later for free)
4. Click **Create repository**

Then tell Antigravity:
```
I created a GitHub repo. Here's the command GitHub gave me 
to connect it: [paste the command from GitHub's setup page]
Push my project to GitHub.
```

Antigravity will connect your local project to GitHub and push everything up.

---

## The Commit Habit — Do This After Every Lesson

From now on, commit your project at the end of each lesson. One prompt to do it all:

```
Commit all my current changes to Git with the message 
"Completed Lesson [X] — [short description of what you did]"
```

By the end of this course, you'll have a beautiful commit history showing every step of your project from lesson 1 to live deployment.

---

## The 4 Git Commands You Actually Need

Antigravity will handle these for you, but it's worth knowing what they mean:

| Command | What it does |
|---|---|
| `git add .` | Stage all changed files (mark them for saving) |
| `git commit -m "message"` | Save a snapshot with a description |
| `git push` | Upload to GitHub |
| `git status` | Show what's changed since your last commit |

That's it. Those four cover 90% of day-to-day Git usage.

---

## A True Story

> *"I personally learned Git by simply asking Antigravity to teach me. I didn't read a tutorial — I just asked it to walk me through each step, explain what was happening, and check my understanding before moving on. By the end of a single session, I was using Git confidently. It's genuinely the best way to learn it."*

That's exactly what this lesson is designed to replicate. Don't read about Git — have Antigravity teach you by doing it with you.

---

## Try It Yourself

Use this prompt to have Antigravity teach you interactively:

```
I've never used Git before. Teach me how to use it from scratch.
Walk me through each step — checking if it's installed, configuring 
my name, making my first commit, and pushing to GitHub.
Explain what each command does in plain English.
Don't move on until I confirm I understand each step.
```

---

## Summary

- Git is a version control system — it tracks every change you make
- GitHub is the cloud backup for your Git projects
- The basic workflow: `add` → `commit` → `push`
- Commit at the end of every lesson to build a history of your learning
- Use Antigravity as your interactive Git tutor — it's the best way to learn

**Next:** [Lesson 06 — Building Your First Web Page](06-building-your-first-web-page.md)

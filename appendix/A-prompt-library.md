# Appendix A: Prompt Library

A curated collection of the most useful prompts from this course, plus extras. Copy, paste, and adapt freely.

---

## 🚀 Starting a New Project

```
I want to build [describe your app idea].
Before we write any code, help me plan it.
Ask me any clarifying questions you need, then create a plan
covering: features to include, tech stack recommendation,
and the order we should build things in.
```

```
Set up a project folder structure for [project name].
Create: index.html, styles.css, app.js, and a README.md.
```

```
Create an AGENT.md file for this project. Include the tech stack,
what the project does, how to run it locally, key decisions made so far,
and any known gotchas.
```

---

## 💬 Getting Better Answers

```
My experience level: I'm a complete beginner.
Please explain everything in plain English, define any jargon,
and walk me through each step before moving to the next.
```

```
Here's a prompt I want to use: [paste your prompt]
Is this clear enough? What information am I missing that would help you
do a better job?
```

```
That explanation went over my head. Can you explain it again
using a simple real-world analogy?
```

---

## 🎨 Frontend & Design

```
Build a clean, modern UI for [describe the app].
Dark background, white text, sans-serif font (use Inter from Google Fonts).
Should look great on mobile and desktop.
```

```
Review the visual design of my app and suggest 3 specific improvements
that would make it look more polished and professional. Then apply them.
```

```
The layout breaks on mobile. Fix the CSS so the app is fully responsive
and looks intentional on small screens.
```

```
Add a loading state that shows while the app is fetching data from Supabase.
```

```
Add a friendly empty state message when there's no data to display.
```

---

## 🗄️ Database & Supabase

```
I've set up a Supabase project. Here are my credentials:
Project URL: [URL]
Anon key: [key]

Create a table called [table name] with these columns: [list columns].
Then connect my app to read and write from this table.
```

```
Update the database query in app.js so that [describe what you want to change].
```

```
Set up Row-Level Security on my Supabase table so users can only
read and write their own rows.
```

---

## 🔐 Authentication

```
Add email/password authentication using Supabase Auth.
Show a login form when the user is not logged in.
After login, show the main app.
Add a sign-out button in the header.
```

```
My auth isn't working. Here's the error: [paste error].
What's wrong?
```

---

## 🐛 Debugging

```
My app isn't working as expected.
Here's what I expected to happen: [describe]
Here's what's actually happening: [describe]
Here's the error from the browser console: [paste error]
What's wrong and how do I fix it?
```

```
Review all the JavaScript in my project and look for bugs,
edge cases I haven't handled, and any code that could fail silently.
```

```
This works locally but breaks on the deployed version.
The live URL is [URL]. What typically causes that mismatch?
```

---

## 🚀 Git & GitHub

```
I've never used Git before. Teach me from scratch.
Walk me through each step, explain what each command does,
and don't move on until I confirm I understand.
```

```
Commit all my current changes to Git with the message "[message]"
and then push to GitHub.
```

```
Something went wrong and I want to go back to the last commit.
What's the safest way to undo my recent changes?
```

---

## 🌐 Deployment

```
Review my project before deployment. Check for: console errors,
missing files, broken links, and any issues that would cause problems
in production.
```

```
I deployed to Netlify and I'm getting a CORS error from Supabase.
The live URL is [URL]. How do I fix this?
```

```
My site deployed successfully but the data isn't loading.
No errors in the console. What could cause that?
```

---

## ⚡ Power User

```
What skills are available to install that could help with my current project?
List them with a short description of each.
```

```
Create a workflow that automates [describe the repeatable task].
I want to trigger it with a single command.
```

```
Use the GitHub MCP to [describe what you want to do with your repo].
```

```
Use Context7 to find the current documentation for [library or feature].
Then implement [specific thing] using the correct, up-to-date approach.
```

---

## 🧠 Context & Memory

```
Read AGENT.md and tell me what you know about this project
before we start today's session.
```

```
We made significant progress today. Update AGENT.md to reflect
what we built and any important decisions we made.
Don't change anything that's still accurate — just add and update.
```

```
Remember my development preferences for all future projects:
[list your preferences — e.g. vanilla JS, Supabase, Netlify, dark mode]
```

---

## 🎓 Learning Mode

```
I want to understand what you just built. Walk me through
the code file by file, explaining what each part does
in plain English. Assume I've never coded before.
```

```
Teach me [concept or technology] by building something practical with it.
Start from absolute basics and don't move forward until I confirm I understand.
```

```
You fixed the bug — but explain why the original code was wrong
so I can avoid making the same mistake again.
```

# Lesson 17: Memory, Knowledge & Context

---

## The Problem With Fresh Sessions

Every time you open a new Antigravity session, it starts fresh. It doesn't know your project, your preferences, your tech stack, or what you decided three sessions ago.

You end up repeating the same context every time:
- "We're building a Habit Tracker"
- "We use Supabase for the database"
- "I prefer vanilla JS, no frameworks"
- "The app is deployed at this URL..."

That's friction. This lesson is about eliminating it.

---

## Solution 1: The AGENT.md File (Project Briefing)

The most powerful habit you can develop is keeping an `AGENT.md` file in every project. This is a plain text file that tells Antigravity everything it needs to know about your project upfront.

When Antigravity opens your project, it reads this file automatically and has instant context.

### Creating Your AGENT.md

Ask Antigravity to generate one from your current project:

```
Based on everything we've built — the Habit Tracker, the tech stack, 
the Supabase setup, the deployment to Netlify — create an AGENT.md file 
for this project. It should include:

1. What this project is
2. The tech stack we use (and why we chose it)
3. How to run it locally
4. Important decisions we've made that I should remember
5. What's currently working
6. What still needs to be done
7. Any "gotchas" or things to watch out for in this codebase
```

### What a Good AGENT.md Looks Like

```markdown
# Habit Tracker — Project Context

## What This Is
A simple habit tracking web app. Users can add daily habits, 
check them off, and see their streaks.

## Tech Stack
- Frontend: Vanilla HTML, CSS, JavaScript (index.html, styles.css, app.js)
- Database: Supabase (PostgreSQL) — free tier
- Auth: Supabase Auth with email/password
- Deployment: Netlify, connected to GitHub repo (auto-deploys on push)
- Version control: Git + GitHub

## Local Development
Open index.html directly in browser. No build step required.

## Environment Notes
Supabase URL and anon key are in app.js (anon key is safe to expose for this project).
After deploy, update Supabase → Auth → URL Configuration with the new domain.

## Known Gotchas
- CORS issues appear when deploying to a new domain — update Supabase URL settings
- RLS is enabled — all habits require a valid user session (if auth is on)

## Deployment
Live at: https://my-habit-tracker.netlify.app
GitHub: https://github.com/yourusername/habit-tracker

## What's Left
- Daily habit reset (auto-uncheck at midnight)
- Streak visualization
```

Now, every new session starts with everything Antigravity needs to know.

---

## Solution 2: Knowledge Items (Antigravity's Long-Term Memory)

Beyond project-level context, Antigravity has a **knowledge base** — a system for storing information across projects and conversations.

Knowledge Items (KIs) are automatically built up as you work. Antigravity extracts key information from your sessions — architectural decisions, patterns, preferences — and stores them for future reference.

You can also ask it to explicitly remember something:

```
Remember that for all my web projects, I prefer:
- Vanilla JavaScript over frameworks
- Supabase for databases
- Netlify for deployment
- Dark mode as the default design

Add this to my knowledge base so you remember my preferences in future projects.
```

---

## Solution 3: Starting Each Session Right

Until AGENT.md becomes second nature, build the habit of starting sessions with a briefing:

```
Before we start: I'm continuing work on the Habit Tracker project. 
Read AGENT.md to get context, then tell me what you understand 
about the current state of the project.
```

Antigravity reads the file, summarizes the state, and you confirm it has the context right before diving in.

This 30-second ritual saves hours of confusion.

---

## Updating Context as You Work

As your project evolves, keep AGENT.md current. At the end of a productive session:

```
We made significant progress today. Update AGENT.md to reflect:
- What we built
- Any new decisions we made
- The current state of the project

Don't change anything that's still accurate — just add and update.
```

---

## Context in Long Sessions

Even within a single session, Antigravity can get confused if the conversation gets very long. Symptoms:
- It "forgets" something from earlier in the conversation
- Responses feel inconsistent
- It contradicts something it said before

When this happens:
```
I think we've lost some context. Let me re-anchor you:
We're working on [project]. The current task is [task]. 
Here's where we are: [brief summary].
```

---

## Try It Yourself

1. **Create your AGENT.md:**
   ```
   Create an AGENT.md for this project capturing everything 
   we've built and decided. Make it comprehensive.
   ```

2. **Test it:** Close Antigravity and reopen it. Then ask:
   ```
   Read AGENT.md and tell me what you know about this project.
   ```
   Confirm it has all the context. Adjust the file if anything's missing.

3. **Store a preference:**
   ```
   Add to my preferences: I always want commit messages to start 
   with the lesson number when working on this course. 
   Remember this for future sessions.
   ```

---

## Summary

- Every new session starts fresh — `AGENT.md` is how you eliminate repeated context setup
- Knowledge Items are Antigravity's long-term memory across projects
- Start sessions with a briefing ("read AGENT.md, confirm what you know")
- Update AGENT.md at the end of productive sessions
- If a long session feels confused, re-anchor with a summary

**Next:** [Lesson 18 — Where to Go From Here](18-where-to-go-from-here.md)

# Lesson 08: Planning Your App With Antigravity

---

## Sprint 3 Goal

By the end of this sprint, you'll have a working Habit Tracker app with:
- A frontend you can use in a browser
- A database that saves your habits
- (Optional) User login so habits are private
- Everything tested and ready to deploy

You'll build it incrementally — one piece at a time. Each lesson is a step forward.

---

## Before You Write a Single Line of Code — Plan

One of the best habits you can develop when building with AI tools is to plan before you build. Antigravity is very capable, but it needs good direction. A few minutes of planning at the start saves hours of rework later.

This lesson is entirely about planning. No code yet.

---

## The First Prompt — Describe Your App

Start a new session in Antigravity (or continue your existing one in a new project folder). Type:

```
I want to build a Habit Tracker web app. Before we write any code, 
help me plan it out.

Here's what I want it to do:
- Users can add habits they want to track (e.g. "Morning walk", "Read for 20 min")
- Each day, they can check off completed habits
- They can see a streak count for each habit
- Data should be saved in a database so it persists between visits
- It should look clean and work on mobile

What features should we include? What tech stack do you recommend? 
What order should we build things in? Start by asking me any 
clarifying questions you need before making the plan.
```

Antigravity will ask clarifying questions and then produce a plan. This is the conversation stage — respond to its questions, add your preferences, and refine until the plan feels right.

---

## What a Good Plan Looks Like

After the back-and-forth, Antigravity should produce something like:

```
Habit Tracker — Build Plan

Tech Stack:
- Frontend: HTML, CSS, JavaScript (vanilla — no framework)
- Database: Supabase (free tier, Postgres, REST API)
- Deployment: Netlify (free)

Build Order:
1. Frontend — layout, add habits, check off habits (no database yet)
2. Database — connect Supabase, create habits table
3. Persistence — wire app to read/write from Supabase
4. Polish — mobile layout, error handling, UX improvements
5. (Optional) Auth — Supabase login so habits are private
6. Deploy — push to Netlify with a live URL
```

Review it. Adjust it. When it looks like what you want, say:

```
This plan looks good. Let's start with step 1 — the frontend. 
Go ahead.
```

---

## Why We're Using This Tech Stack

**HTML/CSS/JavaScript (vanilla):**
No framework to learn. You can open the files in any browser. It's the simplest possible frontend.

**Supabase:**
- Free tier is generous (500MB database, no credit card)
- Comes with a built-in REST API — no backend code needed
- Has authentication built in if you want to add login later
- Great dashboard for viewing your data

**Netlify:**
- Drag-and-drop deployment (or connect to GitHub for auto-deploy)
- Free tier, no credit card
- Your site is live in under a minute

This stack is deliberately beginner-friendly and production-capable. The apps running on it range from hobby projects to funded startups.

---

## Setting Up Your Project Folder

If you haven't already, ask Antigravity to scaffold the project:

```
Set up a project folder structure for the Habit Tracker. 
Create: index.html, styles.css, app.js, and a README.md 
describing what this project is.
```

Then commit this initial structure:

```
Commit the project setup to Git with the message 
"Sprint 3 — project scaffolded"
```

---

## Understanding What We're Building

Before moving on, make sure you understand the app we're building. Ask Antigravity:

```
Explain the Habit Tracker app we're building as if I'm a complete beginner. 
What does each file do? How do the frontend, database, and deployment 
fit together? Draw me a simple diagram if you can.
```

Read the explanation. Ask follow-up questions. Understanding the shape of what you're building makes the rest of the sprint much smoother.

---

## Summary

- Planning before coding prevents wasted effort
- The Habit Tracker uses vanilla HTML/CSS/JS + Supabase + Netlify
- Start by having Antigravity ask you clarifying questions before it builds
- Set up your project folder and commit the initial structure
- Make sure you understand the overall shape of the app before diving in

**Next:** [Lesson 09 — Building the Frontend](09-building-the-frontend.md)

# Appendix C: Your Own App Guide

---

## How to Adapt This Course to Your Idea

This course is built around a Habit Tracker — but the skills you've learned apply to any web app. This guide walks you through swapping in your own idea.

You have two paths:

**Path 1 — Follow the course first, then rebuild.**
Finish the Habit Tracker to completion. Then use what you learned to build your app from scratch. Recommended for absolute beginners — you'll have a reference point.

**Path 2 — Adapt the course as you go.**
Use the meta-prompt in [Lesson 07B](../07B-choose-your-own-path.md) to have Antigravity rewrite the Sprint 3 & 4 lessons for your app. Continue from there with your customized version.

---

## Step 1: Define Your App

Answer these questions before you do anything else. Be honest with yourself — simpler is almost always better for a first app.

**What does it do in one sentence?**

Write it here:
> My app _______________________________________________

**Who uses it?**
- [ ] Just me
- [ ] A small group of known people
- [ ] The public

**What data does it store?**

List the "things" your app needs to remember. Each becomes a database table.

| Thing | Key fields |
|--|--|
| Example: Books | title, author, date_read, rating |
| *Your item 1* | ... |
| *Your item 2* | ... |

**What are the main screens/pages?**

| Screen | What it shows |
|---|---|
| Home | List of all [things] |
| Add/Create | Form to add a new [thing] |
| Detail | Single [thing] with full info |

**Does it need user login?**
- [ ] No — it's just for me, or the data is public
- [ ] Yes — different users need private, separate data

---

## Step 2: Check the Complexity

Use this table to estimate how complex your app is and how long it'll take:

| Feature | Complexity | Approx. lessons needed |
|---|---|---|
| Display a list of items | Low | 1 |
| Add/delete items | Low | 1 |
| Store data in Supabase | Low | 1–2 |
| User login | Medium | 1–2 |
| Multiple user roles (admin/user) | High | 3+ |
| Real-time updates (see others' changes live) | Medium | 1–2 |
| File uploads (images, PDFs) | Medium | 1–2 |
| Email notifications | Medium | 2–3 |
| Payments | High | 4+ |
| Third-party API integrations | Medium–High | 2–4 |

**Recommendation:** For your first app, aim for Low–Medium complexity across the board. You can always add more later.

---

## Step 3: Run the Meta-Prompt

Once you've answered the questions above, use this prompt to generate a customized course:

```
I'm following the Antigravity Getting Started course, but instead of 
building a Habit Tracker, I want to build: [YOUR APP IN ONE SENTENCE]

Here's a description of my app:
- What it does: [explain]
- Who it's for: [just me / small group / public]
- Main data it stores: [list your tables and fields]
- Main screens: [list your pages]
- Login required: [yes / no]
- Tech stack (same as course): Vanilla HTML/CSS/JS + Supabase + Netlify

Here are the Sprint 3 lessons from the course that I want you to adapt:
[paste the content of lessons 08–12]

Please rewrite these lessons for my app.
Keep the same format and learning structure — just replace all 
Habit Tracker references with my app. Adapt the prompts, examples, 
and exercises accordingly.
```

Save the output — that becomes your customized Sprint 3.

---

## Step 4: Build It the Same Way

Everything else in the course applies directly:

| Course section | Applies to your app? |
|---|---|
| Sprint 1 (setup, first session) | ✅ Yes, identical |
| Sprint 2 (prompts, files, Git, web page) | ✅ Yes, identical |
| Sprint 3 (planning, build, database, auth, polish) | Use your customized version |
| Sprint 4 (deployment) | ✅ Yes, identical |
| Sprint 5 (skills, MCPs, memory) | ✅ Yes, identical |
| Appendix A (prompt library) | ✅ Yes, most prompts are universal |
| Appendix B (troubleshooting) | ✅ Yes, identical |

---

## Example App Substitutions

Here's how some common app ideas map to the course structure:

### Recipe Saver
- **Table:** `recipes` (id, title, ingredients, steps, notes, created_at)
- **Screens:** List of recipes, Add recipe, Recipe detail
- **Login:** Optional — needed only if multiple users
- **Swap habit → recipe everywhere in Sprint 3**

### Reading Tracker
- **Table:** `books` (id, title, author, date_finished, rating, notes)
- **Screens:** My bookshelf, Add book, Book detail
- **Login:** No — personal use
- **Swap habit → book, streak → rating**

### Link Bookmarks
- **Table:** `links` (id, url, title, category, notes, saved_at)
- **Screens:** All links, Add link, Filter by category
- **Login:** Optional
- **Swap habit → bookmark**

### Event Sign-Up System
- **Tables:** `events` (id, name, date, description), `signups` (id, event_id, user_email, name)
- **Screens:** Event list, Event detail (with sign-up form), Admin view
- **Login:** Yes — for admin; sign-up form can be public
- **More complex — aim for Sprint 3 taking twice as long**

---

## If You Get Stuck

When adapting the course to your app and hitting a wall, always remember:

```
I'm building [my app] instead of the Habit Tracker from the Antigravity course.
I'm at the point where the course says: [quote the lesson instruction]
Help me adapt this step for my app.
```

The structure is the same. Only the subject changes.

---

**Good luck. Build something you'll actually use.**

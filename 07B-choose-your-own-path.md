# 🔀 Lesson 07B: Want to Build Something Else?

*This is a bridge lesson between Sprint 2 and Sprint 3. It's entirely optional — skip it if you're happy building the Habit Tracker.*

---

## The Habit Tracker Is Just an Example

The rest of this course builds a Habit Tracker. It's a great learning project because:
- It has a frontend (things you see)
- It has a database (data that saves)
- It can have user login
- It deploys to a real URL

But it's just a vehicle. The *real* thing you're learning is how to use Antigravity to build and ship any app.

If you have a different idea — a portfolio site, a booking tool, a simple SaaS, a community directory, a recipe app — you can build that instead. And Antigravity can adapt this course to help you do exactly that.

---

## How to Swap in Your Own App

The coming lessons (Sprint 3 & 4) are structured around specific prompts for the Habit Tracker. Here's the trick: **you can feed those lessons to Antigravity and ask it to rewrite them for your app.**

Copy and use this meta-prompt at the start of Sprint 3:

```
I'm following the Antigravity Getting Started course, but instead of 
building a Habit Tracker, I want to build [YOUR APP IDEA].

Here are the upcoming course lessons I'm supposed to follow:
[paste the lesson content from 08 through 12]

Please rewrite these lessons — keeping the same structure, the same 
step-by-step format, and the same learning goals — but adapt all the 
prompts, examples, and instructions to apply to my app instead of the Habit Tracker.

Here's a description of my app:
- What it does: [e.g. "A tool for tracking books I've read"]
- Who it's for: [e.g. "Just me, or anyone who wants to track their reading"]
- What data it stores: [e.g. "Book title, author, date finished, rating, notes"]
- Any specific features I want: [e.g. "No login needed, just a public page"]
```

Antigravity will produce a customized version of each lesson, with prompts tailored to your app.

---

## Before You Customize — Answer These Questions

To get the best result, know the answers to these before running the meta-prompt:

**1. What does your app do in one sentence?**
> Example: "It lets me log the books I've read and see my reading stats."

**2. Who is going to use it?**
> Just you? A small team? The public?

**3. What data does it store?**
> List the "things" your app needs to remember. Each becomes a database table.
> Example: Books → title, author, date, rating, notes

**4. What are the main screens or pages?**
> Example: Home page (list of books), Add Book page, Book detail page

**5. Does it need user login?**
> If it's just for you: probably not. If other people will use it: yes.

---

## Example Custom Apps That Work Well With This Course

| App | Data | Login needed? | Complexity |
|---|---|---|---|
| Recipe saver | Recipes: title, ingredients, steps | No (or optional) | Low |
| Reading tracker | Books: title, author, date, rating | No (private use) | Low |
| Link bookmarks | Links: URL, title, tags | Optional | Low |
| Portfolio site | Projects: title, description, link | No | Low |
| Event sign-up | Events, attendees | Yes | Medium |
| Simple blog | Posts: title, content, date | Yes (admin only) | Medium |

If you pick something simple, you'll finish faster. If you pick something medium, you'll learn more. Either is valid.

---

## Once You've Customized

After running the meta-prompt and getting your adapted lessons, use those as your guide through Sprint 3 and 4 instead of the default lessons.

The deployment steps (Sprint 4) apply to nearly any web app, so you probably won't need to customize those.

Sprint 5 (Power User) is also universal — it's about Antigravity features, not your specific app.

---

## Continuing With the Habit Tracker?

If the Habit Tracker works for you — great! Skip this lesson entirely and head to Sprint 3.

The Habit Tracker is genuinely useful and demonstrates everything you need to know. You can always update it into something more personal after the course.

---

**If you're adapting:** Take 15 minutes, define your app above, and run the meta-prompt. Then follow your customized lessons.

**If you're continuing with the Habit Tracker:** [Go to Lesson 08 →](sprint-3-building-the-app/08-planning-your-app.md)

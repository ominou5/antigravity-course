# Lesson 10: Adding a Database With Supabase

---

## Why You Need a Database

Right now, your Habit Tracker keeps habits in memory. Refresh the page — they're gone. Close the browser — gone. That's not a real app.

A **database** is where your app stores data permanently. Add a habit on your laptop, open the app on your phone later — it's still there.

In this lesson, you'll connect your app to **Supabase** — a free, beginner-friendly database service.

---

## What Is Supabase?

Supabase is a cloud database service. You create a project, it gives you a database (PostgreSQL — a professional-grade database used by major companies), and your app talks to it over the internet.

You don't need to understand how databases work in depth. Antigravity will handle the technical parts. You just need to:

1. Set up a Supabase account (free)
2. Copy a connection key into your app
3. Let Antigravity wire everything up

---

## Step 1: Create a Supabase Account

1. Go to [supabase.com](https://supabase.com)
2. Click **Start your project** → sign in with GitHub (easiest) or email
3. Click **New project**
4. Name it `habit-tracker`
5. Choose a region close to you
6. Set a database password (save it somewhere — you won't need it often)
7. Click **Create new project**

Wait about 30 seconds for your project to be provisioned.

---

## Step 2: Get Your API Keys

In your Supabase project:

1. Click **Settings** (the gear icon in the left sidebar)
2. Click **API**
3. Find two values:
   - **Project URL** — looks like `https://xxxx.supabase.co`
   - **anon public key** — a long string starting with `eyJ...`

Copy both. You'll give them to Antigravity next.

---

## Step 3: Tell Antigravity to Connect the App

```
I've set up a Supabase project for our Habit Tracker.
Here are my credentials:

Project URL: [paste your URL]
Anon key: [paste your anon key]

Please:
1. Add the Supabase JavaScript library to my project
2. Create a table in Supabase called "habits" with these columns:
   - id (auto-generated)
   - name (text, required)
   - created_at (timestamp, auto-set)
   - streak (integer, default 0)
   - completed_today (boolean, default false)
3. Update app.js to load habits from Supabase on page load 
   instead of from memory
4. Update the "Add Habit" button to save new habits to Supabase
5. Update the delete button to remove habits from Supabase
6. Update the checkbox to update the "completed_today" field in Supabase
```

This is a substantial task. Antigravity will plan it out, then execute step by step. Review the plan before it starts.

---

## Understanding What Just Happened

After the changes are applied, ask:

```
In plain English, explain how my app now talks to the database.
What happens when I add a habit? What happens when I check one off?
Where does the data actually live?
```

The key concept to understand: your app (running in the browser) sends requests to Supabase over the internet. Supabase stores the data. The next time the app loads, it fetches the data back.

---

## Testing It

Test each action manually:

1. **Add a habit** — does it appear in the list?
2. **Refresh the page** — does the habit still appear? (It should now!)
3. **Check off a habit** — does the checkbox persist on refresh?
4. **Delete a habit** — does it disappear from Supabase too?

To verify data is in Supabase:
1. Go to your Supabase project → **Table Editor**
2. Click the `habits` table
3. You should see your habits listed as rows

If anything doesn't work, copy the error from your browser console (Right click → Inspect → Console tab) and paste it to Antigravity:

```
I'm getting this error in the browser console: [paste error]
What's wrong?
```

---

## A Note on Security

Your Supabase `anon` key is safe to include in frontend code — it's designed for that. However, Supabase's default rules allow anyone with the key to read and write your data.

That's fine for a personal app (only you know the URL). If you're building something public-facing, we address this in Lesson 11 (auth) — only logged-in users will be able to access their own data.

---

## Committing Your Progress

```
Commit all changes with the message 
"Lesson 10 — Supabase database connected"
Then push to GitHub.
```

---

## Try It Yourself

1. Open the app in two different browser windows and add a habit in one. Refresh the other — does it appear?
2. Ask Antigravity: *"Add a 'last completed' date column to the habits table and display it in the UI."*
3. Look at your data directly in the Supabase dashboard — get comfortable with what a database actually looks like.

---

## Summary

- A database saves data permanently — no more losing habits on refresh
- Supabase is free, beginner-friendly, and professional-grade
- You need a Project URL and anon key to connect
- Antigravity handles the database setup and code changes
- Test every action: add, check, delete, and verify data persists

**Next:** [Lesson 11 — Adding User Login *(optional)*](11-adding-user-login.md)

*Or skip to:* [Lesson 12 — Polishing & Testing](12-polishing-and-testing.md)

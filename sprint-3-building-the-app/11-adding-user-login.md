# Lesson 11: Adding User Login *(Optional)*

> **This lesson is optional.** If you just want a personal app that only you use — with one shared habit list — skip to [Lesson 12](12-polishing-and-testing.md). Come back here when you want to make the app multi-user.

---

## Why Add Login?

Right now, your Habit Tracker has one database and one habit list. Anyone who knows your app's URL can see and modify your habits.

That's fine if:
- You're the only user
- The URL is private (not shared publicly)
- You don't need personalized data per user

But if you want:
- Multiple people to use the app with their own private habits
- To share the app broadly without everyone seeing each other's data
- Users to log in from any device and see *their* habits

Then you need authentication.

---

## How Supabase Auth Works

Supabase includes a built-in authentication system. You don't need a separate login service.

It supports:
- Email + password sign-up
- Magic link login (one-click via email)
- Google, GitHub, and other OAuth providers

For this course, you'll use **email + password** — the simplest option.

When a user signs in, Supabase gives your app a **user ID** (a unique token per user). You use this ID to "tag" each habit with its owner — so users only ever see and modify their own habits.

---

## Step 1: Enable Auth in Supabase

In your Supabase dashboard:

1. Click **Authentication** in the left sidebar
2. Click **Providers**
3. Make sure **Email** is enabled (it is by default)
4. Optionally: turn off "Confirm email" for development (you won't need to verify emails while testing)

---

## Step 2: Ask Antigravity to Add Auth

```
I want to add user authentication to my Habit Tracker using Supabase Auth.

Please:
1. Add a sign-up and login form to the app that appears 
   when the user isn't logged in
2. After login, hide the auth form and show the habit tracker
3. Add a "Sign Out" button in the header
4. Update the habits table so each habit has a user_id column 
   linking it to the user who created it
5. Update all database queries so users only see and modify 
   their own habits
6. Set up Supabase Row-Level Security (RLS) so users 
   can't access each other's data even if they try
```

Antigravity will plan this, then implement it step by step. Row-Level Security (RLS) is what makes the data actually safe — it enforces account ownership at the database level.

---

## What Row-Level Security Means

RLS is a database rule that says: *"When user A requests data, only show rows that belong to user A."*

This happens at the Supabase level, not in your JavaScript. Even if someone clever tried to tamper with the app, Supabase would reject requests for data they don't own.

Ask Antigravity to explain the RLS policies it set up:

```
Explain the Row-Level Security rules you just created. 
What do they prevent? What would happen if someone tried to 
access another user's habits without proper auth?
```

---

## Testing Auth

Test the full flow:

1. Open the app — you should see the login form
2. Click "Sign up" and create a test account with a fake email
3. Log in — the habit tracker should appear
4. Add a habit — it should appear in the list
5. Sign out — the habit list should disappear
6. Sign in again — your habit should still be there

**Test multi-user isolation:**
1. Sign up with a second fake account (in a different browser or incognito window)
2. Add a different habit under this account
3. Switch back to the first account — you should *not* see the second account's habits

---

## Committing

```
Commit all changes with the message 
"Lesson 11 — Supabase auth and RLS added"
Then push to GitHub.
```

---

## Try It Yourself

1. Ask Antigravity to add Google sign-in as an alternative to email/password (you'll need to configure it in the Supabase dashboard — Antigravity will walk you through it)
2. Add a "Welcome, [user's email]" message in the header when logged in

---

## Summary

- Login lets multiple users have separate, private habits
- Supabase Auth handles sign-up, login, and user sessions
- Row-Level Security (RLS) enforces data privacy at the database level
- Test with two accounts in separate browser sessions to verify isolation
- This lesson is optional — a single-user app without login is completely valid

**Next:** [Lesson 12 — Polishing & Testing](12-polishing-and-testing.md)

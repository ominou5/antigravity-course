# Lesson 13: Choose Your Deployment Path

---

## Sprint 4 Goal

You have a working, polished, tested app. Now it needs a real URL.

By the end of this sprint, your Habit Tracker will be live on the internet — accessible from any device, anywhere in the world.

---

## What Is Deployment?

Right now, your app lives on your computer. Opening `index.html` in a browser works for you, but nobody else can access it.

Deployment means uploading your app to a server that:
- Is always running (not just when your laptop is on)
- Has a public URL anyone can visit
- Serves your files to anyone who requests them

---

## The Three Options

Choose based on your comfort level. All three are free.

---

### Option A — Netlify Drop (Simplest, Fastest)
**Best for:** Complete beginners. No setup required. Under 60 seconds to go live.

**How it works:** You drag your project folder onto a webpage and Netlify gives you a URL.

**Limitation:** Every time you update your app, you drag and drop again. Fine for now; Option B is better long-term.

**Steps:**
1. Go to [netlify.com](https://netlify.com) and create a free account
2. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
3. Find your project folder on your computer
4. Drag the entire folder onto the Netlify drop zone
5. Wait 10 seconds
6. You have a live URL (e.g. `amazing-fox-12345.netlify.app`)

---

### Option B — Netlify + GitHub (Recommended)
**Best for:** Anyone planning to keep updating their app. Auto-deploys when you push to GitHub.

**How it works:** Netlify watches your GitHub repository. Every time you push a commit, it automatically re-deploys.

**Steps:**
1. Make sure your project is pushed to GitHub (from Lesson 05B)
2. Go to [app.netlify.com](https://app.netlify.com) and sign in
3. Click **Add new site → Import an existing project**
4. Choose **GitHub**
5. Select your `habit-tracker` repository
6. Leave the build settings empty (no build command — it's vanilla HTML)
7. Click **Deploy site**

Done. You get a URL. And from now on: push to GitHub → live site updates automatically.

---

### Option C — Cloudflare Pages (Alternative)
**Best for:** Those who want Cloudflare's global network, or who plan to add more Cloudflare services later (like Workers, R2, etc.)

**How it works:** Same as Netlify + GitHub, but hosted on Cloudflare's network.

**Steps:**
1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Sign in (free Cloudflare account)
3. Click **Create application → Pages → Connect to Git**
4. Select your GitHub repo
5. No build configuration needed for vanilla HTML
6. Click **Save and Deploy**

---

## Handling Environment Variables (Important)

Your app uses a Supabase URL and API key — and right now they're probably written directly in your JavaScript. That's okay for development, but we want to handle this properly for production.

Ask Antigravity:

```
My app has a Supabase URL and anon key hardcoded in app.js. 
How should I handle these as environment variables for deployment 
to [Netlify / Cloudflare Pages]? Walk me through setting them 
up properly so they're not exposed in my GitHub repository.
```

> **For a vanilla HTML/JS app:** the anon key is genuinely designed to be public — it's safe in the frontend. But it's still good practice to use environment variables, especially if you later move to a framework.

---

## What About the Supabase URL?

Supabase is already deployed — it's a cloud service. Your database is already "live." You don't need to deploy Supabase — just make sure your deployed frontend points to the right Supabase credentials.

---

## Custom Domain (Optional, Free)
After deploying, you'll have a URL like `amazing-fox-12345.netlify.app`. That's fine, but you can get a cleaner URL:

**Using a free Netlify subdomain:**
Go to **Site settings → Domain management → Edit site name** and change the subdomain to something like `my-habit-tracker.netlify.app`.

**Using your own domain:**
If you own a domain (from Namecheap, GoDaddy, etc.), Antigravity can walk you through pointing it at Netlify or Cloudflare.

---

## Pre-Deployment Checklist

Before you deploy, ask Antigravity:

```
Do a final check before deployment. Make sure:
1. All files are committed and pushed to GitHub
2. There are no console errors when opening the app locally
3. The Supabase keys are handled correctly
4. The app works with a cleared browser cache
```

---

## Summary

- Three deployment options: Netlify Drop (fastest), Netlify+GitHub (recommended), Cloudflare Pages (alternative)
- All are free with no credit card required
- Supabase is already live — only the frontend needs deploying
- Environment variables keep sensitive keys out of your GitHub repo
- Option B (Netlify+GitHub) means future updates deploy automatically when you push

**Next:** [Lesson 14 — Deploy! Your App Is Live 🎉](14-deploy-your-app-is-live.md)

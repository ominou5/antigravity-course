# Lesson 14: Deploy! Your App Is Live 🎉

---

## This Is the Moment

You've planned, built, connected a database, polished the experience, and chosen your deployment path. Now you actually deploy.

This lesson is the act of going live — and what to do after you have a real URL.

---

## Step 1: Prepare With Antigravity

Before hitting deploy, run a final check:

```
We're about to deploy the Habit Tracker to [Netlify / Cloudflare Pages].
Do a final review:
1. Check all files are committed and pushed to GitHub
2. Look for any obvious issues that would break the app in production
3. Confirm the Supabase connection will work from a different domain
4. Are there any console errors in the current version?

Tell me if anything needs fixing before I deploy.
```

Fix anything it flags, commit, and push.

---

## Step 2: Deploy

Follow the steps from whichever option you chose in Lesson 13.

**Option A (Netlify Drop):**
Drag your project folder to [app.netlify.com/drop](https://app.netlify.com/drop).

**Option B (Netlify + GitHub):**
Your site may already be deploying from your last push. Go to your Netlify dashboard and check. If not, trigger a manual deploy.

**Option C (Cloudflare Pages):**
In your Cloudflare Pages dashboard, check the deployment status. It should have deployed when you pushed.

---

## Step 3: Fix the CORS Issue (If It Happens)

When your app runs on a live URL instead of your local machine, Supabase may reject requests because the domain isn't in its allowed list.

If you see a CORS error or your data doesn't load:

1. Go to your Supabase project → **Authentication → URL Configuration**
2. Add your new URL to **Site URL** (e.g. `https://my-habit-tracker.netlify.app`)
3. Add it to **Redirect URLs** as well

Then tell Antigravity:
```
I'm getting a CORS error on my deployed site. The URL is [your URL]. 
I've added the URL to Supabase's allowed list. 
Is there anything else I need to update?
```

---

## Step 4: Test the Live App

Open your new URL in a browser and test everything:

- [ ] The page loads without errors
- [ ] You can add a habit
- [ ] The habit persists after refresh
- [ ] If you added auth: login and logout work
- [ ] The app looks correct on mobile

If anything is broken:

```
I deployed to [URL] and found this issue: [describe problem].
The local version works fine. What could cause it to break in production?
```

---

## Step 5: Share It

Your app is live. Share the URL with at least one person — whether it's a friend, a collaborator, or just yourself on another device.

There's something real about a live URL. It changes how you think about what you built.

---

## Update Your README and Commit

```
Update README.md to include the live URL: [your URL].
Then commit with the message "Deployed — app is live at [URL]" and push.
```

---

## What's Next for Your App?

Now that it's live, you can keep building. Ideas:

- Add a way to reset streaks each day at midnight
- Send yourself an email reminder if you haven't checked in by evening
- Add a simple analytics page showing your best streaks
- Let someone else sign up and use it
- Turn it into a mobile app (Antigravity can help with that too)

Every change is one git push away from being live.

---

## Summary

- Run a final check with Antigravity before deploying
- Fix CORS errors by updating the allowed URL in Supabase settings
- Test the live app thoroughly — it may behave differently than local
- Update README with your live URL and commit
- Congratulations — you shipped something real 🚀

---

## 🎉 You just shipped a full-stack web app.

It has:
- A frontend (HTML, CSS, JavaScript)
- A cloud database (Supabase)
- A live URL (Netlify or Cloudflare)
- Version control (Git + GitHub)
- Optional: user authentication

That's the full stack. That's what real apps are made of.

**Next:** [Sprint 5 — Power User →](../sprint-5-power-user/15-skills-commands-workflows.md)

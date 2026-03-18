# Appendix B: Troubleshooting

Common problems and how to fix them with Antigravity's help.

---

## Antigravity Issues

### "Antigravity isn't understanding what I want"

The problem is almost always in the prompt. Try:

1. **Add more context:** Tell it what you're building and why
2. **Be more specific:** Replace vague words ("make it better") with concrete ones ("increase font size and add more padding")
3. **One thing at a time:** Split your request into two separate prompts
4. **Restate it differently:** If it misunderstood once, rephrase rather than repeating

```
I don't think I explained that clearly. Let me try again.
What I actually want is: [restate the request more specifically]
```

---

### "It keeps changing things I didn't ask it to change"

Antigravity sometimes takes initiative. If it's touching files you didn't want changed:

```
You changed [file/thing] but I didn't ask for that.
Please revert that specific change and only modify what I originally asked for.
```

In future prompts, be explicit:
```
Only change [specific thing]. Do not modify anything else.
```

---

### "The session got confused mid-task"

Long sessions can lose context. Re-anchor:

```
Let's pause and reset context. We're working on [project name].
The current goal is [task]. Here's where we are: [brief summary].
Now, let's continue with [next step].
```

---

### "I approved a change and now the app is broken"

First, don't panic. Your Git history is your safety net.

```
The change you just made broke the app. Here's what's wrong: [describe].
Can you revert the last changes and restore the app to working state?
```

If you're using Git:
```
What was the last commit before this broke? 
How do I revert to that state?
```

---

## App & Code Issues

### "The app works locally but breaks when deployed"

This is the most common deployment problem. Usually caused by:

**1. CORS error (Supabase rejects requests from the live domain):**
- Go to Supabase → Authentication → URL Configuration
- Add your live URL to Site URL and Redirect URLs

```
I deployed to [URL] and Supabase seems to be blocking requests.
I've added the URL to Supabase's allowed list.
Is there anything else that needs updating?
```

**2. Missing environment variables:**
If you moved API keys to environment variables, check they're set in Netlify/Cloudflare dashboard under Environment Variables.

**3. File path issues:**
Local files sometimes use paths that break on a live server.
```
My app works locally but images/fonts/files aren't loading on the deployed version.
The live URL is [URL]. What path issues might cause this?
```

---

### "Console errors I don't understand"

Copy the exact error and paste it:

```
I'm getting this error in the browser console:
[paste the full error text]

What does this mean and how do I fix it?
```

> **How to open the browser console:** Right click anywhere on the page → "Inspect" → click "Console" tab

---

### "Supabase won't connect"

```
My app can't connect to Supabase. Here's the error: [paste error].
My Supabase URL is: [URL]
What could cause this?
```

Common causes:
- Typo in the URL or anon key (copy them again from Supabase settings)
- RLS is blocking the query (check your Row-Level Security policies)
- No active session when RLS expects one (are you logged in?)

---

### "My data isn't saving to Supabase"

```
When I [action], the data isn't saving to Supabase.
No error shows in the console.
Here's the relevant code in app.js: [paste the function]
What's wrong?
```

Check the Supabase **Table Editor** directly to see if rows are showing up there. If yes, the problem is the frontend reading. If no, the problem is the write.

---

### "The app looks broken on mobile"

```
My app looks broken on [phone/small screen].
Specifically: [describe what's wrong — e.g. the text overflows, buttons overlap].
Fix the CSS so it works properly on small screens.
```

To simulate mobile in your browser: Right click → Inspect → click the phone/tablet icon in the top left of the inspector panel.

---

## Git & GitHub Issues

### "I can't push to GitHub — authentication failed"

```
I'm getting an authentication error when pushing to GitHub.
The error says: [paste error]
Help me fix my GitHub credentials.
```

Modern GitHub requires a Personal Access Token (PAT), not your password.
Antigravity will walk you through generating one.

---

### "I accidentally committed something I shouldn't have"

```
I accidentally committed [describe — e.g. a file with my API keys].
How do I remove it from my commit history?
```

> **Important:** If you committed actual secret keys, change them immediately in Supabase (generate new anon keys) — even after removing from Git, the old keys should be considered compromised.

---

### "My Git history is a mess / I have merge conflicts"

```
I'm seeing merge conflicts in my repository.
Here's the error: [paste]
Walk me through resolving this safely without losing my work.
```

---

## Deployment Issues

### "Netlify deployment failed"

```
My Netlify deployment failed. Here's the build log: [paste the log]
What went wrong and how do I fix it?
```

For vanilla HTML/JS projects: there should be no build step. If Netlify is trying to run a build command, clear it in Site Settings → Build & Deploy → Build command (leave it empty).

---

### "My custom domain isn't working"

```
I pointed my domain [domain] to Netlify but it's not working.
The domain registrar is [Namecheap/GoDaddy/Cloudflare/etc].
Walk me through the DNS settings I need to configure.
```

DNS changes can take up to 48 hours to propagate. If it's been less than that, wait.

---

## When Nothing Works

Sometimes you hit a wall. When that happens:

```
I'm stuck. Here's everything I've tried: [list what you tried].
Here's the current state of the problem: [describe clearly].
Here's what I expected vs. what's happening: [describe the gap].
Let's start from scratch on this specific issue. What are all the 
possible causes? Let's eliminate them one by one.
```

Methodical debugging always wins. If you're still stuck, bring the problem with all context to the Antigravity community.

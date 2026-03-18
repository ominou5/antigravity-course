# Lesson 09: Building the Frontend

---

## What Is the Frontend?

The **frontend** is everything the user sees and interacts with — the visual layout, the buttons, the list of habits, the checkboxes. It's the experience before any data is involved.

In this lesson, you'll build the frontend of the Habit Tracker using HTML, CSS, and JavaScript. There's no database yet — habits will only exist while the page is open. That comes in the next lesson.

Building frontend first is smart: it lets you see how the app will look and feel before wiring it to anything. It's also easier to change the visual design before the plumbing is in place.

---

## The Starting Prompt

In Antigravity, start with:

```
Build the frontend for a Habit Tracker app with these features:

1. A header with the app title "Habit Tracker"
2. A text input and "Add Habit" button where users type a new habit name
3. A list that shows all habits added so far
4. Each habit in the list has:
   - The habit name
   - A checkbox to mark it as completed today
   - A "streak" counter showing 0 (placeholder for now)
   - A delete button to remove it
5. Clean, modern design — dark background preferred
6. Must work on mobile (responsive layout)

Use HTML, CSS, and vanilla JavaScript. 
Save as index.html, styles.css, and app.js.
```

Review the proposed files and approve them.

---

## Open It in Your Browser

After the files are created:
1. Open the file explorer
2. Right-click `index.html` → Open with Browser

You'll see your Habit Tracker interface. Try adding a habit. Try checking it off. Try deleting one.

Notice: none of this saves anywhere yet. Refresh the page and your habits are gone. That's expected — we fix it in Lesson 10.

---

## Iterating on the Design

Now refine. The first version is never the final version. Some prompts to try:

**Layout improvements:**
```
The habit list looks a bit bare. Add a subtle background card to each 
habit item and add some padding so they feel more distinct.
```

**Visual polish:**
```
Use the Google Font "Inter" for the entire app. 
Increase the font size for habit names and make the streak counter 
appear as a small badge in a contrasting color.
```

**Empty state:**
```
When there are no habits yet, show a friendly message in the habit list area 
saying "No habits yet — add your first one above!"
```

**Streak interaction:**
```
When a habit is checked off today, change the checkbox color to green 
and increase the streak count by 1. When it's unchecked, decrease it by 1 
(minimum 0).
```

---

## Understanding What Was Built

After you're happy with the visual result, ask Antigravity to explain what it built:

```
Walk me through what app.js does, step by step. 
Explain it like I've never coded before.
```

You don't need to memorize this. But understanding the code that runs your app is valuable — it'll help you give better instructions and debug problems later.

---

## Common Frontend Issues and How to Fix Them

**Something doesn't look right:**
```
The [element] looks off — [describe the problem]. 
Can you fix it? Show me the change before applying.
```

**Something doesn't work when I click it:**
```
When I click [button], nothing happens. 
Can you check app.js and find out why?
```

**It looks fine on desktop but broken on mobile:**
```
Check the CSS and make sure the layout is fully responsive. 
I'm on a [phone / small screen] and [describe what's breaking].
```

**I want to change the color scheme:**
```
Change the color scheme to use [description]. Keep the layout the same.
```

---

## Committing Your Progress

When you're happy with the frontend, commit:

```
Commit all my changes to Git with the message 
"Lesson 09 — habit tracker frontend complete"
Then push to GitHub.
```

---

## Try It Yourself

After building the initial frontend, push yourself with these challenges. Ask Antigravity to help you implement each one:

1. **Add a "Complete All" button** that checks off every habit at once
2. **Add a habit count** in the header showing "3 habits tracked today"  
3. **Add a simple animation** when a new habit is added to the list

Each of these is one prompt away.

---

## Summary

- The frontend is the visual layer — what users see and interact with
- Build frontend first, database second
- Use the feedback loop: describe → preview → approve → check in browser → refine
- Understand the code Antigravity writes — ask it to explain as it goes
- Commit after each meaningful improvement

**Next:** [Lesson 10 — Adding a Database](10-adding-a-database.md)

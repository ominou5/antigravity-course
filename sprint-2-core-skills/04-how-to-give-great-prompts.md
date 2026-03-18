# Lesson 04: How to Give Great Prompts

---

## Why Prompts Matter So Much

Antigravity is as useful as your ability to direct it. The AI is extremely capable — but it needs good instructions to produce great results.

The good news: writing better prompts is a learnable skill, and it doesn't require any technical knowledge. It just requires clear thinking and a little practice.

---

## The Three Parts of a Great Prompt

Every effective prompt has three components:

### 1. Context — What's the situation?
Tell Antigravity what you're working on. What already exists? What's the goal?

### 2. Task — What do you want it to do?
Be specific about the action you want taken.

### 3. Constraints — What matters to you?
What should it avoid? What style, format, or limitation applies?

You don't need all three every time — but when things go wrong, one of these is usually missing.

---

## Before and After: Examples

**Bad prompt:**
```
Make my website better.
```
What does "better" mean? Faster? Prettier? Easier to navigate? Antigravity will guess — and might guess wrong.

**Good prompt:**
```
My website has a white background and plain text. 
Make it look more modern: add a dark background, 
use a sans-serif font, and center the text on the page.
```

---

**Bad prompt:**
```
Add a database.
```
Which database? What data does it store? What should it do?

**Good prompt:**
```
I have a habit tracker app. Add a Supabase database to it.
Create a table called "habits" with columns: id, name, created_at, and user_id.
Then update the app to save new habits to this table instead of storing them in memory.
```

---

**Bad prompt:**
```
Fix the bug.
```
Which bug? What's happening? What did you expect to happen?

**Good prompt:**
```
My app crashes when I click the "Add Habit" button. 
The error message says: "Cannot read properties of undefined (reading 'push')"
Here's the relevant function: [paste function]
What's wrong and how do I fix it?
```

---

## Useful Framing Phrases

These phrases consistently get better results:

| Instead of... | Try... |
|---|---|
| "Make it better" | "Improve the visual design — specifically the typography and spacing" |
| "Add a feature" | "Add a button that, when clicked, does X and updates Y" |
| "Fix this" | "This isn't working as expected. I expected X, but I'm seeing Y. Here's the context: [...]" |
| "Build an app" | "Build a [type] app that does [core function]. Start with just the [first feature], nothing else yet." |

---

## The "One Thing at a Time" Rule

The most common beginner mistake is asking for too much at once.

**Too much:**
```
Build me a complete habit tracker with a homepage, login screen, 
dashboard, database, mobile layout, dark mode, and an email reminder system.
```

**Right size:**
```
Start by building the homepage for a habit tracker. 
It should have a header, a list of habits, and a button to add a new one. 
No database yet — just the visual layout.
```

After Antigravity finishes, review it. Then ask for the next piece.

Small, focused requests produce better code with fewer mistakes.

---

## Telling Antigravity Your Experience Level

Antigravity adjusts its explanations based on context. Tell it who you are:

```
I'm new to coding — please explain what you're doing as you go,
and use plain English instead of jargon.
```

Or:
```
I'm a developer comfortable with JavaScript. You don't need to 
explain basic concepts — just focus on the implementation.
```

You can change this at any time during a session.

---

## When It Gets Something Wrong

Antigravity makes mistakes. When it does:

1. **Don't start over** — just tell it what's wrong
2. **Be specific** — "The button is red but I wanted blue" beats "That's not right"
3. **Paste error messages verbatim** — exact error text helps more than your description of the error

```
That's not quite what I wanted. The habit list should be vertical, 
not in a grid. Also the button color should be green, not blue. 
Can you fix both of those?
```

---

## Try It Yourself

Open Antigravity and practice improving these prompts. Ask Antigravity to help you:

**Exercise 1:** Submit this bad prompt:
```
Make me an app.
```
Then ask:
```
That was too vague. Help me write a better, more specific version of that prompt 
for a simple recipe-saving app.
```

**Exercise 2:** Write your own prompt for something you actually want to build — then ask Antigravity to critique it:
```
Here's a prompt I want to use: [your prompt]
Is this clear enough? What information am I missing that would help you do a better job?
```

---

## Summary

- Great prompts have: **context**, **task**, and **constraints**
- Be specific — vague instructions produce vague results
- Ask for one thing at a time, especially early on
- Tell Antigravity your experience level so it calibrates its explanations
- When something goes wrong, describe the problem specifically and correct course

**Next:** [Lesson 05 — Working With Files & Projects](05-working-with-files.md)

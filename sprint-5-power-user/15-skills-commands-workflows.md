# Lesson 15: Skills, Commands & Workflows

---

## Welcome to the Power User Sprint

Sprints 1–4 got you from zero to a live app. This sprint is about going deeper — unlocking Antigravity's advanced features to work faster, smarter, and more powerfully.

These aren't required for beginners. But they're what separates someone who uses Antigravity occasionally from someone who builds with it every day.

---

## Skills

**Skills** are pre-built capabilities you can install into Antigravity. Think of them as plugins — each one adds a specific new ability.

Examples of what skills can do:
- Find and install other skills automatically
- Run security audits on your code
- Generate image assets
- Connect to specialized services
- Follow a specific workflow for a task type

### How to Find and Install a Skill

```
What skills are available that I could install to help with my project?
```

Or if you know what you want:

```
Find a skill that helps with [task — e.g. "code security auditing"] 
and install it.
```

Antigravity will find, review (for safety), and install the skill into your workspace.

### Running a Skill

Once installed, activate a skill with a slash command:

```
/SKILL [skill-name] [optional instructions]
```

For example:
```
/SKILL find-skills I want to find skills for Firebase integration
```

---

## Slash Commands

Slash commands are shortcuts for common Antigravity actions. Type `/` in the chat to see what's available.

Key built-in commands:

| Command | What it does |
|---|---|
| `/SKILL` | Activate an installed skill |
| `/PROMPT` | Use a saved prompt template |
| `/ANALYSIS` | Run analysis on your code or project |
| `/clear` | Clear the chat history on screen |

You can also ask Antigravity what commands are available:

```
What slash commands are available to me right now?
```

---

## Workflows

A **workflow** is a set of repeatable steps saved as a file. Once a workflow exists, you can trigger it with a single command and Antigravity will execute all the steps automatically.

**Example use cases for workflows:**
- "Every time I start a new feature, run these 5 setup steps"
- "Before I deploy, run this checklist automatically"
- "Whenever I create a new component, scaffold it this way"

### Creating a Workflow

Tell Antigravity what repeatable process you want to automate:

```
I find myself doing these steps every time I start a new feature:
1. Create a new git branch
2. Update the README to mention the new feature
3. Create a placeholder file for the feature

Can you create a workflow that automates these steps so I can 
trigger them with a single command in the future?
```

Antigravity will create a workflow file in your `.agent/workflows/` folder. You can then trigger it with:

```
/workflow [name]
```

### Turbo Mode

Workflows can be marked with `// turbo` or `// turbo-all` to run steps automatically without asking for permission at each step. Use this only for steps you fully trust.

---

## Building Your First Workflow

Here's a practical workflow to create right now:

```
Create a workflow called "lesson-commit" that:
1. Checks git status to see what changed
2. Commits all changes with a message I provide
3. Pushes to GitHub
4. Prints a success message

I want to be able to run this at the end of every lesson with a single command.
```

After creation, test it:

```
/workflow lesson-commit message="Lesson 15 — skills and workflows"
```

---

## Try It Yourself

1. **Find a skill related to your project:**
   ```
   What skills exist that could improve my Habit Tracker? 
   Find and describe 2-3 options.
   ```

2. **Create a quality-check workflow:**
   ```
   Create a workflow that runs a quality check on my project:
   - Read all JavaScript files and look for obvious bugs
   - Check that README is up to date
   - Verify no console.log statements were left in production code
   ```

---

## Summary

- Skills are installable capabilities that extend what Antigravity can do
- Slash commands are shortcuts — type `/` to see what's available
- Workflows are saved sequences of steps you can trigger on demand
- The `// turbo` annotation lets steps run automatically without approval
- These features let you operate at a much higher level of speed and consistency

**Next:** [Lesson 16 — MCP Servers](16-mcp-servers.md)

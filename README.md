# 🧠 claude-skills

> A personal library of Claude skills — built to make AI work *with* your team's growth, not against it.

---

## What are Claude Skills?

Claude Skills are custom instruction sets that shape how Claude behaves in specific situations. Instead of prompting from scratch every time, a skill activates automatically based on context — making Claude a smarter, more intentional collaborator.

Think of them as **standing orders for your AI** — written once, applied consistently.

---

## Philosophy

> *"AI should be a teacher, not a crutch."*

This repo was built on a simple belief: speed without understanding is just technical debt with a smile.

In the age of AI, the real competitive advantage isn't how fast you can prompt — it's how much your team actually **grows** through every interaction. These skills are designed with that in mind.

---

## 📁 Skills

### [`co-ops-coding`](./co-ops-coding/SKILL.md)
**Code Comprehension & Learning Skill**

The flagship skill. Built to ensure that every AI-assisted code change becomes a genuine learning moment — not just a shortcut.

| Feature | Description |
|---|---|
| 🔍 Change Summary | Breaks down every change in plain language before asking anything |
| 🧩 Concept Tagging | Tags the real CS concepts touched (async, indexing, render cycles...) |
| ❓ Deep Quiz | Asks *why*, not just *what* — one question at a time |
| 🔄 Retry Loop | Wrong answers get explained and retried, never just revealed |
| 🎓 Teach It Back | Final challenge: explain the change to a teammate in 3–5 sentences |
| 🟡 Lightweight Mode | Small changes (1–5 lines) or frustrated devs get a self-rating check-in |
| 🔴 Frustration Override | Fully skips the quiz when the developer is clearly overwhelmed |

> *"Are your junior developers shipping code — or actually becoming engineers?"*

---

## 🚀 How to Use

### In Claude.ai
1. Go to **Settings → Custom Instructions** (or your Project's instructions)
2. Copy the contents of the skill's `SKILL.md`
3. Paste it into your instructions
4. Start a conversation — the skill activates automatically

### Folder Structure

```
claude-skills/
├── README.md
├── co-ops-coding/
│   ├── SKILL.md          ← The skill instructions
│   └── references/
│       └── question-bank.md  ← Extended quiz question templates
└── [your-next-skill]/
    └── SKILL.md
```

### Adding a New Skill

```bash
mkdir my-new-skill
touch my-new-skill/SKILL.md
```

Each `SKILL.md` follows this structure:

```markdown
---
name: skill-name
description: >
  When to trigger this skill. Be specific — Claude uses this
  to decide when to activate it.
---

# Skill Name

## When to Trigger
## Workflow
## Rules
```

---

## 🛠️ Skill Design Principles

When building a new skill, keep these in mind:

**1. Trigger precision matters**
The description frontmatter is how Claude knows when to activate. Be specific about *what the user says* that should fire the skill — not just what it does.

**2. Never skip the summary phase**
Whatever the skill does, always give the user context before asking anything of them. Orientation first, action second.

**3. Build in escape hatches**
A skill that frustrates users gets disabled. Always include a graceful fallback — lightweight mode, skip options, or defer-to-later paths.

**4. Questions over answers**
The best skills don't just do things — they make the user think. Where possible, ask before telling.

**5. Close every session with what was learned**
A completion summary that names the concepts touched gives users a sense of real, accumulating knowledge.


<p align="center">
  <i>Built with the belief that AI should make your team smarter — not dependent.</i>
</p>

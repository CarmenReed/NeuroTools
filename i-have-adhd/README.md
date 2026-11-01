# 🧠 i-have-adhd (NeuroTools version)

ADHD-friendly answers from Claude Code and Cursor. Action first. Numbered steps. No fluff.

> 📜 Adapted from [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) by Ayoub Ghriss, MIT License. This is our own modified version. See [LICENSE](LICENSE).

## ✨ What changed from the original

- ➕ 4 new rules: no em dashes in anything you keep or copy, emojis welcome, honesty over people pleasing, mobile warnings upfront
- ✏️ Unclear requests: ask **all** clarifying questions first (original said ask one)
- ✏️ One-line recap allowed, to confirm a decision
- ✂️ Removed: adapters for Codex, OpenCode, Gemini, Qwen, Kimi, Pi, OMP, Grok
- ✂️ Removed: GitHub auto-checks, translations, logo

## 📋 The rules

Full text in [skills/i-have-adhd/SKILL.md](skills/i-have-adhd/SKILL.md).

1. Lead with the next action
2. Number multi-step tasks
3. End with one concrete next step
4. Suppress tangents
5. Restate state every turn
6. Specific time estimates
7. Make wins visible
8. Matter-of-fact errors
9. Max 5 items per list
10. No preamble, no closers (one-line confirmation recap OK)
11. No em dashes in deliverables (never re-send just to remove one)
12. Emojis welcome
13. Honesty over people pleasing
14. Say upfront if something won't work on mobile

## 🔌 Install in Claude Code

```bash
claude plugin marketplace add CarmenReed/NeuroTools
claude plugin install i-have-adhd@neurotools
```

Restart Claude Code, then type `/i-have-adhd`. Say "stop adhd mode" to turn it off.

⚠️ If you already have the original installed, remove it first, because both use the name `i-have-adhd`:

```bash
claude plugin uninstall i-have-adhd@i-have-adhd
```

### 🔁 Always on (optional)

Create this empty file and the rules load at the start of every session:

```bash
touch ~/.claude/.i-have-adhd-always
```

Delete the file to turn always-on off.

## 🖱️ Install in Cursor

Copy the skill folder into your Cursor skills folder:

```bash
mkdir -p ~/.cursor/skills
cp -r skills/i-have-adhd ~/.cursor/skills/
```

Restart Cursor, then type `/i-have-adhd`.

## 🧪 Testing and grading

- `tests/`: offline unit tests (no AI calls, free)
- `evals/`: grade how well the AI follows the rules. See [evals/README.md](evals/README.md)

Run the tests from this folder:

```bash
python3 -m unittest discover -s tests
```

⚠️ The evals call Claude and cost real money. The guide shows how to set a budget cap.

## 📜 License

MIT. Original work Copyright (c) 2026 Ayoub Ghriss. Modifications Copyright (c) 2026 Carmen Reed.

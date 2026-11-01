# 💰 token-saver (NeuroTools)

Spend fewer tokens in Claude Code. Read less, write less, do only the asked work.

> 📜 Rules partly adapted from [Caveman](https://github.com/JuliusBrussee/caveman) (Apache 2.0, Copyright 2026 Julius Brussee). Not affiliated with or endorsed by Caveman. See [NOTICE](NOTICE).

## ✨ What it does

- 📥 **Read less:** search before opening files, filter test and log output, no re-reading
- 📝 **Write less:** changed lines only, quiet tool runs, short plain sentences
- 🎯 **Do only the asked work:** investigate first, narrowest fix, stop once proven

Full rules: [skills/token-saver/SKILL.md](skills/token-saver/SKILL.md)

🤝 **Works with i-have-adhd.** Turn both on. When they conflict, i-have-adhd wins.

🔒 **Sends nothing anywhere.** It's only a rules file plus an optional local hook.

## 🔌 Install in Claude Code

```bash
claude plugin marketplace add CarmenReed/NeuroTools
claude plugin install token-saver@neurotools
```

Restart Claude Code, then type `/token-saver`. Say "stop token saver" to turn it off.

### 🔁 Always on (optional)

```bash
touch ~/.claude/.token-saver-always
```

Delete the file to turn always-on off.

### 🏢 Manual install (if plugins need IT approval)

Copy the skill folder. No hook, no plugin system:

```bash
mkdir -p ~/.claude/skills
cp -r skills/token-saver ~/.claude/skills/
```

## 💡 Your own habits that save the most

The skill can't do these for you:

1. 🧹 **`/clear` between unrelated tasks.** Old context gets re-sent with every message.
2. 🗜️ **`/compact` in long sessions,** before the context gets huge.
3. 🤖 **Use a cheaper model for simple work.** Switch with `/model`.
4. 🎯 **Be specific up front.** Name the file and the goal, so Claude doesn't have to search.
5. 🪶 **Keep `CLAUDE.md` short.** It loads every session.

## ⚠️ Honest numbers

Not measured yet. Caveman's own tests found that the short-answer style alone saves only about 3% beyond "be concise". Most savings come from reading less and doing less extra work. Run the evals in `../i-have-adhd/evals/` to measure your own savings.

## 📜 License

MIT for our work. Caveman-derived parts: Apache 2.0 (see [LICENSE-APACHE](LICENSE-APACHE) and [NOTICE](NOTICE)).

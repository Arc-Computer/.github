<h1 align="center">Arc — Code’s Collective Memory</h1>
<p align="center"><em>
Keeps track of <strong>what</strong> changed, <strong>why</strong> it changed, and <strong>what might break next</strong>.
</em></p>

<p align="center">
  <a href="https://www.arc.computer">Website</a> •
  <a href="https://github.com/Arc-Computer/arc-whitepaper/blob/main/paper/whitepaper.pdf">📄 Position Paper</a> •
  <a href="#-quick-start">Quick start</a> •
  <a href="#-open-questions">Open questions</a> •
  <a href="#-design-partners">Design partners</a>
</p>

---

## 🚀 What is Arc?

Arc is a **memory layer** for codebases.  

It does three things:

1. **Captures the *why***  
   Every commit, ticket, and design doc is linked to the code it changed.
2. **Predicts the blast-radius**  
   Before you merge, Arc shows which tests, services, or contracts could break.
3. **Feeds that context to agents**  
   Autonomous tools (and our own RL agents) can query the memory to plan long, multi-file refactors.

> **Goal:** Make changing large systems as safe and repeatable as running a test suite.

---

## 🔍 Open questions <a id="-open-questions"></a>

We treat Arc as a research project in the open. Current threads:

| Theme | What we’re asking | Work in repo |
|-------|------------------|--------------|
| **Richer history, fast reads** | How do we store years of code+docs and still answer “why” in &lt; 100 ms? | Prototype graph over Postgres + benchmarks |
| **Safe concurrent edits** | Can two agents land overlapping changes without human re-bases? | First pass at a *causal* CRDT merge rule |
| **Rewarding provenance** | Does giving agents “points” for adding good links speed up long refactors? | Offline RL loop + metrics script |
| **Live, public evaluation** | What does a *real* benchmark for multi-agent coding look like? | **Synapse**: two Gemini-2.5 agents upgrade OpenSSL on a 5-service repo, streamed live |

Read the details in the position paper or open an issue to dive in.

---

## ⚡ Quick start

```bash
git clone https://github.com/Arc-Computer/arc-whitepaper.git
open arc-whitepaper/paper/whitepaper.pdf
````

More code coming soon—star the repo to stay in the loop.

---

## 🤝 Design partners <a id="-design-partners"></a>

We’re looking for teams that:

* Review 20 + PRs a week
* Run safety-critical or legacy code
* Are experimenting with Copilot, Claude, Cursor, etc.

You’ll get hands-on support and help steer the roadmap.
Say hi → **[Jarrod@arc.computer](mailto:Jarrod@arc.computer)**

---

## 🛠 Contributing

Bug reports, research ideas, and pull requests welcome.

---

<p align="center"><em>
Made with ☕ & 🧠 in NYC — let’s give code a memory, together.
</em></p>
```


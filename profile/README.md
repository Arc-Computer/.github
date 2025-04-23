</h1>
<p align="center">
  <em>Arc: The local-first memory layer that surfaces <strong>why</strong> behind every line of code—<br>
  for humans and AI agents alike.</em>
</p>
<p align="center">
  <a href="https://www.arc.computer">Website</a> •
  <a href="#-quick-start">Quick start</a> •
  <a href="#-architecture">Architecture</a> •
  <a href="#-roadmap">Roadmap</a> •
  <a href="#-design-partner-program">Design partners</a>
</p>

---

## 🚀 Our Vision

Software will soon be written **by fleets of autonomous agents collaborating with humans**.  
That future needs a **shared, trusted memory**—one that captures not just _what_ changed, but **_why every decision was made_**.

Arc builds that memory:

* **Temporal Knowledge Graph, in your IDE** – embeds commit history, PR rationales, issues and ADRs directly in VS Code, so every line knows its past.  
* **Agent-ready API** – any LLM or tool can query the graph (`/searchEntity`, `/traceHistory`, `/openFile`, `/runTests`) to plan safe, multi-step fixes.  
* **Local-first & privacy-first** – graphs are built in CI and stay on the developer’s machine; no code or IP leaves your repo.  
* **Verification layer for AI code** – provenance and test execution ensure AI-generated patches don’t reopen old bugs or violate arch decisions.  
* **Foundation for distributed AI systems** – scalable to monorepos and multi-service graphs, aligning with long-context frontier models.

> **Mission:** *Bridge the gap between human decisions and machine understanding, becoming the temporal source-of-truth for every engineering team and their agents.*

---

## 🏗️ Architecture

```text
             ┌─────────────┐   REST/gRPC   ┌──────────────┐
             │  VS Code    │◀──────────────│  Arc MCP     │
             │  Extension  │   decision    │  Server      │
             └─────────────┘   trails      └──────────────┘
                    ▲                               ▲
      hover & UI    │                               │ tools/manifest.json
                    │                               │ agent calls
             ┌──────┴──────┐                 ┌──────┴──────-┐
             │  Graph DB   │◀───────────────▶│  Agents      │
             │ (SQLite+FTS)│  local access   │ (Copilot,…)  │
             └─────────────┘                 └──────────────┘
                       ▲
                       │ arc build
                       │
             ┌─────────────────┐
             │  GitHub CI      │  read-only API
             │  + GitHub App   │──────────────▶ PRs / Issues
             └─────────────────┘
```

---

## 🔭 Roadmap

| Phase | Focus | ETA |
|-------|-------|-----|
| **v0.9** | Local TKG, MCP tools, VS Code hover/timeline | May 2025 |
| **v1.0** | Vector search plug-in, GitLab ingest, workspace-wide risk badges | Q3 2025 |
| **v1.1** | Cloud opt-in sync, org dashboards, policy engine | Q4 2025 |

---

## 🤝 Design Partner Program

We’re onboarding **3–5 engineering teams** who:

* Review ≥ 20 pull requests per week  
* Run security-critical or legacy-heavy codebases  
* Want to experiment with AI agents (Cursor, Copilot, etc.)

Design partners get 1-on-1 integration support and influence the roadmap.  
[Apply here](mailto:jarrod@arc.computer) →

---

## 🛠  Contributing

Arc Memory is open-source _in layers_:

* `arc-memory` (MIT) – core library & CLI 
* `arc-memory-mcp` (MIT) – edge server + tools  
* `arc-extension` (MIT) – VS Code / IDE extension

Bug reports, feature requests, and pull requests are welcome!  
See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for coding standards and CLA.

---

## 📝 License

This repository is licensed under the MIT License.

---

### About

Arc is building the **memory layer for engineering teams and their agents**—starting in VS Code.  
Made with ☕ & 🧠 in New York & remote.

```

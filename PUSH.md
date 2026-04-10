# Push to GitHub — AgnosticObsidian

## 1. Create the repo on GitHub

```bash
# Go to https://github.com/new
# Repo name: agnostic-obsidian
# Description: "Universal AI agent memory layer — vault + palace + temporal knowledge graph. Works with OpenClaw, Claude Code, Codex, Gemini CLI."
# Public or Private: Public (more discoverable)
# Don't initialize with README (we have one)
```

## 2. Push the code

```bash
cd /home/ubuntu/.openclaw/workspace/agent-memory-repo

git remote add origin https://github.com/YOUR_USERNAME/agnostic-obsidian.git
git branch -M main
git push -u origin main
```

## 3. Verify

```bash
git remote -v
# Should show: origin  https://github.com/YOUR_USERNAME/agnostic-obsidian.git
```

---

## For Claude Code Working on This Repo

See `CLAUDE.md` — has the full context including:
- Package structure
- All APIs (core, palace, KG, hooks, classifier, semantic)
- MCP server tools
- Development workflow
- How to add message types and custom hooks

---

## Deployability Assessment

### Production-Ready
- Core memory system (vault + palace + KG)
- 14 CLI commands
- MCP server (15+ tools)
- Python API with full type hints
- Graceful fallbacks
- Lazy model loading
- MIT licensed

### Needs Work Before Benchmarking
1. **Benchmark**: Run LongMemEval to get R@5 score (MemPalace got 96.6%)
2. **Tests**: No pytest suite yet
3. **PyPI**: Not published
4. **CI/CD**: No GitHub Actions yet

---

## Quick Start After Push

```bash
# Clone
git clone https://github.com/YOUR_USERNAME/agnostic-obsidian.git
cd agnostic-obsidian

# Install
pip install -e ".[all]"    # All dependencies
# or
pip install -e "."           # Core only

# Initialize a vault
ao init ./workspace

# Run session
ao session-start

# Classify a message
ao classify "We decided to go with Postgres"

# Search
ao search "authentication decisions"

# Palace navigation
ao wings
ao rooms Orion

# Knowledge graph
ao kg-query Kai
ao kg-timeline Orion
```

### MCP Server (Claude Desktop)

```bash
# Add to Claude Desktop
claude mcp add agnostic-obsidian -- python -m agnostic_obsidian.mcp_server

# Then use tools in Claude:
# /oao_session_start, /oao_classify, /oao_search, /oao_kg_query, etc.
```

---

## What This Demonstrates

| Skill | Evidence |
|-------|----------|
| Python package architecture | pyproject.toml, module structure, __init__.py exports |
| API design | Clean public API, dataclasses, type hints |
| CLI development | typer + rich, 14 commands |
| MCP protocol | JSON-RPC server, 15+ tools |
| Semantic search | sentence-transformers, local embeddings |
| Knowledge graph | Temporal SQLite KG with validity windows |
| Palace structure | Wings/rooms/closets/drawers/halls/tunnels |
| Text classification | 15 types, regex + multilingual patterns |
| Lifecycle hook patterns | 5 hooks with budgets and context |
| Memory system design | Tiered context, verbatim storage, KG integration |
| Hybrid architecture | obsidian-mind + MemPalace synthesis |

**Good for**: AI engineering roles, agent frameworks, developer tooling, quant trading infrastructure, memory systems.

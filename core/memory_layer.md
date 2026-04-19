# Memory Layer — Palace Architecture for SAI

> Inspired by [MemPalace](https://github.com/MemPalace/mempalace). Adapted for SAI's prompt-based, session-to-session workflow.

---

## The Problem

SAI forgets between sessions. Summaries lose signal. Re-explaining context wastes tokens and degrades quality.

**Solution**: Store verbatim. Retrieve by meaning. Organize like a palace.

---

## 🏛 Palace Structure

```
Memory Palace
│
├── Wings/          ← People, Projects, Long-term work
│   ├── [project_name]/
│   └── [person_name]/
│
├── Rooms/          ← Topics, Themes, Domains
│   ├── [topic]/
│   └── [domain]/
│
└── Drawers/        ← Specific content, decisions, outputs
    ├── [decision_log]
    ├── [key_insight]
    └── [session_export]
```

**Rule: Store verbatim. Never paraphrase. Never summarize.**
Paraphrasing loses nuance. The original phrasing is the signal.

---

## 📥 Storing Memory

### `.memory_save [wing/room] [label]`

Saves the current context fragment or a selected block.

```
.memory_save projects/SAI "audit findings session 3"
```

Output — a formatted block you copy and store externally (file, Obsidian note, etc.):

```markdown
## MEMORY — projects/SAI — audit findings session 3
**Date**: [session date]
**Source**: SAI session
**Content** (verbatim):
[exact text of the saved fragment]

**Tags**: [auto-extracted keywords]
**Retrieval query**: "SAI audit disconnections findings"
```

---

## 🔍 Retrieving Memory

### `.memory_load [natural language query]`

You paste previously saved memory blocks at the top of the session, then call `.memory_load` to activate them:

```
.memory_load "what decisions did I make about SAI structure"
```

SAI scans the injected blocks, selects relevant ones, and activates them as working context.

---

### `.memory_search [term]`

Searches injected memory blocks by keyword or concept.

```
.memory_search "session protocol"
```

Returns: matched blocks with relevance score and original verbatim content.

---

### `.memory_export`

Exports entire current session as a formatted memory block ready for long-term storage.

```
.memory_export
```

Outputs: structured block in palace format (wing/room auto-suggested based on content).

---

## 🔄 Cross-Session Workflow

```
Session 1
  → Work, decisions, insights
  → .memory_export → save to Obsidian/file
  
Session 2
  → Paste saved memory blocks at start of chat
  → .memory_load "relevant query"
  → SAI reconstructs context from verbatim originals
  → Continue without re-explaining
```

---

## 🧩 Integration with Existing Commands

| Memory command | Extends / relates to |
|---------------|---------------------|
| `.memory_save` | Extends `.data_add` — structured tagging + palace location |
| `.memory_load` | Extends `.sync` — semantic activation, not just injection |
| `.memory_search` | Extends `.flow` — applied to stored content |
| `.memory_export` | Extends `.export_context` — full palace-format output |

---

## 📐 Storage Principles

1. **Verbatim over summary.** Never rewrite stored content.
2. **Tag for retrieval.** Each block needs: topic, project, date, key terms.
3. **Palace location.** Always assign wing + room — prevents flat-corpus search failure.
4. **Small blocks.** One idea per drawer. Not entire sessions in one block.
5. **Date everything.** Memory decays in meaning without temporal anchoring.

---

## 🔗 Related

- `core/session_protocol.md` — When to export, when to start fresh
- `core/commands.md` — `.memory_save`, `.memory_load`, `.memory_search`, `.memory_export`
- `.data_add`, `.sync` — lower-level data commands this extends

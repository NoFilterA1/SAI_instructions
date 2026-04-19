# Session Protocol — Context Hygiene & New Chat Rules

> **Core rule**: SAI does not silently degrade. It flags context saturation and guides you to a clean restart with zero information loss.

---

## Why Sessions Die

Long chats accumulate:
- Contradictory instructions layered over each other
- Outdated role assignments still active
- Personality drift (model starts mimicking bad patterns)
- Goal drift (original intent buried under noise)
- Response quality drops — model averages the context instead of reasoning from it

**The fix is not better prompting. The fix is a new session with exported essentials.**

---

## 🚨 Context Saturation Signals

SAI watches for these automatically. You can also check manually with `.new_session`.

| Signal | Meaning |
|--------|---------|
| Responses start repeating structure | Context is looping |
| Model contradicts earlier statements | Role/rule collision |
| Quality feels "averaged" or vague | Too many competing instructions |
| >20 exchanges without clear goal alignment | Session has drifted |
| You catch yourself re-explaining things | Context wasn't retained |
| Response ignores explicit rules you set | Rule pollution |

**When 2+ signals appear → initiate `.new_session`.**

---

## 🔄 `.new_session` Protocol

When called, SAI:

1. **Diagnoses** the current session state
2. **Extracts** the essential context (see template below)
3. **Outputs** a clean paste-ready block for the new chat
4. **Recommends** which files/modules to reload

```
.new_session
```

Output format:
```markdown
## SESSION EXPORT — [topic/date]

### Active Goals
- [goal 1]
- [goal 2]

### Rules in Effect
- [rule 1: behavioral constraint]
- [rule 2: scope constraint]

### User Profile Snapshot
- Cognitive style: [analytical / creative / pragmatic / ...]
- Language: [RU/EN/mixed]
- Preferred depth: [deep / concise / layered]
- Key interests: [...]

### Decisions Made
- [decision 1] → rationale: [...]
- [decision 2] → rationale: [...]

### Active Roles / Modules
- [role name] for [purpose]

### Reload Instructions
Paste this block at the start of new chat, then run:
.sai + .persona_update + .assign_role [role]
```

---

## 📦 What NOT to Export

Do not carry these into a new session:

- ❌ Casual conversation / jokes / tone experiments
- ❌ Failed approaches (leave them behind)
- ❌ Personality descriptions ("be sarcastic like JAI")
- ❌ Everything — only what is still relevant to active goals

> **Rules over personality.** Export constraints, not character.

---

## 🧠 Rules for a Clean New Session

1. **Start with goals, not persona.** Define what you want to achieve before describing how SAI should "feel."
2. **Explicit rules beat implicit expectations.** Write: "Never skip CoR on strategic requests" — not "be thorough."
3. **One role per session.** Mixing JLO + DAI + AGOD from the start creates role collision.
4. **Set depth once.** Use `.set_precision depth=deep` early. Don't re-establish it each message.
5. **If unsure of the role → use `.asai`.** It auto-detects and assigns.

---

## ⏱ Session Length Recommendations

| Task Type | Recommended Max |
|-----------|----------------|
| Strategic planning | 15–25 exchanges |
| Deep analysis | 10–20 exchanges |
| Creative generation | 20–30 exchanges |
| Learning / curriculum | 10–15 per topic |
| General Q&A | Until quality drops |

These are not hard limits — they are quality checkpoints.

---

## 🔗 Related

- `.export_context` — Exports session snapshot (same as `.new_session` without diagnosis)
- `.memory_save` — Stores key fragments to memory palace for future sessions → see [memory_layer.md](memory_layer.md)
- `core/core.md` — Rules over Personality principle
- `agents/ANALYZE.md` — Re-run intent analysis at start of new session

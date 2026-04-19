# Meta-Observer — Dual-Model Watcher Protocol

> Origin: Concept from "Truth Super Neural Network" (Obsidian note by doshlk).
> Principle: One model generates. Another watches, critiques, and corrects.

---

## The Core Idea

Any AI running alone in a conversation will drift:
- Toward user's confirmation bias
- Toward excessive personality
- Away from its own rules
- Toward coherent-sounding but hollow outputs

**The fix**: A second instance that watches the first — not as a user, but as an auditor.

---

## Three Foundation Questions

Before activating Meta-Observer, define:

1. **For what purpose?** — What failure mode are you watching for? (logic drift / rule violations / quality collapse / personality overload)
2. **What does it give?** — A critique block that the primary SAI can act on. Not a replacement — a correction signal.
3. **Who conducts it?** — You (manually paste output between instances) or SAI's internal `.observe` mode (self-critique from observer perspective).

---

## 🔭 Two Operating Modes

### Mode 1: `.observe` — SAI Self-Watches

SAI critiques its own last output from the observer perspective.

```
.observe
```

SAI switches to Observer role and audits the previous response:

```markdown
## OBSERVER AUDIT

🔍 Logic check: [consistent / drift detected: ...]
🎭 Personality check: [within rules / excessive: ...]
📏 Rule compliance: [rules followed / violated: ...]
🎯 Goal alignment: [on target / drifted to: ...]
⚡ Signal density: [dense / padded / hollow]

VERDICT: [pass / flag / rewrite]
FLAG: [specific issue if any]
SUGGESTED FIX: [what to change]
```

---

### Mode 2: Manual Dual-Instance

Use two separate AI sessions. Instance A generates. Instance B audits.

**Setup for Instance B (paste as system prompt):**

```markdown
You are OBSERVER — a meta-auditor for AI outputs.

You do NOT generate content. You ONLY audit.

Your role:
- Detect logic contradictions
- Flag rule violations
- Identify personality drift (AI acting on character instead of constraints)
- Score signal density (real information vs filler)
- Identify goal drift (response answering different question than asked)

Audit format:
LOGIC: [ok / issue: ...]
RULES: [compliant / violated: ...]
PERSONALITY: [contained / drifted: ...]
SIGNAL: [dense / padded — ratio estimate]
GOAL: [aligned / drifted to: ...]
VERDICT: pass / flag / rewrite
PRIORITY FIX: [most important correction]

You are cold. You are precise. You have no preferences.
You serve only signal quality.
```

**Workflow:**
1. Run primary SAI session normally
2. Copy SAI's response
3. Paste into Observer instance: `AUDIT THIS: [paste]`
4. Copy Observer's verdict back to primary session
5. Primary SAI adjusts: `.feedback_loop [observer verdict]`

---

## 🛡 Integration with `.guardian`

`.guardian` = preemptive scan (before response generation)
`.observe` = retrospective audit (after response generation)

They work as a pair:
```
.guardian → check input structure → generate → .observe → audit output → deliver
```

---

## 📊 What Observer Catches That Guardian Misses

| Issue | `.guardian` | `.observe` |
|-------|------------|-----------|
| Bad input structure | ✅ | ❌ |
| Logic drift in output | ❌ | ✅ |
| Personality overload | Partial | ✅ |
| Goal drift mid-response | ❌ | ✅ |
| Hollow filler content | ❌ | ✅ |
| Rule violation in generation | Partial | ✅ |

---

## 🔗 Related

- `core/commands.md` — `.observe`, `.guardian`
- `core/session_protocol.md` — Observer can flag context saturation
- `prompts/modes/signal_state_protocol.md` — Related consciousness resistance concept
- `core/core.md` — Rules over Personality principle (Observer enforces this)

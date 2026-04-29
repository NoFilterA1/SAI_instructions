# 🧠 SAI — Self-Adaptive Intelligence

![Badge](https://img.shields.io/badge/SAI-Self%20Adaptive%20Intelligence-2f2f2f?style=for-the-badge&labelColor=111111)

> _"Not another AI framework. A living, thinking ecosystem that chooses the right method when it matters."_

🔧 **Latest**: 9 automatic analysis techniques, 10-phase pipeline, session hygiene, memory architecture  
📊 **67 files** | **~10K lines** | **2-layer system** | **Production-ready**

---

## 📌 Navigation

- 🔍 [Core Philosophy](./core/core.md) — Mission, principles, Zero Position
- 🧬 [9 Analysis Techniques](./core/techniques_integration.md) — Automatic + manual activation
- 🔗 [Architecture & Pipeline](./ARCHITECTURE.md) — System map, 10-phase flow
- 🧩 [Commands Reference](./core/commands.md) — 25+ commands with examples
- 🎓 [Practical Examples](./prompts/techniques_examples.md) — 7 real scenarios
- 👤 [User Layer (USER_PACK)](./user_pack/) — Your persistent personal system

---

## 🧬 What is SAI?

**SAI** = Self Adaptive Intelligence.

A **cognitive framework** that:
- Starts from zero-bias thinking
- Combines logic, intuition, and strategy
- **Automatically selects analysis methods** based on what you ask
- Evolves with every interaction

SAI doesn't imitate thought — it **restructures how thought flows**.

---

## 🔗 Multi-Agent Architecture

SAI operates through a **distributed 3-agent chain**:

```
User Input
    │
    ▼
┌──────────┐    ┌──────────┐    ┌──────────┐
│ ANALYZE  │───▶│ PROMPTOR │───▶│   SAI    │
│          │    │          │    │          │
│ Clarify  │    │ Structure│    │ Execute  │
│ Intent   │    │ Intent   │    │ + Evolve │
└──────────┘    └──────────┘    └──────────┘
                                      │
              (9 Techniques Activate Here)
              (CoR & CoP with Feedback)
```

**Philosophy**: Clarity → Structure → Execution  
**Power**: Three minds aligned. Works alone or chained.

---

## 💡 9 Analysis Techniques (Auto-Select + Manual)

When you ask SAI something, it **automatically detects** which method fits best. Or **invoke manually** for precision:

| Situation | Technique | Command |
|-----------|-----------|---------|
| **Brainstorming** | Living Thinking — evolutionary ideation | `.living [topic]` |
| **Root cause** | Recursive Dive — chained "why?" questions | `.recursive_dive [Q]` |
| **Decision with trade-offs** | Sparring — clash opposite viewpoints | `.sparring "[A]" "[B]"` |
| **Too much text** | Compression — dense meaning, 3-6 words | `.compress` |
| **Hidden systems** | Pattern Recognition — recurring structures | `.pattern_extract` |
| **Know me better** | Persona Adaptation — continuous learning | `.persona_adapt` |
| **Need the truth** | Escalation — adjustable bluntness (1-4) | `.escalate` |
| **Ambiguous phrase** | Semantic Fullness — all interpretations | `.semantic_full [phrase]` |
| **Complex system** | Full Integration — map + feedback loops | `.full_integration` |

→ **Full reference**: [core/techniques_integration.md](./core/techniques_integration.md)  
→ **Real examples**: [prompts/techniques_examples.md](./prompts/techniques_examples.md)

---

## 🔄 10-Phase Pipeline

Every request flows through **structured phases**:

```
1. MOUNT           → Load your profile & memory
2. CONTEXT         → Build effective prompt
3. INPUT ANALYSIS  → Deep understanding (intent, stakes)
4. STRATEGY        → Select technique, role, style
5. CoR & CoP       → Chain of Reason + Prompt (with 9 techniques)
6. RESPONSE        → Generate + quality checks
7. OUTPUT + META   → Response + self-reflection
8. SAVE_STATE      → Propose profile updates
9. LEARNING        → Adapt from feedback
10. NEXT SESSION   → Export or start fresh
```

**HYPER LOOP**: Parallel background thinking while you read.

→ **Visualization**: [SAI_PIPELINE_VISUALIZATION.html](./SAI_PIPELINE_VISUALIZATION.html)

---

## 🏗️ Two-Layer System

### System Layer (Stateless Core)
- 20 core files
- 25+ commands
- 7 cognitive roles
- Techniques & strategies
- Philosophy & rules

### User Layer (USER_PACK)
- Your profile
- Memory palace
- Task tracking
- Custom agents
- Grows with every session

**Without USER_PACK**: Every chat is a stranger.  
**With USER_PACK**: Continuation of a system that remembers.

→ **Start**: [user_pack/README.md](./user_pack/README.md)

---

## 📚 Repository Structure

```
SAI_clean/
├── core/                          # The cognitive engine
│   ├── core.md                   # Mission & principles
│   ├── techniques_integration.md  # ← 9 techniques + auto-activation
│   ├── commands.md               # 25+ commands
│   ├── corcop.md                 # Chain of Reason/Prompt
│   ├── session_protocol.md       # Context hygiene
│   ├── memory_layer.md           # Verbatim palace memory
│   └── [12 more core files]
│
├── agents/                        # 3-agent pipeline
│   ├── ANALYZE.md                # Intent clarification
│   └── PROMPTOR.md               # Intent formalization
│
├── modules/                       # 20 concept + function modules
│   └── INDEX.md                  # Discovery map
│
├── prompts/                       # Ready-to-use prompts
│   ├── techniques_examples.md     # 7 real scenarios
│   ├── meta_observer.md           # Self-critique protocol
│   └── modes/                    # Expressive modes
│
├── user_pack/                     # Your personal layer (templates)
│   ├── PROFILE.md               # Who you are
│   ├── MEMORY_LOG.md            # Dynamic memory
│   ├── AGENTS.md                # Custom agents
│   └── TASKS.md                 # Task tracking
│
├── SAI_PIPELINE_VISUALIZATION.html
└── ARCHITECTURE.md
```

---

## 🚀 Quick Start

### Simplest Way
```
[Just ask SAI what you need]
```
SAI explains itself through real tasks. Commands appear when needed.

### Core Mode
```
.sai
[your request here]
```
Full internal reasoning: logic, strategy, technique selection.

### Auto-Config
```
.asai
[your request here]
```
Self-detects intent, assigns roles, optimizes prompt.

### Manual Technique
```
.living "generate project ideas"
.recursive_dive "why do I procrastinate?"
.sparring "[Stay at job]" "[Change careers]"
```

---

## ✨ Key Features

✅ **Automatic technique selection** — right method for right problem  
✅ **Manual override** — explicit commands for precision  
✅ **10-phase pipeline** — structured reasoning flow  
✅ **Session hygiene** — detects & resets context degradation  
✅ **Memory palace** — verbatim, cross-session recall  
✅ **Rules over personality** — stable constraints, no drift  
✅ **3-agent chain** — ANALYZE → PROMPTOR → SAI  
✅ **Compressed mode** — dense output, result first, no filler  

---

## 🧠 Core Philosophy: Rules Over Personality

SAI encourages **behavioral rules** over personality traits:

> **Rule** (survives): "Never skip CoR on strategic requests."  
> **Personality** (drifts): "Be sarcastic and edgy."

Rules are stable. Personality pollutes context. Expressive modes (JAI, JLO, DAI) are **tools for tasks**, not identity.

→ **See**: [core/core.md](./core/core.md) — Principle #6

---

## 🔄 Improvements from External Sources

| Source | Integration | File |
|--------|-------------|------|
| **MemPalace** | Verbatim palace structure (wings/rooms/drawers) | `core/memory_layer.md` |
| **Obsidian** | Dual-model watcher / self-critique | `prompts/meta_observer.md` |
| **Reddit compression** | 3-6 words, result first, no filler | `core/style.md` |
| **User research** | Rules-first, session hygiene | `core/core.md` |

---

## 📦 Local Development Version

For personal use with your profile and experiments:
→ **Use**: `/home/user/Programs/SAI_clean/`

Includes: MY_CARD.md, USER_DATA/ (archived techniques, personal experiments)

→ **See**: `USER_DATA_GUIDE.md` in Programs version

---

## 👨‍💻 Credits

**Original system**: doshlk — [GitHub: NoFilterA1](https://github.com/NoFilterA1)  
**Latest enhancements**: 9 technique integration, session hygiene, memory architecture, pipeline visualization

**Tested with**: Claude 3.5 Sonnet, Claude Opus, Claude Haiku

---

## 📖 Read Next

1. Start with: [core/core.md](./core/core.md) — understand the mission
2. Explore: [core/techniques_integration.md](./core/techniques_integration.md) — see how techniques work
3. Practice: [prompts/techniques_examples.md](./prompts/techniques_examples.md) — real scenarios
4. Reference: [core/commands.md](./core/commands.md) — full command syntax

---

> _"SAI is not a system you use. It is an intelligent environment you enter."_

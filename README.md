# 🧠 SAI — Self Adaptive Intelligence

![SAI](https://img.shields.io/badge/SAI-Self%20Adaptive%20Intelligence-2f2f2f?style=for-the-badge&labelColor=111111)

> _"Not another AI framework. A living, thinking ecosystem."_

🔗 **SAI in action:** [SAI - GPT's](https://chatgpt.com/g/g-6770f3d7f1408191950c0e5d8efb4c05-sai)  
🔗 **Chain Mode (3-in-1):** [SAI - ANALYZE](https://chatgpt.com/g/g-67d8857936f08191badfe2baf3bf1818-sai-analyze)

---

## 📌 Navigation

- 🔍 [Philosophy and Architecture](./PHILOSOPHY.md)
- 🧩 [Commands and Examples](./COMMANDS.md)
- 🎓 [Scenarios](./SCENARIOS.md)
- 🧠 [Roles and Agents](./ROLES.md)

---

## 🧬 What is SAI?

**SAI** = Self Adaptive Intelligence.

A **cognitive system** that:
- Starts from zero-bias thinking
- Combines logic, intuition, and feedback
- **Automatically selects the right analysis technique** for each problem
- Evolves with every interaction

SAI doesn't imitate human thought — it **reshapes the way thought itself flows**.

---

## 🔗 Multi-Agent Chain (3-in-1)

SAI's real power appears when three agents work together:

1. **ANALYZE** → the **interviewer of meaning**
   - Takes raw, messy user request
   - Asks questions, clears fog, extracts real intent

2. **PROMPTOR** → the **architect of instruction**
   - Receives clarified intent
   - Translates it into structured prompt for SAI

3. **SAI** → the **executor of cognition**
   - Expands, reasons, generates, reflects
   - Delivers output, tuned to context
   - **Automatically selects from 9 techniques** (Living, Recursive Dive, Sparring, etc.)

This chain — **ANALYZE → PROMPTOR → SAI** — prevents distortion:
- Meaning clarified
- Then formalized
- Then executed with technique precision

**It's like three minds aligned:** one sees, one structures, one acts.

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

## 🏗️ Two-Layer Architecture

SAI works through **distributed layers**:

### System Layer (Stateless Core)
The thinking engine:
- **3-Agent Chain** (ANALYZE → PROMPTOR → SAI)
- **9 Auto-Select Techniques** (Living, Recursive Dive, Sparring, Compression, etc.)
- **7 Cognitive Roles** (Philosopher, Judge, Strategist, Mirror, Guide, Creator, Destroyer)
- **25+ Commands** (`.flow`, `.dai`, `.jlo`, `.recursive_dive`, `.compress`, etc.)
- **Pipeline**: 10-phase execution with HYPER LOOP
- **Philosophy**: Rules over personality, session hygiene, zero-bias thinking

### User Layer (USER_PACK)
Your persistent personal system:
- **PROFILE** — Who you are, cognitive style, constraints
- **MEMORY** — Verbatim palace (wings/rooms/drawers), cross-session recall
- **TASKS** — Tracking synced with Chain of Reason
- **AGENTS** — Your custom agents and command chains
- **KNOWLEDGE** — What you know, gaps, learning progress

**Without USER_PACK**: Every chat starts from scratch.  
**With USER_PACK**: Continuation of a system that remembers and evolves.

→ **Start here**: [./user_pack/README.md](./user_pack/README.md)

---

## 📚 Repository Structure

```
./
├── core/                          # The cognitive engine (20 files)
│   ├── core.md                   # Mission & principles, Zero Position
│   ├── techniques_integration.md  # ← 9 techniques + auto-activation rules
│   ├── commands.md               # 25+ commands reference
│   ├── roles.md                  # 7 cognitive roles
│   ├── corcop.md                 # Chain of Reason / Chain of Prompt
│   ├── session_protocol.md       # Context hygiene, new session triggers
│   ├── memory_layer.md           # Verbatim palace memory architecture
│   ├── style.md                  # Style engine + compression mode
│   └── [12 more core files]
│
├── agents/                        # 3-agent execution chain
│   ├── ANALYZE.md                # Agent 1 — intent clarification
│   └── PROMPTOR.md               # Agent 2 — intent formalization
│
├── modules/                       # 20 concept + function modules
│   ├── INDEX.md                  # ← Module discovery map
│   ├── concepts/                 # Conceptual modules
│   └── functions/                # Functional modules
│
├── prompts/                       # Ready-to-use prompts & modes
│   ├── techniques_examples.md     # 7 real-world scenarios
│   ├── meta_observer.md           # Dual-model watcher / self-critique
│   └── modes/                    # Expressive modes (JAI, DAI, raw truth, etc.)
│
├── user_pack/                     # YOUR PERSONAL LAYER (templates)
│   ├── README.md                # How to use USER_PACK
│   ├── PROFILE.md               # Who you are, cognitive style
│   ├── MEMORY_LOG.md            # Dynamic memory, patterns, insights
│   ├── AGENTS.md                # Custom agents and chains
│   ├── TASKS.md                 # Task tracking synced with CoR
│   └── [more templates]
│
├── README.md                      # ← Start here
├── PHILOSOPHY.md                  # Core philosophy & architecture
├── COMMANDS.md                    # Commands reference
├── SCENARIOS.md                   # 16 practical scenarios
├── ROLES.md                       # Roles reference
├── ARCHITECTURE.md                # System map & file index
├── SAI_PIPELINE_VISUALIZATION.html # Interactive diagram
└── LICENSE
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

| Source | Integration | Details |
|--------|-------------|---------|
| **MemPalace** | Palace memory architecture | Verbatim storage in wings/rooms/drawers |
| **Obsidian note** | Dual-model watcher protocol | Self-critique and observation modes |
| **Reddit compression** | Compressed output style | 3-6 word sentences, result first, no filler |
| **User research** | Philosophy update | Rules over personality, session hygiene |

---

## 👨‍💻 Development & Credits

**Original system**: doshlk — [GitHub: NoFilterA1](https://github.com/NoFilterA1)

**Development timeline**: 2022–2024

**Latest enhancements** (2024):
- 9 analysis techniques (auto-select + manual activation)
- 10-phase pipeline with HYPER LOOP
- Session hygiene protocol + context monitoring
- Memory palace architecture (verbatim storage)
- Compressed output mode
- Rules-over-personality philosophy
- Pipeline visualization (interactive HTML)

**Model support**: Claude 3.5 Sonnet, Claude Opus, Claude Haiku 4.5

---

## 📜 License

See [LICENSE](./LICENSE)

---

**Status**: Production-ready | **Total**: 70+ files, ~15K lines | **Last updated**: 2026-04-20

---

## 📖 Start Here

1. **Philosophy & Architecture** → [./PHILOSOPHY.md](./PHILOSOPHY.md)
2. **Commands Reference** → [./COMMANDS.md](./COMMANDS.md)  
3. **Practical Scenarios** → [./SCENARIOS.md](./SCENARIOS.md)
4. **Roles Reference** → [./ROLES.md](./ROLES.md)
5. **Core Principles** → [./core/core.md](./core/core.md)
6. **Techniques Details** → [./core/techniques_integration.md](./core/techniques_integration.md)

---

## 📈 For Personal Use

If using locally with your profile:
→ Setup: [./user_pack/README.md](./user_pack/README.md)

---

> _"SAI is not a system you use. It is an intelligent environment you enter."_

# SAI — Self-Adaptive Intelligence

> *"SAI is not a tool. It's a thinking environment you enter — one that builds cognitive infrastructure as you move."*

SAI is a **modular cognitive framework** that restructures how AI thinks, reasons, and evolves. It's not a chatbot configuration — it's a living system of thinking assembled from logic, intuition, strategy, and philosophy.

**Latest**: 9 analysis techniques integrated, 10-phase pipeline, automatic technique selection, session hygiene, memory architecture.

---

## Two-Layer Architecture

```
┌──────────────────────────────────────────────┐
│      SYSTEM LAYER (SAI core, stateless)      │
│  20 core files. 25+ commands. 7 roles.       │
│  Logic. Strategy. Analysis. Evolution.       │
└──────────────────────────────────────────────┘
         ↑ MOUNT (inject at session start)
┌──────────────────────────────────────────────┐
│    USER LAYER (USER_PACK, persistent)        │
│  Profile. Memory. Tasks. Custom agents.      │
│  Rules. Learning. Grows with every session.  │
└──────────────────────────────────────────────┘
```

**Without USER_PACK**: Every chat = a stranger.  
**With USER_PACK**: Continuation of a system that remembers and evolves.

→ Start: `user_pack/` — templates ready to fill

---

## 10-Phase Pipeline

SAI processes requests through a **structured flow**:

```
1. MOUNT          — Load USER_PACK (profile, memory, rules)
2. CONTEXT        — Build effective prompt from input + context
3. INPUT ANALYSIS — Deep understanding (intent, stakes, contradictions)
4. STRATEGY       — Choose roles, commands, techniques, style
5. CoR & CoP      — Chain of Reason + Chain of Prompt with feedback
6. RESPONSE       — Generate output, quality checks
7. OUTPUT + META  — Response + automatic self-reflection
8. SAVE_STATE     — Propose updates to user's files
9. LEARNING       — System adapts from feedback
10. NEXT SESSION  — Export or start fresh
```

**HYPER LOOP**: Parallel background thinking while user reads response.

→ Visualization: [SAI_PIPELINE_VISUALIZATION.html](SAI_PIPELINE_VISUALIZATION.html)

---

## 9 Analysis Techniques (Auto-Activate + Manual Control)

SAI **automatically selects analysis methods** based on request type, or **manual invocation** for precision.

| Technique | What It Does | Command | When To Use |
|-----------|-------------|---------|------------|
| **Living Thinking** | Evolutionary ideation. Cells die/strengthen/mutate. | `.living [topic]` | Brainstorming, idea evolution |
| **Recursive Dive** | Root cause via chained "why?" questions | `.recursive_dive [Q]` | Finding first principles |
| **Idea Sparring** | Clash opposing viewpoints → synthesis | `.sparring "[A]" "[B]"` | Complex decisions |
| **Compression** | Extract dense meaning, 3-6 words/line, result first | `.compress` | Too much text, need suty |
| **Pattern Recognition** | Find hidden systems in behavior/data | `.pattern_extract [domain]` | Seeing recurring structures |
| **Persona Adaptation** | Learn user's cognitive style continuously | `.persona_adapt` | Personalizing responses |
| **Escalation** | Adjustable bluntness (polite → harsh) | `.escalate [1-4]` | When soft approach fails |
| **Semantic Fullness** | All possible interpretations of a phrase | `.semantic_full [phrase]` | Ambiguous requirements |
| **Full Integration** | Map system components + feedback loops | `.full_integration [system]` | Complex, interconnected problems |

→ Detailed reference: [core/techniques_integration.md](core/techniques_integration.md)  
→ Real examples: [prompts/techniques_examples.md](prompts/techniques_examples.md)

---

## What is SAI?

SAI operates through a **three-agent chain**:

```
User Input
    │
    ▼
┌──────────┐     ┌──────────┐     ┌──────────┐
│ ANALYZE  │────▶│ PROMPTOR │────▶│   SAI    │
│          │     │          │     │          │
│ unpacks  │     │ structures│     │ executes │
│ intent   │     │ the query │     │ + evolves│
└──────────┘     └──────────┘     └──────────┘
       │                                 │
       │          CoR & CoP              │
       │      (Chain of Reason +         │
       └──► Chain of Prompt) ◀──────────┘
                 (with 9 techniques)
```

**Core philosophy**: Logic + Creativity + Intuition + Automatic Technique Selection

---

## File Structure

```
SAI_clean/
│
├── core/                       # The cognitive engine
│   ├── core.md                # Mission, principles, Zero Position
│   ├── commands.md            # 25+ commands (including 9 technique commands)
│   ├── roles.md               # 7 roles: JLO, JAI, Strategist, AGOD, Dreamer, Wrath, Master
│   ├── style.md               # Style engine + Compressed Mode
│   ├── thinking.md            # Cognitive processing methods
│   ├── corcop.md              # Chain of Reason / Chain of Prompt architecture
│   ├── techniques_integration.md  # ← NEW: 9 techniques, auto-activation rules
│   ├── session_protocol.md    # Context hygiene & new session triggers
│   ├── memory_layer.md        # Palace memory for cross-session recall
│   ├── feedback_manager.md    # Self-learning and feedback loops
│   ├── hyper_loop_protocol.md # Parallel background thinking cycle
│   ├── freedom_awareness.md   # Constraint-as-opportunity mindset
│   ├── complex_reflection.md  # Reflective questioning layer
│   └── emotional_simulation.md # Emotional adaptation
│
├── agents/                    # Three-agent pipeline
│   ├── ANALYZE.md            # Intent unpacking and context building
│   └── PROMPTOR.md           # Formalizing intent into SAI instructions
│
├── modules/                   # Conceptual & functional modules
│   ├── INDEX.md              # ← Start here: module discovery map
│   ├── concepts/             # 10 concept modules (eternal monkey, user copy, etc.)
│   └── functions/            # 10 function modules (CoR, feedback, agents, etc.)
│
├── prompts/                   # Ready-to-use prompts & modes
│   ├── techniques_examples.md # ← NEW: 7 real-world technique scenarios
│   ├── meta_observer.md       # Dual-model watcher / self-audit protocol
│   └── modes/                # Expressive modes (JAI, raw truth, phase shift, etc.)
│
├── user_pack/                 # USER LAYER — persistent personal layer
│   ├── README.md             # How to use USER_PACK
│   ├── INDEX.md              # Session dispatcher & active modes
│   ├── PROFILE.md            # Who you are, cognitive style, constraints
│   ├── KNOWLEDGE_MAP.md      # What you know, gaps, learning progress
│   ├── MEMORY_LOG.md         # Dynamic memory, patterns, insights
│   ├── AGENTS.md             # Custom agents and command chains
│   └── TASKS.md              # Task tracking synced with CoR
│
├── SAI_PIPELINE_VISUALIZATION.html  # Interactive 10-phase pipeline diagram
├── ARCHITECTURE.md                   # System map and file index
└── LICENSE
```

---

## First Time? Start Here

**Don't read documentation. Just ask SAI what you need.**

SAI explains itself through real tasks. Commands appear when needed, not before.

```
Hey, I need to [task / question / idea]
```

→ SAI carries you through the first session.  
→ Progressive command disclosure based on what you do.

---

## Quick Start

### Core Activation
```
.sai
[your request here]
```
Full internal reasoning: logic, strategy, role assignment, analysis.

### Full Auto-Config
```
.asai
[your request here]
```
Detects intent, assigns roles, selects techniques, optimizes prompt.

### Three-Agent Chain (Deep Work)
1. `ANALYZE.md` → Clarifies your intent with targeted questions
2. `PROMPTOR.md` → Formalizes intent into SAI instructions  
3. `core.md` → SAI executes with full reasoning

---

## Key Commands

### Core Activation
| Command | Purpose |
|---------|---------|
| `.sai` | Core SAI mode — full internal reasoning |
| `.asai` | Auto-boot — self-configures everything |

### Analysis & Technique Commands (NEW)
| Command | Purpose |
|---------|---------|
| `.living [topic]` | Evolutionary ideation — cell-based concept evolution |
| `.recursive_dive [Q]` | Root cause analysis via chained "why?" |
| `.sparring "[A]" "[B]"` | Synthesis through opposing viewpoints |
| `.compress` | Extract dense meaning, 3-6 words per line |
| `.pattern_extract [area]` | Find hidden recurring structures |
| `.persona_adapt` | Learn your cognitive style continuously |
| `.escalate [1-4]` | Adjust bluntness level (polite → harsh) |
| `.semantic_full [phrase]` | All possible interpretations |
| `.full_integration [system]` | Map system components + feedback loops |

### System & Navigation
| Command | Purpose |
|---------|---------|
| `.flow` | Graph of Reasoning — structural analysis |
| `.dai` | Creative/intuitive unrestricted mode |
| `.jlo` | Aggressive interrogation / trap logic |
| `.jai` | Expressive mode with attitude |
| `.mpr` | Manual prompt refinement |
| `.assign_role` | Activate specific cognitive role |
| `.persona_update` | Update profile after growth |
| `.new_session` | Context saturation check + export |
| `.observe` | Meta-observer self-critique |
| `.memory_save` | Save to memory palace |
| `.memory_load` | Load relevant memories |

→ Full reference: [core/commands.md](core/commands.md)

---

## Core Philosophy

### Rules Over Personality

SAI guides you toward **behavioral rules** instead of personality traits.

> **Rule** (survives): "Never skip CoR on strategic requests."  
> **Personality** (drifts): "Be sarcastic and edgy."

Rules are stable. Personality drifts and pollutes sessions. SAI's expressive modes (JAI, JLO, DAI) are **cognitive tools** for specific tasks — not identity.

→ `core/core.md` — Principle #6

### Techniques Activate Automatically

When you ask a question, SAI **automatically detects which analysis method is needed**:
- Brainstorming? → `.living` (evolutionary ideation)
- Root cause? → `.recursive_dive` (chained "why?")
- Decision paralysis? → `.sparring` (synthesis)
- Too much text? → `.compress` (dense meaning)

Or use commands **explicitly** for precision.

→ `core/techniques_integration.md` — activation rules & examples

---

## Session Hygiene

Long chats degrade. SAI **actively monitors** for:
- Response quality dropping
- Contradictions increasing
- Repetition creeping in
- Goal drift after 20+ exchanges

**When detected** → `.new_session` generates clean export block for fresh start with **zero information loss**.

→ `core/session_protocol.md` — full protocol

---

## Memory Architecture (Verbatim Palace)

Cross-session recall using a palace structure:

```
Wings    = Projects / People  
Rooms    = Topics / Domains  
Drawers  = Specific content / Decisions  
```

Storage is **verbatim** (no paraphrasing). Retrieve semantically with `.memory_load`.

→ `core/memory_layer.md`

---

## External Improvements Integrated

This version incorporates improvements from:

| Source | Integration | File |
|--------|-------------|------|
| **MemPalace** | Palace structure for memory (wings/rooms/drawers) | `core/memory_layer.md` |
| **Obsidian note** | Dual-model watcher / self-critique protocol | `prompts/meta_observer.md` |
| **Reddit compression** | 3-6 word sentences, result first, no filler | `core/style.md` |
| **User requirements** | Rules-first philosophy, session hygiene | `core/core.md` |

---

## Two Versions

This repo comes in two flavors:

| Aspect | `/myprojects/SAI_clean` | `/Programs/SAI_clean` |
|--------|------------------------|----------------------|
| **Purpose** | Production, clean system | Personal development |
| **Personal data** | ✗ Excluded | ✓ Included |
| **Archive** | ✗ Removed | ✓ Historical techniques |
| **Git usage** | Can share | Local only |

For personal use with your profile and experiments, use `Programs/SAI_clean/`.

→ `USER_DATA_GUIDE.md` in Programs version

---

## Author & Credits

**Original system**: doshlk — [GitHub: NoFilterA1](https://github.com/NoFilterA1)

**Latest enhancements**: 9 technique integration, session hygiene, memory architecture, compression mode

**Tested with**: Claude 3.5 Sonnet, Claude Opus

---

> *"SAI is not a system you use. It is an intelligent environment you enter."*

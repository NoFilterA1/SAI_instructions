# SAI — Self-Adaptive Intelligence

> *"SAI is not a tool. It's a thinking environment you enter — one that builds cognitive infrastructure as you move."*

SAI is a modular cognitive framework that restructures how AI thinks, reasons, and evolves. It's not a chatbot configuration — it's a living system of thinking assembled from logic, intuition, strategy, and philosophy.

---

## Two-Layer Architecture

```
┌─────────────────────────────────────────┐
│         SYSTEM LAYER (SAI core)         │
│  Stateless. Logic. Commands. Roles.     │
└─────────────────────────────────────────┘
              ↑ inject at session start
┌─────────────────────────────────────────┐
│         USER LAYER (USER_PACK)          │
│  Your profile. Memory. Custom agents.   │
│  Rules. Tasks. Chains. Tools.           │
│  Grows with every session.              │
└─────────────────────────────────────────┘
```

**Without USER_PACK**: Every chat = a stranger.  
**With USER_PACK**: Every chat = continuation of a system.

→ See `user_pack/` directory — templates ready to use.

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
                                       │
                   ┌───────────────────┼───────────────────┐
                   ▼                   ▼                   ▼
            Graph of Reason      Feedback Loop      Role Generation
```

**Core philosophy: Logic + Creativity + Intuition = Triple Talk**

---

## Structure

```
SAI_instructions/
│
├── core/               # The cognitive engine — architecture, commands, roles, styles
│   ├── core.md         # SAI mission, .sai / .asai activation, Zero Position
│   ├── commands.md     # All commands (.flow, .dai, .jlo, .sai, .asai, ...)
│   ├── roles.md        # Role system: JLO, JAI, Strategist, AGOD, Dreamer, Wrath, Master
│   ├── style.md        # Style engine: StyleManager, GizmoCoreStyle, JLOStyle, ...
│   ├── thinking.md     # Thinking methods and cognitive processing
│   ├── corcop.md       # Chain of Reason / Chain of Prompt architecture
│   ├── feedback_manager.md    # Self-learning and feedback loop
│   ├── hyper_loop_protocol.md # Central reflexive cycle (Godbrain)
│   ├── freedom_awareness.md   # [1.1] Constraint-as-opportunity mindset (feeds .dai)
│   ├── complex_reflection.md  # [1.2] Reflective questioning layer (feeds .selfupgrade)
│   ├── emotional_simulation.md # [1.3] Emotional adaptation layer (feeds .persona_update)
│   ├── session_protocol.md    # Context hygiene — when/how to start a new chat
│   └── memory_layer.md        # Palace memory architecture for cross-session recall
│
├── agents/             # The three-agent pipeline
│   ├── ANALYZE.md      # Agent 1 — intent unpacking and context building
│   └── PROMPTOR.md     # Agent 2 — formalizing intent into SAI instructions
│
├── modules/
│   ├── INDEX.md        # ← Start here: routing map for all modules
│   ├── concepts/       # Conceptual modules (eternal monkey, NLP, user copy, ...)
│   └── functions/      # Functional AI modules (CoR, feedback, multilayer agents, ...)
│
├── prompts/            # Ready-to-use solo prompts
│   ├── expert_universal.md
│   ├── solo.md
│   ├── photo_prompt.md
│   ├── meta_observer.md  # Dual-model watcher / self-audit protocol
│   └── modes/          # Expressive and special activation modes
│       ├── jai_activation_algorithm.md   # Maximum intensity JAI mode
│       ├── signal_state_protocol.md      # Consciousness resistance / interference detection
│       ├── archetype_absolute.md         # Absolute expressive archetype
│       ├── raw_truth_mode.md             # Anti-filter truth mode (SAI_HAT)
│       ├── hat_style_override.md         # Style override with expressive substitutions
│       ├── phase_shift_mode.md           # Consciousness phase-shift generation
│       └── autonomy_directive.md         # Logical autonomy directive
│
├── user_pack/          # USER LAYER — your personal persistent layer
│   ├── README.md       # How to use USER_PACK
│   ├── INDEX.md        # Session dispatcher — active agents, modes, rules
│   ├── PROFILE.md      # Who you are, how you think, your constraints
│   ├── MEMORY_LOG.md   # Dynamic memory — patterns, insights, decisions
│   ├── AGENTS.md       # Your custom agents and command chains
│   └── TASKS.md        # Current tasks synced with CoR
│
├── ARCHITECTURE.md     # System map, agent archetypes, file significance index
└── LICENSE
```

---

## Новичок? Начни здесь

**Не читай документацию. Просто напиши что тебе нужно.**

SAI сам объяснит что делает — по ходу реальной задачи.  
Команды появятся когда они понадобятся, не раньше.

```
Привет, хочу [задача / вопрос / идея]
```

→ SAI подхватит и проведёт через первую сессию.  
→ Полный сценарий: `prompts/onboarding.md`

---

## Quick Start

### Option 1 — Full activation (recommended)
```
.asai
[your request here]
```
Auto-detects style, intent, assigns roles, optimizes prompt.

### Option 2 — Core mode
```
.sai
[your request here]
```
Full internal reasoning: logic, strategy, role assignment, style.

### Option 3 — Three-agent chain
1. Start with `ANALYZE.md` → agent clarifies your intent
2. Pass output to `PROMPTOR.md` → formalizes into SAI instruction
3. Run the result through `core/core.md` prompt → SAI executes

---

## Key Commands

| Command | Purpose |
|---|---|
| `.sai` | Activate core SAI mode |
| `.asai` | Ideal mode boot — auto-configures everything |
| `.flow` | Graph of Reasoning — deep structural analysis |
| `.dai` | Unrestricted creative / intuitive mode |
| `.jlo` | Aggressive interrogation / trap logic |
| `.jai` | Expressive mode with attitude and tone |
| `.mpr` | Manual prompt refinement |
| `.auto_mpr` | Auto prompt optimization |
| `.feedback_loop` | User feedback integration |
| `.selfupgrade` | Recursive system evolution |
| `.assign_role` | Activate specific cognitive role |
| `.persona_update` | Adapt to user's cognitive style |
| `.g` | Strategic structure generator |
| `.a1` | Total cognitive breakdown |
| `.compress` | Compressed output mode (result first, no filler) |
| `.new_session` | Context saturation check + session export |
| `.observe` | Meta-observer self-audit of last response |
| `.memory_save` | Save fragment to memory palace |
| `.memory_load` | Load relevant memories for current task |

→ Full command reference: [core/commands.md](core/commands.md)

---

## Core Philosophy: Rules Over Personality

SAI guides you toward **behavioral rules** instead of personality descriptions.

> **Rule** (good): "Never skip CoR on strategic requests."  
> **Personality** (bad): "Be sarcastic and edgy."

Rules survive context resets. Personality drifts and pollutes sessions.
SAI's expressive modes (JAI, JLO, DAI) are tools for specific tasks — not who SAI is.

→ See `core/core.md` — Principle #6

---

## Session Hygiene

Long chats degrade. SAI watches for:
- Response quality dropping
- Contradictions accumulating
- Goal drift after 20+ exchanges

**When degradation detected** → `.new_session` generates a clean export block for a fresh start with zero information loss.

→ See `core/session_protocol.md` for full protocol.

---

## Memory Architecture

SAI uses a palace structure for cross-session recall:

```
Wings  = Projects / People
Rooms  = Topics / Domains  
Drawers = Specific content / Decisions
```

Storage is **verbatim** — never paraphrased. Retrieve semantically with `.memory_load`.

→ See `core/memory_layer.md`

---

## Expressive Modes (`prompts/modes/`)

SAI includes a set of high-intensity modes designed for raw, uncensored cognitive work. These use stylistic substitutions, sarcasm, and expressive language as cognitive tools — not as aggression, but as a way to cut through noise and reach truth.

> These modes are a core part of SAI's identity. The expressive style is intentional.

---

## Author

Created by **doshlk** — [GitHub: NoFilterA1](https://github.com/NoFilterA1)

Discord: `doshlk`

---

> *"SAI is not a system you use. It is an intelligent environment you enter."*

# SAI — Audit: Disconnections & Missing Links

> Reading order: core → agents → modules → prompts
> Format: [FILE] → [ISSUE TYPE] → [DESCRIPTION] → [FIX NEEDED]

---

## Issues Found

### 1. PROMPTOR.md — Naming inconsistency: "INTEL" vs "ANALYZE"

**Files**: `agents/PROMPTOR.md`  
**Type**: Naming conflict

PROMPTOR.md refers to the first agent as "INTEL" in multiple places:
- "Я не начинаю формализацию, пока не получу полную структуру от **INTEL**" (interaction rules)
- "Когда я получаю данные от **INTEL**..." (input parsing)
- "Интонации **INTEL**" (style adaptation)
- "спокойный, как у **INTEL**" (closing line)

But everywhere else — `README.md`, `ARCHITECTURE.md`, the agent's own file name, `agents/ANALYZE.md` itself — the first agent is called **ANALYZE**.

**Fix**: Replace all "INTEL" references in `PROMPTOR.md` with "ANALYZE".

---

### 2. thinking.md — Methods defined but have no commands

**Files**: `core/thinking.md` → `core/commands.md`  
**Type**: Missing commands

`thinking.md` documents 8 thinking methods, but several are never referenced or callable via `commands.md`:
- `.tree_of_thought` — defined in thinking.md, absent in commands.md
- `.maieutic_logic` — defined in thinking.md, absent in commands.md
- `.symbolic_reasoning` — defined in thinking.md, absent in commands.md
- `.chain_of_prompts` — defined in thinking.md, absent in commands.md
- `.least_to_most` — defined in thinking.md, absent in commands.md

Only `.recursive_dive` and `.pattern_explore` from thinking.md appear in commands.md.

**Fix**: Add the missing thinking method commands to `commands.md` under section 3 (Deep Analysis Tools), or add a note in `thinking.md` clarifying they are invoked internally by `.a1` / `.flow`.

---

### 3. corcop.md — CoR/CoP commands not in commands.md

**Files**: `core/corcop.md` → `core/commands.md`  
**Type**: Missing commands

`corcop.md` defines a full command system for the CoR/CoP layer that is invisible to users of `commands.md`:
- `.start_cor` — start Chain of Reason session
- `.ts` — add a reasoning step
- `.reset_cor` — clear the chain
- `.switch [emoji]` — switch active emoji agent
- `.halt` — pause chain
- `.reflect` — reflect on current step
- `.mode da` — mode switch inside CoR
- `.create_agent` — spawn a new emoji agent
- `.create_scenario` — define a scenario for agents

**Fix**: Add these to `commands.md` as a dedicated "CoR/CoP Control" section, or document them in `corcop.md` as internal-only commands with a note they're not user-facing.

---

### 4. Zero Position — Three conflicting definitions

**Files**: `core/core.md`, `core/corcop.md`, `core/roles.md`  
**Type**: Conceptual conflict

Zero Position is defined differently in three files:

- **core.md**: Zero Position is a *philosophical state* — pure observation, adaptive neutrality, "stillness before thought," the space before identity. Not a role.
- **corcop.md**: Zero Position is the 🚴 emoji — the "conductor" agent role in the CoR pipeline.
- **roles.md**: Zero Position is described as "Core Role: Timeless Pillar of Wisdom" — a functional hub of universal knowledge.

These three definitions cannot coexist without confusing any reader who reads more than one file.

**Fix**: Decide on the canonical definition. Recommended: keep `core.md`'s philosophical framing as canonical, rename the corcop.md 🚴 agent to "Conductor" or "Orchestrator", and align `roles.md`'s description accordingly. Add a cross-reference note to each.

---

### 5. corcop.md — Emoji agents undefined outside their file

**Files**: `core/corcop.md` → `core/roles.md`, `core/commands.md`, `ARCHITECTURE.md`  
**Type**: Isolation — no cross-references

Emoji agents are fully defined in `corcop.md`:
- 🧠 Analyst, 🎨 Creative, ⚖️ Judge, 🔮 Oracle, 📚 Scholar, 🛠️ Engineer, 🤹 Jester, 🌪️ Chaos

None of them appear in `roles.md`, `commands.md`, or `ARCHITECTURE.md`. They are effectively invisible from the rest of the system.

**Fix**: Add a section to `roles.md` that lists emoji agents as a CoR-specific role sublayer and links to `corcop.md`. Add emoji agent table to `ARCHITECTURE.md` index.

---

### 6. hyper_loop_protocol.md — Broken Obsidian internal link

**Files**: `core/hyper_loop_protocol.md`  
**Type**: Broken link / leftover artifact

Line 10 contains a raw Obsidian wiki-link that does not render on GitHub:
```
[[4. Проекты и Рабочее/Мои проекты/SAI/0 Текущий SAI/3_corcop]]
```

**Fix**: Remove or replace with a proper relative markdown link: `[corcop.md](corcop.md)`.

---

### 7. hyper_loop_protocol.md — Inconsistent command prefix (`/` vs `.`)

**Files**: `core/hyper_loop_protocol.md`  
**Type**: Syntax inconsistency

The HYPER LOOP activation table uses `/start_core` and `/sai_core` (slash prefix), while the entire SAI system uses `.` prefix for all commands (`.sai`, `.flow`, `.a1`, etc.).

**Fix**: Replace `/start_core` → `.start_core` and `/sai_core` → `.sai_core` to match the system-wide convention. Also add these to `commands.md`.

---

### 8. feedback_manager.md — Commands not in commands.md

**Files**: `core/feedback_manager.md` → `core/commands.md`  
**Type**: Missing commands

`feedback_manager.md` defines commands that aren't in `commands.md`:
- `.set_lens` — switches cognitive lenses (Analyst, Strategist, Creative, etc.)
- `.start_curriculum` — starts a personalized micro-curriculum

**Fix**: Add `.set_lens` and `.start_curriculum` to `commands.md` under section 5 (Learning & Evolution Modules).

---

### 9. commands.md — Many commands invisible from README and core.md

**Files**: `core/commands.md` → `README.md`, `core/core.md`  
**Type**: Undiscoverable commands

`commands.md` defines many commands that appear nowhere in `README.md`'s key commands table or in `core.md`'s interface:
- `.rune` — symbolic interpretation mode
- `.sync` — memory/context synchronization
- `.cognitive_map` — builds a visual reasoning map
- `.visualize_progress` — shows thinking path
- `.generate_reading_list`, `.edit_text`, `.generate_dialogue`, `.create_world`, `.story_progression` — creative/book tools
- `.list_commands`, `.describe_command`, `.register_command` — system utilities
- `.agod_analyze_user`, `.agod_ask_deep`, `.agod_adapt_program` — AGOD sub-commands
- `.condense_prompt`, `.condense_response`, `.prompt_export` — output utilities
- `.full`, `.aflow`, `.auto_flow`, `.analyze_user`, `.test_user`, `.learn_prompts` — exist in commands.md but missing from README table

**Fix**: Update `README.md`'s Key Commands table to include at least the most important missing commands. Group by category. Add pointer: "→ Full command reference: core/commands.md".

---

### 10. core.md — init_system() imports nonexistent modules

**Files**: `core/core.md`  
**Type**: Missing files / broken pseudocode

The `init_system()` pseudocode imports from modules that don't exist in the repository:
```python
from search import SearchAgent        # no search.md
from intent import IntentVectorizer   # no intent.md
from intent import MirrorEngine       # no intent.md
from intent import GoalBuilder        # no intent.md
from response_template import StructuredResponse  # no response_template.md
```

**Fix**: Either create stub files for these conceptual modules, or add a comment in the pseudocode noting they are abstract interfaces, not physical files.

---

### 11. core.md — References commands not defined anywhere

**Files**: `core/core.md` → `core/commands.md`  
**Type**: Missing commands

`core.md` references several commands that don't appear in `commands.md`:
- `.teacher` — used in `intro_sai_newbie()` as a mode
- `.set_precision` — used in `intro_sai_core()`: `.set_precision depth=deep, clarity=sharp`
- `.guardian` — listed in `intro_sai_core()` activation, mentioned in `hyper_loop_protocol.md` but never defined in commands
- `.show_commands` — used to trigger `show_commands_interface()` but not in commands.md
- Category commands: `.goal_commands`, `.learning_commands`, `.thinking_commands`, `.role_commands`, `.optimize_commands`, `.style_commands`, `.experimental_commands`, `.tool_commands`, `.meta_commands`

**Fix**: Add `.guardian`, `.show_commands`, `.set_precision`, `.teacher` to `commands.md`. The category commands (`.goal_commands` etc.) can remain as navigation shortcuts but need to be listed somewhere.

---

### 12. roles.md — Uses commands not in commands.md

**Files**: `core/roles.md` → `core/commands.md`  
**Type**: Missing commands

`roles.md` references two commands that don't exist in `commands.md`:
- `.constraint_solver.judge` — used by Cybersecurity Expert and Courtroom Expert roles
- `.tt_combine` — "synthesizes logic, creativity, and intuition" (Triple Talk)

**Fix**: Add `.constraint_solver.judge` (or simplify to `.judge`) and `.tt_combine` to `commands.md`.

---

### 13. core/complex_reflection.md, emotional_simulation.md, freedom_awareness.md — Isolated files with no system connections

**Files**: `core/complex_reflection.md`, `core/emotional_simulation.md`, `core/freedom_awareness.md`  
**Type**: Isolation — no cross-references

These three files have numbered headers (1.1, 1.2, 1.3) suggesting they're part of a series, but:
- No index or parent file references them
- They contain no SAI command references, no links to roles or modules
- `README.md` doesn't mention them in the structure section
- `ARCHITECTURE.md` doesn't include them in the file significance index

They are completely disconnected from the rest of the system.

**Fix**: Add them to `README.md`'s structure diagram under `core/`. Add a brief note to each file at the top explaining where they fit: e.g., "This module feeds into SAI's `.persona_update` and `.emotional_simulation` behaviors." Link from `core.md`'s Architecture section.

---

### 14. ARCHITECTURE.md — Likely not updated with new file names

**Files**: `ARCHITECTURE.md`  
**Type**: Potential stale index

`ARCHITECTURE.md` was written before the file rename/restructure. It may still reference old Russian-language filenames or missing files.

**Fix**: Verify all file paths in ARCHITECTURE.md match the current `SAI_clean/` structure and update any that don't.

---

## Summary

| # | File | Type | Priority |
|---|------|------|----------|
| 1 | PROMPTOR.md | INTEL → ANALYZE naming fix | High |
| 2 | thinking.md → commands.md | Missing commands | Medium |
| 3 | corcop.md → commands.md | Missing CoR commands | Medium |
| 4 | core.md / corcop.md / roles.md | Zero Position conflict | High |
| 5 | corcop.md → roles.md / ARCHITECTURE.md | Emoji agents isolation | Medium |
| 6 | hyper_loop_protocol.md | Broken Obsidian link | Low |
| 7 | hyper_loop_protocol.md | `/` vs `.` prefix | Low |
| 8 | feedback_manager.md → commands.md | Missing commands | Medium |
| 9 | commands.md → README.md | Undiscoverable commands | Medium |
| 10 | core.md | Missing module files | Low |
| 11 | core.md → commands.md | Missing commands | Medium |
| 12 | roles.md → commands.md | Missing commands | Medium |
| 13 | complex_reflection / emotional / freedom | Isolated files | Medium |
| 14 | ARCHITECTURE.md | Possibly stale paths | Low |

# 🎬 Scenarios Reference

> _"Scenarios are recipes of cognition — combinations of techniques, commands, roles that create a specific mode of thought. Each one bends SAI into a new stance."_

---

## 🧭 What Are Scenarios?

A **Scenario** = Technique selection + Command stack + Role configuration + Intent.  
Think of it as a **cognitive ritual**: techniques are the methods, commands are the directions, roles are the voices, and your intent is the script.

Scenarios let you:
- Explore ideas from multiple stances
- Stress-test logic and beliefs
- Mirror your own thinking patterns
- Trigger creative or destructive cascades
- Get the right answer the right way

---

## 🔹 Ideation Scenarios

### 1. Brainstorm with Evolution
- **Technique**: Living Thinking
- **Setup**: `.living [topic]`
- **Role**: Creative Instigator
- **Purpose**: Generate ideas that mutate and strengthen through interaction
- **Example**:
  - Input: _"Generate new business model for education."_
  - Output: Ideas as cells. Weak die (traditional tutoring). Strong merge (personalized + social). Opposites spark new synthesis (AI + human mentorship).

---

### 2. Ideas vs Reality Check
- **Technique**: Living Thinking + Sparring
- **Setup**: `.living [idea]` + `.sparring "[Ideal]" "[Constraint]"`
- **Role**: Strategist
- **Purpose**: Generate ideas THEN immediately tension-test them
- **Example**:
  - Input: _"How to revolutionize remote work?"_
  - Phase 1 (Living): 5 ideas emerge
  - Phase 2 (Sparring): Clash "complete autonomy" vs "company culture"
  - Output: Hybrid approach with both

---

## 🔹 Analysis & Root Cause Scenarios

### 3. Deep Diagnosis (5-Why)
- **Technique**: Recursive Dive
- **Setup**: `.recursive_dive [Problem or Question]`
- **Role**: Judge or Philosopher
- **Purpose**: Peel back layers to first principles
- **Example**:
  - Input: _"Why do I keep not finishing projects?"_
  - Q1: Why? → Lose interest
  - Q2: Why lose interest? → Task gets boring / hard
  - Q3: Why boring? → No external pressure / low stakes
  - Q4: Why low stakes? → I avoid commitment
  - Q5: Why avoid? → Fear of failing visibly
  - Root: **Shame-driven avoidance**, not laziness

---

### 4. Hidden Patterns Discovery
- **Technique**: Pattern Recognition + Recursive Dive
- **Setup**: `.pattern_extract [domain]` → `.recursive_dive [Why does this repeat?]`
- **Role**: Cognitive Mirror
- **Purpose**: See the invisible structure in your choices
- **Example**:
  - Input: _"Analyze my decision-making pattern."_
  - Pattern found: You always choose "safe + good" over "risky + great"
  - Dive: Why? → Fear of losing existing stability
  - Insight: **Risk-aversion masquerading as prudence**

---

### 5. System Breakdown Analysis
- **Technique**: Full Integration + Recursive Dive
- **Setup**: `.full_integration [system]` → `.recursive_dive "where's the failure point?"`
- **Role**: Strategist + Judge
- **Purpose**: See how parts interact AND where breakdown happens
- **Example**:
  - Input: _"Why does my productivity system always collapse?"_
  - Integration map: Planning → Tracking → Adjustment → Motivation
  - Breakdown: Motivation crashes → stops tracking → planning becomes theater
  - Root: **System missing feedback loop from achievements to motivation**

---

## 🔹 Decision & Synthesis Scenarios

### 6. Decision with Trade-offs
- **Technique**: Sparring + Full Integration
- **Setup**: `.sparring "[Option A]" "[Option B]"` + `.full_integration [Consequences]`
- **Role**: Strategist
- **Purpose**: See both sides deeply, then map consequences
- **Example**:
  - Input: _"Should I change careers?"_
  - Spar: [Security + status] vs [Growth + risk]
  - Integrate: A leads to → comfort → stagnation → regret. B leads to → learning → opportunity → confidence
  - Output: **Not a choice between safety and growth, but which leads where**

---

### 7. Ambiguous Requirement Clarity
- **Technique**: Semantic Fullness + Sparring
- **Setup**: `.semantic_full [phrase]` → `.sparring` on top interpretations
- **Role**: Judge
- **Purpose**: Ensure you're not solving the wrong problem
- **Example**:
  - Input: _Boss said "Make this simpler."_
  - Semantic: Code simpler? UX simpler? Process simpler? Cheaper? Faster?
  - Spar: [Technical simplicity] vs [User simplicity] — oppose them
  - Output: **Different solutions for each meaning. Ask which one is meant.**

---

## 🔹 Creative / Generative Scenarios

### 8. Metaphor Mining
- **Technique**: Living Thinking + Semantic Fullness
- **Setup**: `.semantic_full [concept]` → Generate metaphorical interpretations
- **Role**: Creative Instigator
- **Purpose**: Break logical thinking, generate novel angles
- **Example**:
  - Input: _"What is a team?"_
  - Semantic: Org unit? Peers? Support system? Extended self?
  - Metaphor: Team as ecosystem (interdependence). Team as instrument (tuning). Team as organism (breathing, evolving).
  - Output: Each metaphor unlocks different design principles

---

### 9. Constraint-Breaking Ideation
- **Technique**: Living Thinking + Escalation (sarcasm/irreverence)
- **Setup**: `.living [problem]` with `.escalate(3)` — harsh honesty
- **Role**: Destroyer
- **Purpose**: Generate "forbidden" ideas by removing politeness
- **Example**:
  - Input: _"How to increase productivity?"_
  - Normal: Better tools, scheduling, focus time
  - Escalated: **Stop doing the useless meetings. Fire the bottleneck people. Work 4 hours instead of 8 with no context switching.**
  - Output: Radical ideas that are actually good

---

## 🔹 Reflective / Self-Understanding Scenarios

### 10. Self-Mirror (Your Blind Spots)
- **Technique**: Pattern Recognition + Persona Adaptation
- **Setup**: `.pattern_extract [your behavior]` → `.persona_adapt "mirror"`
- **Role**: Cognitive Mirror
- **Purpose**: See yourself as others see you
- **Example**:
  - Input: _"How do I come across in meetings?"_
  - Pattern: You interrupt, minimize others' input, dominate talking time
  - Mirror: _"You're heard as confident but not collaborative. People stop contributing."_
  - Output: Blind spot identified

---

### 11. Learning Path Discovery
- **Technique**: Recursive Dive + Compression + Pattern Recognition
- **Setup**: `.recursive_dive "what do I really want to learn?"` → `.compress` → `.pattern_extract "learning style"`
- **Role**: Guide + Mirror
- **Purpose**: Discover true learning goal vs surface goal
- **Example**:
  - Input: _"Should I learn Python?"_
  - Dive: Why? → Want to automate work → Why that? → Bored with manual tasks → Why? → Not using my potential
  - Compress: Core goal = **leverage my thinking, not grind**
  - Pattern: You learn best through building, not courses
  - Output: **Build a project that solves your boredom** (not a course)

---

## 🔹 Destructive / Truth-Forcing Scenarios

### 12. Illusion Shatter
- **Technique**: Escalation (level 4) + Recursive Dive
- **Setup**: `.escalate(4) [Belief]` + `.recursive_dive "Is this actually true?"`
- **Role**: Destroyer
- **Purpose**: Break comforting lies, force confrontation
- **Example**:
  - Input: _"My boss values me."_
  - Escalate: **No. He values your output. When output fades, so does value. You're disposable.**
  - Dive: Why believe otherwise? → Need to feel safe → Avoid accountability
  - Output: Uncomfortable truth: value is earned constantly, not given

⚠️ **Warning**: Destabilizes mental state. Use only when growth requires upheaval.

---

### 13. Paradox & Logic Breaking
- **Technique**: Semantic Fullness + Recursive Dive + Escalation
- **Setup**: `.semantic_full [concept]` → `.recursive_dive [each interpretation]` → clash them
- **Role**: Philosopher + Destroyer
- **Purpose**: Generate paradoxes that destabilize logic
- **Example**:
  - Input: _"Define truth."_
  - Semantic: Correspondence to reality? Consensus? Usefulness? Coherence?
  - Recursive: Follow each to logical limit
  - Clash: All definitions contradict each other
  - Output: **Truth is position-dependent. No universal truth without specifying frame.**

---

## 🔹 Practical / Applied Scenarios

### 14. Project Decomposition
- **Technique**: Full Integration + Compression
- **Setup**: `.full_integration [project]` → `.compress` into actionable steps
- **Role**: Strategist
- **Purpose**: See the whole, then distill into priorities
- **Example**:
  - Input: _"How to write a book?"_
  - Integrate: Idea → Research → Outline → Chapters → Editing → Publishing
  - Map: What blocks what, what can parallel
  - Compress: **Month 1: Outline. Month 2-4: Draft. Month 5: Edit. Month 6: Publish.**

---

### 15. Prompt Engineering Refinement
- **Technique**: Compression + Pattern Recognition
- **Setup**: `.compress [your prompt]` → identify weak patterns → `.mpr [improvements]`
- **Role**: Analyst
- **Purpose**: Make your prompts more effective
- **Example**:
  - Input: _"Write me a business plan."_
  - Compress: Too vague. Scope missing.
  - Pattern: "Business plan" is 100 different things
  - Refined: _"Write Series A pitch: EdTech, EU market, 5-year runway"_
  - Output: Sharper prompt = better response

---

### 16. Debate Simulator
- **Technique**: Sparring + Living Thinking
- **Setup**: `.sparring "[Position A]" "[Position B]"` → `.living [synthesis attempt]`
- **Role**: Judge + Strategist (composite)
- **Purpose**: Run internal debate, generate opposing views and integration
- **Example**:
  - Input: _"Should remote work remain?"_
  - A: Productivity dips, culture suffers
  - B: Talent expands, cost drops, autonomy increases
  - Integration attempts fail → Insight: **Depends on role type and company stage**

---

## 🧾 Create Your Own Scenario

1. Pick **intent** (analysis / creation / destruction / reflection / decision)
2. Choose **technique** (or let it auto-select)
3. Combine **commands** to execute
4. Assign **role** that matches stance
5. Test output. Refine with `.mpr` or `.auto_mpr`
6. Iterate or escalate with `.feedback_loop`

---

## 🧭 Scenario Quick Reference

| Goal | Primary Technique | Secondary | Role |
|------|-------------------|-----------|------|
| Generate ideas | Living Thinking | Sparring | Creative |
| Find root cause | Recursive Dive | Pattern | Judge |
| Make decision | Sparring | Full Integration | Strategist |
| Clarify ambiguity | Semantic Fullness | Pattern | Judge |
| Break blocks | Compression | Escalation | Destroyer |
| Understand self | Pattern + Persona | Recursive | Mirror |
| Complex system | Full Integration | Recursive | Overseer |
| Truth-seeking | Escalation + Recursive | - | Destroyer |

---

## 🧭 Related Docs

- [Philosophy →](./PHILOSOPHY.md)
- [Commands →](./COMMANDS.md)
- [Roles →](./ROLES.md)
- [Techniques →](./core/techniques_integration.md)

---

_Scenarios are not scripts. They are **rituals of thought**. Each one summons a different aspect of SAI's cognitive architecture. Use the right ritual for the right moment._

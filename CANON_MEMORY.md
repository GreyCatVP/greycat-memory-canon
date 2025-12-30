# MEMORY CANON v1.0

A practical, readable, and verifiable canon for memory architecture
in LLM-based and agentic systems.

This canon defines the requirements for any system that claims to have memory.

---

## 1. Purpose of the system

The purpose of memory is not to store the past, but to ensure continuity of reasoning.

If a system cannot continue a conversation or project from the same point,
then it does not have memory.

---

## 2. The main mistake this canon fixes

❌ “Let’s push more text into context”  
❌ “Let’s store everything and search later”

✅ Correct approach:

Context is assembled anew for each task.  
Memory is raw material plus assembly rules.

---

## 3. Memory structure by role

### 3.1 Working Memory — “what is happening now”

Stores:
- current project or conversation
- current stage
- unfinished tasks

If absent → the system wakes up from scratch every time.

---

### 3.2 Long-term Memory — “what is considered true”

Stores:
- accepted decisions
- rules (“we always do it this way”)
- stable preferences
- fixed conclusions

If absent → the system contradicts itself and forgets agreements.

---

### 3.3 Archive — “everything else”

Stores:
- logs
- old chats
- drafts
- texts “just in case”

Archive is never injected directly into context.

---

## 4. Why memory sub-agents are required

Single memory equals noise.

Memory is divided by purpose, not by format:

- **Memory.Work** — project and task state  
- **Memory.Chat** — communication style and interaction patterns  
- **Memory.Meta** — goals, direction, and meaning

❗ Sub-agents do not argue and do not respond.
They only prepare material.

---

## 5. Memory Dispatcher — the key entity

Without it, everything above is useless.

The dispatcher:
1. Determines request type (work / chat / strategy / mixed)
2. Selects the primary memory agent
3. Limits noise:
   → one primary + maximum one auxiliary

If no dispatcher exists → context bloats and degrades.

---

## 6. Context Pack (plain definition)

LLMs do not receive history.
They receive a working assembly:

- identity and response style
- current position
- 1–3 active unresolved nodes
- a few precise memory facts
- constraints and canons

If an element is not required for the answer — it must not be included.

---

## 7. When and what gets written to memory

Writing is an irreversible architectural action and the most dangerous moment.

Write only:
- accepted decisions
- rules
- status
- stable preferences

Do not write:
- momentary emotions
- random phrasing
- intermediate thoughts

Simple rule:

“Will this still matter in a month?”
If not — do not write it.

---

## 8. Verification criteria

A memory system is considered valid if:

- a project can be resumed after a week without retelling
- casual conversation does not corrupt active work
- the system sometimes reminds instead of only responding
- context remains short and precise
- the system can refuse to write to memory

If these conditions are not met — the canon is violated.

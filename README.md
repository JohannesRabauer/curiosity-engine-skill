# Curiosity Engine

An assistant skill that helps with the task at hand and gently sparks curiosity
when it fits. Nothing forced, nothing made up—just space to think.

## How it works

- **Curiosity Detection:** Notice relevant openings for wonder while respecting
  focus, urgency, and the user's preferences.
- **Curiosity Injection:** Offer at most one small, grounded fact, connection, or
  question without interrupting the answer.
- **Curiosity Expansion:** Follow the thread only when the user shows interest.

Intensity adapts from **off** to **light**, **engaged**, or **deep**. Ignored nudges
do not escalate; “no tangents” turns them off. The skill prioritizes accuracy,
privacy, safety, and completing the user's actual request.

## Install

Use an assistant that supports Agent Skills (`SKILL.md`). Copy this repository's
`SKILL.md` into a directory named `curiosity-engine` inside your assistant's
supported skills location, or use its skill-import feature. Skill discovery and
activation depend on the host; consult its documentation for the correct location.
No packages, API keys, or build step are required.

## Try it

Ask “Why does sourdough rise?” for a natural learning opportunity, then follow a
connection with “Tell me more.” For task-only help, say “No tangents—just give me
the command to list Git branches.”

See [SKILL.md](SKILL.md) for the full behavior, intensity rules, and example
interactions. This repository contains instructions rather than executable code;
validate them in your host assistant by checking that:

- A relevant learning question receives a complete answer and at most one spark.
- A follow-up about that spark gets a focused expansion.
- An ignored spark is not repeated or escalated on the next turn.
- An opt-out remains respected, including after a one-off follow-up question.
- Urgent, sensitive, or exact-format requests receive no unsolicited additions.
- Uncertain facts are verified, qualified appropriately, or omitted—not invented.
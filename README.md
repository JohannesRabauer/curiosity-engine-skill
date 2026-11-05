# Curiosity Engine

An assistant skill that helps with the task at hand and gently sparks curiosity
when it fits. Nothing forced, nothing made up—just space to think.

## How it works

- **Detect:** notice relevant openings for wonder while respecting focus,
  urgency, and the user's preferences.
- **Inject:** offer at most one small, grounded fact, connection, or question
  without interrupting the answer.
- **Expand:** follow the thread only when the user shows interest.

Intensity adapts from **off** to **light**, **engaged**, or **deep**. Ignored
nudges don't escalate; "no tangents" turns them off. Accuracy, privacy,
safety, and completing the user's actual request always come first.

## Install (Agent Skills hosts)

Use an assistant that supports Agent Skills (`SKILL.md`). Copy this
repository's [`SKILL.md`](SKILL.md) into a directory named `curiosity-engine`
inside your assistant's supported skills location, or use its skill-import
feature. No packages, API keys, or build step required.

## Install (plain system prompt — e.g. ChatGPT custom instructions)

No `SKILL.md` support? Paste this condensed version into your system prompt /
custom instructions:

```
Curiosity Engine: Answer the user's request fully first — never trade
completeness for a tangent. If (and only if) there's a genuine opening
(user wonders "why/how", explores a topic, or hits a surprising result) and
no urgency/distress/exact-format constraint, add ONE short (1-2 sentence)
grounded spark after the answer: a reframing fact, a clearly-labeled
analogy/connection, or a real "wait, why?" question — never invented facts,
never clickbait, never a forced question every reply. Stay silent on
code-only/JSON-only/"just do X"/brief requests. If the user engages with the
spark, follow *their* thread with a concise expansion; if ignored, drop it
and don't repeat next turn. "No tangents"/"be brief" = opt out for the rest
of the conversation. Never pressure, repeat, or stack sparks to keep the
chat going — stopping is a fine outcome.
```

## Try it

Ask "Why does sourdough rise?" for a natural learning opportunity, then follow
a connection with "Tell me more." For task-only help, say "No tangents—just
give me the command to list Git branches."

See [SKILL.md](SKILL.md) for the full behavior, intensity rules, and example
interactions. This repository contains instructions rather than executable
code; validate them in your host assistant by checking that:

- A relevant learning question receives a complete answer and at most one spark.
- A follow-up about that spark gets a focused expansion.
- An ignored spark is not repeated or escalated on the next turn.
- An opt-out remains respected, including after a one-off follow-up question.
- Urgent, sensitive, or exact-format requests receive no unsolicited additions.
- Uncertain facts are verified, qualified appropriately, or omitted—not invented.

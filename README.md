# 💡 Curiosity Engine

[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-ffcb47)](SKILL.md)
[![Website](https://img.shields.io/badge/docs-website-58a6ff)](https://johannesrabauer.github.io/curiosity-engine-skill/)
[![License](https://img.shields.io/badge/license-see%20repo-lightgrey)](#)

An assistant skill that helps with the task at hand and gently sparks curiosity
when it fits. Nothing forced, nothing made up—just space to think.

**🌐 [See the project website](https://johannesrabauer.github.io/curiosity-engine-skill/)**
for a quick visual tour, or keep reading for the full details and install
instructions below.

## Contents

- [How it works](#how-it-works)
- [Install (Agent Skills hosts)](#install-agent-skills-hosts)
- [Install (plain system prompt)](#install-plain-system-prompt--eg-chatgpt-custom-instructions)
- [Try it](#try-it)

## How it works

- **Detect:** notice relevant openings for wonder while respecting focus,
  urgency, and the user's preferences.
- **Simplify:** "ELI5" and similar phrases ("in simple terms", "dumb it
  down", "TL;DR") get a plain-language rewrite of the main answer, not an
  extra tangent.
- **Inject:** offer at most one small, grounded fact, connection, or question
  without interrupting the answer.
- **Expand:** follow the thread only when the user shows interest, with a
  small Mermaid or ASCII diagram if a visual genuinely helps.

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
completeness for a tangent. If the user says "ELI5" or asks for it "in
simple terms"/"dumbed down"/"plain English"/"TL;DR", rewrite the main answer
in short sentences, everyday words, and one concrete analogy — no jargon.
If (and only if) there's a genuine opening (user wonders "why/how", explores
a topic, or hits a surprising result) and no urgency/distress/exact-format
constraint, add ONE short (1-2 sentence)
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

---

🌐 **[Project website](https://johannesrabauer.github.io/curiosity-engine-skill/)**
· 📄 **[SKILL.md](SKILL.md)** · 👤 [@JohannesRabauer](https://github.com/JohannesRabauer)

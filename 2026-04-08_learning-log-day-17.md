# 2026-04-08 — Day 17: Rules Don't Run Backwards

> Danielle Vantini | Non-Technical AI Founder
> DanielleVantini.com | @danivwc

## What I Was Trying to Do

Fix a problem I had created myself. I added an archiving rule to all 19 of my agent config files two days earlier. I expected the bloated inboxes to shrink automatically. They did not. I wanted to know why.

## What Actually Happened

The INBOXes were still bloated — hundreds of lines of stale entries — even though the rule was in every CLAUDE.md file. I assumed the agents were ignoring the rule. They were not.

The agents were following the rule perfectly. The rule said "archive completed tasks." But the rule only applied to future behavior. The 200+ lines already in each file were past state. The rule did not reach backwards in time to clean them up.

I had to run a manual cleanup. Not because the system was broken. Because I had misunderstood what "adding a rule" means.

## What I Figured Out

**Rules govern future behavior. One-time migrations are separate work.** This is the most important distinction I have learned about AI agent systems and I did not read it anywhere. I felt it. Every student who builds a Claude Code system will hit this exact mistake, and most of them will blame the agents. The agents are fine. The rule is fine. What is missing is the migration step — the manual or scripted cleanup that moves the starting state to where the rule assumes you already are.

**Policy and enforcement are two different jobs.** Adding a rule to a config file is policy. Running the cleanup is enforcement. They feel like the same thing when you are writing the rule. They are not.

**Every new system-wide rule needs two parts: the rule itself, and the migration to comply with it.** If you only write the rule, you will be confused in 48 hours when nothing has changed. Write both. Ship both.

## What This Means for Non-Technical Founders

Before you add a rule to your AI system, ask yourself: do I also need to run a one-time migration to get to the starting state the rule assumes? If yes, build that migration the same day. If no, make sure you are sure. Most of the time, the answer is yes and you did not notice.

This is not a technical failure. It is a model-of-the-system failure. The fix is learning how AI agents actually follow rules — and when they do not, and why "do not" is almost always "cannot" instead.

## Next Step

Write this distinction into course material. It is the kind of lesson every student will hit and every coach will need to explain. Better to explain it once in a lesson than fifty times in coaching calls.

---

## More From Danielle Vantini
- [DanielleVantini.com](https://daniellevantini.com) — Personal brand hub
- [@danivwc on Instagram](https://instagram.com/danivwc)
- [AI Adoption History](../ai-adoption-history/) — Documented proof dating to 2021

---

**About the Author**
Danielle Vantini is one of the earliest non-technical business adopters of AI — with documented proof dating to 2021. She builds multi-agent systems in Claude Code without writing code. Follow the journey at DanielleVantini.com.

Tags: #ClaudeCode #AIAgents #NonTechnicalFounder #PromptEngineering #DanielleVantini

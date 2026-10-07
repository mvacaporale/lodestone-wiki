---
title: Turning AI Into a World-Class Designer (Anshu Chimala)
tags:
- ai-tooling
- design
- prompting
- product-development
- llms
summary: Lessons on getting distinctive, non-generic design out of AI by treating it as a guided process (Double Diamond) rather than a one-shot prompt.
---

# How to Turn Your AI Into a World-Class Designer

**Author:** Anshu Chimala · **Source:** Lenny's Newsletter (guest post), 2026-09-01
[Article link](https://www.lennysnewsletter.com/p/how-to-turn-your-ai-into-a-world)

## Core thesis

AI models are bad designers *by default* because they are next-token predictors trained to make safe, predictable choices — the result is "generic slop." Great design needs emotional resonance and rule-breaking, the opposite of what an LLM naturally reaches for. The gap between mediocre and exceptional AI design is **process and human guidance**, not the model.

## The framework — Double Diamond, adapted for AI

1. **Discover** — explore diverse directions with bold prompts.
2. **Define** — develop a distinct design identity through iteration.
3. **Deliver** — polish by removing what doesn't serve the user.

## Seven techniques

**Discover**
- **Seed strings** — inject a random alphanumeric string into prompts to force genuine variety across outputs (avoids samey results without looking random).
- **Ambitious prompts** — give a specific, wild creative brief ("pixel-art theme," "isometric 3D city") instead of a generic ask.

**Define**
- **Subagent feedback loops** — run a separate "design critic" model to judge aesthetics objectively, so the building agent doesn't get attached to mediocre work.
- **Image generation** — pull in real visual assets (OpenAI/Gemini APIs) to replace code-based fallbacks like CSS gradients.
- **Video generation for motion** — use video models to design sophisticated animations, glass effects, and fluid state transitions.

**Deliver**
- **Ruthless deletion** — strip decorative elements that don't serve users (gradients, glows, excess labels) to reach premium minimalism.
- **Remove "AI tells"** — identify and eliminate the patterns that signal AI authorship.

## Takeaway

Thoughtful prompt engineering, a critic-in-the-loop, and strategic use of specialized tools (image/video gen) unlock creative quality most users never reach. Direct the AI through a real design process; don't expect a good result from a single prompt.

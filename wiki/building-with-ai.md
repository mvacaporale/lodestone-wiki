---
title: Building with AI
---

> _This page is LLM-generated organization. The [notes](../notes/) it links
> to are the author's own writing._

# Building with AI

The practical counterweight to the theory clusters: notes from actually building things with AI tools. The recurring lesson is that good results come from **process and system design, not one-shot prompts** — whether that's running a design model through a real discovery-define-deliver loop, prompting Claude to explain its work like a staff engineer in a 1:1, or structuring a product effort around the riskiest assumption rather than the most complete build.

Two of these notes are infrastructure-flavored: a survey of backend services chosen specifically for how well AI coding agents can drive them, and the knowledge-management system design that feeds the vault this wiki is published from. [How This Wiki Was Built](../notes/how-this-wiki-was-built.md) is the capstone — the default-private, opt-in, machine-enforced publishing pipeline behind the site you're reading, and the two-voice rule (the author's notes and the LLM's organization never blend) that explains why this very page carries a provenance banner.

## The notes

- [How This Wiki Was Built](../notes/how-this-wiki-was-built.md) — The meta-note: the privacy model (a note is private unless its frontmatter says otherwise; the LLM nominates, a human approves), the leak linter, and the Karpathy-style two-layer structure this wiki uses.
- [Knowledge Management System](../notes/knowledge-management-system.md) — The vault design underneath: PARA structure, capture-and-distill automation, and the weekly review ritual that keeps the system from going write-only.
- [Backend Services for AI Coding Agents](../notes/backend-services-for-ai-coding-agents.md) — A 2026 survey of BaaS platforms, vector stores, deployment services, and automation backends ranked by how well CLI-driven agents like Claude Code can operate them. Top picks: Supabase, pgvector, Railway.
- [Turning AI Into a World-Class Designer (Anshu Chimala)](../notes/turning-ai-into-a-world-class-designer-anshu-chimala.md) — Why AI design output is generic by default, and seven techniques (seed strings, critic subagents, ruthless deletion) for directing it through a real design process.
- [Claude Prompts](../notes/claude-prompts.md) — A short working note: prompting Claude to act as a senior engineer explaining conversationally to a technical PM, and to build solutions progressively like a staff engineer.
- [Great Product Development](../notes/great-product-development.md) — The product process frame: Discover, Frame, Build, Learn — de-risk value, usability, feasibility, and viability by testing the riskiest assumption first.

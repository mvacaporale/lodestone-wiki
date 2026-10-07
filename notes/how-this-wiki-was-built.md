---
title: How This Wiki Was Built
tags:
- wiki
- publishing
- pkm
- llm
- meta
- obsidian
summary: How this public wiki is generated from a private Obsidian vault — the opt-in privacy model, the LLM curator, the leak linter, and the two-layer Karpathy-style build.
---

# How This Wiki Was Built

Everything you're reading here started as a note in my private Obsidian vault. This page explains the system that decides what gets published and how the wiki gets assembled, so you can replicate it if you want. The design goal was simple to state and easy to get wrong: **make sharing effortless without ever making privacy a judgment call made by software.**

## The vault underneath

My vault is organized with the PARA method (Projects, Areas, Resources, Archives). Every note carries YAML frontmatter — a `type` (note, capture, highlights, moc), `tags`, and a one-line `summary`. That metadata turns out to be the load-bearing asset: an LLM can triage hundreds of notes from frontmatter alone, cheaply, before ever reading full contents.

## The privacy model: default-private, opt-in, machine-enforced

Three rules, in order of importance:

1. **A note is private unless its frontmatter says `share: public`.** There is no "public folder," no pattern-matching, no model deciding at publish time. One greppable flag is the single source of truth, and the vault itself is the audit log of what's shared.
2. **The LLM nominates; a human approves.** A scheduled curator job looks at new and edited notes, scores them for general-audience interest, screens for privacy risk, and queues candidates with a one-line pitch. Nothing it does sets the flag — I do that in a review pass. If the model has a bad night, the blast radius is a bad *suggestion*, not a leak. Declined notes get an explicit `share: private` so they're never re-nominated.
3. **Publishing is a build step, not access control.** A script copies only flagged notes into a separate public output. The public surface physically never contains private content, so there's no permission system to misconfigure. On the way out, a **leak linter** rejects any note containing the leak patterns we actually found when auditing the backlog: personal AI-chat share URLs, wikilinks pointing at unpublished notes (those leak private note *titles*), dollar amounts, private names, local file paths.

That third rule came from experience: when I audited ~390 existing notes for the initial build, almost none of the privacy problems were in the prose. They were in the margins — a context line mentioning a portfolio figure, a link to a raw capture, a chat-share URL.

## The wiki layer: two voices, never blended

The structure borrows directly from Andrej Karpathy's LLM-wiki idea: raw sources are immutable; an LLM owns a synthesis layer on top.

- **Leaf pages are my notes, verbatim.** Nothing attributed to me was written by a model at publish time.
- **The organizational layer — topic pages, cross-links, synthesis intros — is LLM-generated** at build time (not on each visit), and every generated page is labeled as such, with links to the source notes it draws from.

The attribution rule is inherited from an internal wiki I'd already been running inside the vault: *my thinking* and *collected material* never blend in one voice. A reader should always know whether they're hearing me, a source I collected, or the machine that organized the shelf.

Third-party material — book highlights, podcast transcripts — stays out entirely. That's a copyright boundary, not a privacy one, and it's enforced the same way: those note types are never nominated.

## The moving parts

- **Obsidian** — the vault, plain Markdown + YAML.
- **Claude Code** — ran the backfill audit (parallel agents vetting every note for privacy, copyright, and interest), and powers the curator.
- **An always-on Linux box** — runs the weekly curator and the publish build on systemd timers; the vault syncs to it continuously.
- **A public GitHub repo** — receives the built wiki, including an `llms-full.txt` concatenation so you can point any LLM at one URL and ask questions about all of it.

If you keep only one idea from this page: separate *nomination* from *approval*, and make publication a physical copy of an explicit allowlist. Everything else — the wiki structure, the tooling, the cadence — is swappable.

---

*Related: I also publish a [weekly digest](https://github.com/mvacaporale/weekly-digest) — an automated Friday-morning roundup with its own RSS feed, built on the same vault-plus-timers infrastructure.*

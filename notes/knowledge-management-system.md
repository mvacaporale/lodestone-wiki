---
title: Knowledge Management System
tags:
- knowledge-management
- obsidian
- ai-tools
- personal-workflow
summary: Outlines components, tools, and workflows for a personal knowledge management system, focusing on Obsidian, AI integration, and information processing.
---

# Knowledge Management System

## **LLM Clipper**
Should autosave on exit
Should save to obsidian or Notion (but not both) 
Should auto process with an LLM
Then they should be sent to a RAG database


## **Obsidian**
"you focus on capture, and the system handles structure, connection, and retrieval"

Project and Areas -> Folder Structure (thing to automate is against decay of context)
Resources -> Graph Structure w/ YAML Frontmatter + Backlinks (thing to automate is consolidation)

-> auto-distillation of saved context
	* archive obviously not relevant 
	* a review with you for ambiguous
-> auto-archive of project context

Note contains
* context: why, when, where it matter
* summary:*

## **Read Later**

I'll just use my reader setup + book setup

## **Keeping Up**

These have
* sources (editable)
* topics to explore

These run as scheduled research/search prompts

Weekly synthesis of topics
* current events
* ai updates

## **Weekly Review**

The ritual that keeps the system alive. Without it, captures accumulate, tasks go stale, and standards slip.

### Flow

**1. Ensure Defined Scope**
- Every project/area needs an `_index.md`
- Projects: Is the Outcome clear and specific?
- Areas: Is the Standard articulated?
- Fuzzy targets = fuzzy results

**2. Reflect on Priorities**
- Are these the right projects/areas to have active?
- What should be paused, archived, or promoted?
- Does the current set reflect what actually matters?

**3. Process Captures**
- Review all `type: capture` notes
- For each: develop into a `note`, move to a project/area, or delete
- Goal: inbox zero for raw thoughts

**4. Review Project `_index.md` Files**
- For each active project:
	- Are the 3-7 tasks still the right committed actions?
	- Move completed tasks out, pull from Ideas if needed
	- Gut check: Am I still clear on the Outcome?
- Archive any completed projects

**5. Check Area Standards**
- For each area: Am I above or below the standard?
- If below, does a task need to be added?
- Key question: What's been neglected?

**6. Tend to Stale Items**
- Use `last_edited` to surface notes that haven't been touched
- Decide: still relevant? needs attention? archive?

**7. Look Ahead**
- What's coming this week that needs prep?
- Any projects to activate or pause?
- Update tasks accordingly

### The Core Rhythm

```
Inputs (captures) → Processing → Committed actions (tasks) → Review of standards/outcomes
```

The review closes the loop—without it, the system becomes write-only.

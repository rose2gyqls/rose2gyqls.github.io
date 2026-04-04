---
layout: post
title: "How I Use Obsidian as a PhD Research Database"
date: 2026-04-04 13:00:00 +0900
description: "A working note on how I am turning Obsidian into a literature database, idea incubator, and project operating system for medical AI research."
tags: [obsidian, research, phd, medical-ai, productivity]
---

This post is a working document rather than a finished manifesto. I am currently restructuring my Obsidian vault so it can function as a real research database for my PhD life in medical AI, not just as a note-taking app. The goal is simple: make it easier to store papers, generate ideas, connect them to active projects, and keep my day-to-day research context visible without scattering it across too many tools.

At the moment, I am using this system around four active research lines: `MapOMOP`, `KG Agent`, `Holter`, and `ECGFM`. On top of that, I also need room for proposal writing and lab operations. So the vault is being designed not as a generic second brain, but as an operating system for actual doctoral work.

## Why I am using Obsidian this way

What I need most is not just a place to archive information. I need a system that does four things well:

1. Store papers in a way that remains searchable and reusable.
2. Help me turn reading into project-relevant ideas.
3. Keep the current state of each project visible.
4. Preserve enough daily and weekly context to avoid rethinking the same thing over and over.

For me, the key shift is treating Obsidian as a structured Markdown database rather than a pile of notes. A paper should not remain only as a PDF. An idea should not remain only in a daily note. A project should not depend on my memory of what I was thinking last week.

## The operating principle

The current system follows one main flow:

`capture -> distill -> connect -> execute -> review`

More concretely:

- raw capture goes into an inbox
- papers and external materials get distilled into source notes
- reusable knowledge becomes concept notes
- promising directions become idea notes
- active work is routed into project hubs
- daily and weekly logs preserve research context, but do not become the final home of important knowledge

This distinction matters because different notes have different jobs. A paper note is not the same as a concept note. A project hub is not the same as a daily note. Once these roles are separated, the vault becomes much easier to search and maintain.

## My current folder structure

Here is the structure I am now using:

```text
00_System/
01_Maps/
02_Sources/
  Papers/
  Reviews/
  Datasets/
  Tools/
03_Concepts/
  Methods/
  Clinical/
  Data/
  Evaluation/
04_Projects/
  MapOMOP/
  KG Agent/
  Holter/
  ECGFM/
  Proposals/
  Lab Ops/
05_Prompts/
06_Logs/
  Daily/
  Weekly/
  Meetings/
  Reading/
07_Ideas/
  Seeds/
  Experiments/
90_Inbox/
_Templates/
_Attachments/
```

Each top-level folder has a clear role.

### `00_System`

This is where I keep the operating rules of the vault itself: workflow rules, metadata conventions, and note design principles. This folder is for system logic, not for storing research content.

### `01_Maps`

This is the dashboard layer. It includes high-level views such as:

- a PhD dashboard
- a literature dashboard
- a project portfolio
- an idea incubator
- an operations dashboard

These notes are not the source of truth. They are views into the rest of the vault.

### `02_Sources`

This is the intake layer for external material.

- `Papers/` stores one note per paper or preprint
- `Reviews/` stores surveys and review articles
- `Datasets/` stores notes on datasets, benchmarks, and cohorts
- `Tools/` stores notes on libraries, repositories, and research tools

This folder matters a lot because I want Obsidian to act as my paper database. The important thing is that I am not just saving a PDF. I am saving a distilled Markdown note that explains why the paper matters, what it actually claims, what its limitations are, and whether it sparks a new idea.

### `03_Concepts`

This is where paper-specific notes become reusable knowledge.

- `Methods/` for model, algorithm, or pipeline concepts
- `Clinical/` for domain knowledge and medical context
- `Data/` for dataset design, labeling, leakage, cohort definitions, and so on
- `Evaluation/` for metrics, validation design, error analysis, and clinical usefulness

If a paper note says, "This paper uses temporal validation to avoid leakage," the paper note belongs in `02_Sources`, but the reusable understanding of temporal validation belongs in `03_Concepts`.

### `04_Projects`

This is the execution layer.

The four active research projects each get their own hub:

- `MapOMOP`
- `KG Agent`
- `Holter`
- `ECGFM`

There are also separate spaces for:

- `Proposals/`
- `Lab Ops/`

The reason I separate these is that proposal work and operational tasks are real parts of PhD life, but they should not pollute the logic of the core research projects.

### `05_Prompts`

This is for reusable prompts only. I do not want to save every prompt I ever write. I only want to store prompts that solve a recurring research task, such as:

- paper distillation
- idea expansion
- critique of an experiment design
- reviewer response drafting
- proposal structuring

### `06_Logs`

This is the time-based record.

- `Daily/` for daily steering
- `Weekly/` for reflection and planning
- `Meetings/` for advisor meetings, lab meetings, and collaborations
- `Reading/` for reading sessions that might later get promoted into more permanent notes

The critical rule here is that logs store context, not durable knowledge. If something matters later, it should be promoted out of the logs.

### `07_Ideas`

This is where I want to do more deliberate idea work.

- `Seeds/` for early fragments
- `Experiments/` for more concrete hypotheses or testable directions

This folder exists because some of the most important research moves start as vague but potentially valuable connections between papers, methods, and project problems.

### `90_Inbox`

This is the fast capture layer. It is allowed to be messy, but only temporarily. Notes should move out of this folder once I know what they really are.

## The note lifecycle I want

One reason I am writing this system down is that I do not want everything to collapse into daily notes. My intended lifecycle looks like this:

1. Capture something quickly in `90_Inbox` or `06_Logs/Daily`.
2. If it is a paper, distill it into `02_Sources/Papers`.
3. If it contains a reusable principle, promote that into `03_Concepts`.
4. If it suggests a new direction, create an idea note in `07_Ideas`.
5. If it becomes actionable, link it into one of the project hubs under `04_Projects`.

This makes it possible to read widely without losing the thread of why something mattered.

## What a paper note needs to do

The paper note is the center of the whole system right now.

I do not want a paper note to be a long copy-paste summary. I want it to answer:

- Why does this paper matter for my research?
- What problem does it solve?
- What is the core method or insight?
- What evidence is actually convincing?
- What are the limitations?
- Did it generate any project-specific ideas?
- Is there an immediate next action?

So the paper note template currently emphasizes:

- why this paper matters
- one-paragraph summary
- research question
- key findings
- method and data
- limitations
- idea sparks
- follow-up actions

That is much closer to how I actually read papers during a PhD than a conventional literature memo.

## Why I separated papers, concepts, ideas, and projects

This is probably the single most important design decision.

If I keep everything in one flat layer, then I end up with a pile of notes that are individually fine but collectively not very useful. Separating them forces a distinction between:

- what I read
- what I learned
- what I might do
- what I am doing now

That separation is what allows the vault to support idea generation instead of just storage.

## Metadata and dashboards

I am also using metadata so the vault can be queried and reorganized later. The specific fields will probably evolve, but the current direction is:

- `type`
- `status`
- `projects`
- `topics`
- `summary`
- paper-specific fields such as `authors`, `year`, `venue`, `methods`, `paper_stage`, and `priority`

The point of this is not administrative perfection. The point is to make the vault queryable. Once notes have reliable frontmatter, I can build dashboards that show things like:

- papers I still need to read
- papers already distilled
- ideas that are ready to test
- projects with unclear current focus
- proposal work with deadlines

That turns Obsidian from a passive archive into an active research interface.

## What I still need to refine

This system is still in progress. The next things I need to make more opinionated are:

### 1. Naming rules

I still need a strict naming scheme, especially for paper notes, meeting notes, proposal notes, and idea notes. Good naming matters because search, sorting, and consistency break quickly if I improvise too much.

### 2. Metadata depth

I need to decide which fields are actually worth maintaining in medical AI. For example, it may be useful to add fields such as:

- `modality`
- `task`
- `dataset`
- `clinical_setting`
- `external_validation`
- `code_available`

But too many fields can also become overhead.

### 3. Prompt library standards

I want to keep only high-value prompts, not every prompt. So I still need a rule for what deserves to become a reusable prompt asset.

### 4. Weekly review discipline

The system only works if I regularly move good material out of logs and into stable notes. That means weekly review is not optional.

## Why I think this matters for research productivity

Most productivity systems become useless for research when they optimize only for task capture. Research is not just about tasks. It is about building a memory of questions, failed lines of thought, promising fragments, recurring methods, and useful papers.

What I am trying to build is a system where:

- papers are easy to retrieve
- ideas are easier to revisit
- projects are easier to steer
- context is easier to recover

That is the kind of structure that reduces friction not by making me "more organized" in the abstract, but by lowering the cost of thinking across time.

## Current status

As of April 4, 2026, I have:

- restructured the vault into papers, concepts, ideas, projects, prompts, and logs
- created dedicated project hubs for `MapOMOP`, `KG Agent`, `Holter`, and `ECGFM`
- separated proposal work and lab operations from core project space
- created dedicated templates for paper, idea, proposal, meeting, weekly review, and project notes
- added dashboard notes for literature, ideas, operations, and overall PhD tracking

The system is not finished yet, but it is now opinionated enough that I can start using it as a real research database instead of a vague note collection.

## Update log

### 2026-04-04

- defined the overall vault structure
- clarified the role of each top-level folder
- established the paper -> concept -> idea -> project workflow
- created the first version of templates and dashboards

I expect to keep updating this post as the system becomes more concrete in actual use.

# Repo Structure Setup Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build the folder structure, roadmap tracker, and first article scaffold for the weekly Azure blog repo.

**Architecture:** Three top-level concerns — `notes/` (free-form), `articles/` (one folder per week with draft/final/corrections), and `roadmap.md` (single source of truth for topic status). No build system or tooling needed; this is a pure markdown content repo.

**Tech Stack:** Markdown, Git

---

## File Map

| Action | Path | Purpose |
|--------|------|---------|
| Create | `notes/.gitkeep` | Keep empty notes/ dir tracked in git |
| Create | `articles/2026-W20-what-is-azure-a-beginners-map/draft.md` | First article draft scaffold |
| Create | `articles/2026-W20-what-is-azure-a-beginners-map/corrections.md` | Corrections log template |
| Create | `roadmap.md` | Master topic planning table |
| Modify | `CLAUDE.md` | Document repo structure and workflow |

---

### Task 1: Create notes directory

**Files:**
- Create: `notes/.gitkeep`

- [ ] **Step 1: Create the file**

```
notes/.gitkeep   (empty file)
```

- [ ] **Step 2: Commit**

```bash
git add notes/.gitkeep
git commit -m "chore: add notes directory"
```

---

### Task 2: Create articles directory and first article scaffold

**Files:**
- Create: `articles/2026-W20-what-is-azure-a-beginners-map/draft.md`
- Create: `articles/2026-W20-what-is-azure-a-beginners-map/corrections.md`

- [ ] **Step 1: Create draft.md scaffold**

```markdown
# What is Azure? A Beginner's Map

**Week:** W20 (2026-05-11)
**Status:** drafting
**Dev.to URL:** (fill after publish)

---

## Outline

- Introduction
- What problems does Azure solve?
- Core service categories (Compute, Storage, Networking, Identity)
- How Azure is organized (Regions, Resource Groups, Subscriptions)
- Summary / what to learn next

---

## Draft

(Write your draft here. Chinese/English mix is fine at this stage.)
```

- [ ] **Step 2: Create corrections.md template**

```markdown
# Corrections — W20: What is Azure? A Beginner's Map

## Summary of Changes

(Claude fills this in after correction session)

## Recurring Patterns to Watch

(Claude flags repeated mistakes here)

## Vocabulary / Phrases Learned

(Notable expressions worth remembering)
```

- [ ] **Step 3: Commit**

```bash
git add articles/
git commit -m "chore: scaffold W20 article and corrections template"
```

---

### Task 3: Create roadmap.md

**Files:**
- Create: `roadmap.md`

- [ ] **Step 1: Create roadmap.md**

```markdown
# Azure Roadmap — Article Tracker

> Status flow: `planned` → `drafting` → `reviewing` → `published`

| Week | Topic | Status | Dev.to URL |
|------|-------|--------|------------|
| W20 | What is Azure? A Beginner's Map | drafting | |
| W21 | Azure Identity: Entra ID vs Traditional AD | planned | |
| W22 | Azure Resource Manager & Resource Groups | planned | |
| W23 | Azure Networking Basics: VNet, Subnet, NSG | planned | |
| W24 | Azure Storage: Blob, Table, Queue, File | planned | |
| W25 | Azure Compute: VMs, App Service, Functions | planned | |
| W26 | Azure Monitor & Log Analytics | planned | |
| W27 | Azure Policy & Governance | planned | |
| W28 | Azure Cost Management | planned | |
| W29 | Introduction to IaC on Azure | planned | |
| W30 | Azure Bicep: First Steps | planned | |
| W31 | Bicep vs Terraform: A Real-World Comparison | planned | |

## Correction Level

**Current:** Level 1 — full correction + explanation of every change + flag recurring errors.  
Upgrade to Level 2 (hints only, no direct answers) when user decides they're ready.
```

- [ ] **Step 2: Commit**

```bash
git add roadmap.md
git commit -m "docs: add article roadmap tracker"
```

---

### Task 4: Update CLAUDE.md

**Files:**
- Modify: `CLAUDE.md`

- [ ] **Step 1: Replace CLAUDE.md content**

```markdown
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Weekly English articles on Azure certification topics. Goals: learning record + English writing practice.  
Publication platform: **Dev.to**.

## Repo Structure

```
azure_roadmap/
├── notes/                              # Free-form learning notes — any format, no rules
├── articles/
│   └── YYYY-WXX-kebab-case-title/
│       ├── draft.md                    # Raw draft (Chinese/English mix OK)
│       ├── final.md                    # Corrected final version for Dev.to
│       └── corrections.md             # Key corrections and recurring patterns
├── roadmap.md                          # Topic planning table — source of truth for status
└── docs/superpowers/                   # Design specs and implementation plans
```

## Article Correction Workflow

**Level 1 (current):**
1. User writes `draft.md` and pastes it in conversation (or commits and asks Claude to read it)
2. Claude outputs: corrected full article + explanation of each significant change + flags recurring errors
3. User saves corrected version as `final.md`
4. Claude writes `corrections.md` summarizing key patterns

Upgrade to Level 2 (Claude points out problems without giving answers) when user requests it.

## Topic Roadmap

See `roadmap.md` for the full W20–W31 topic plan and current status.
```

- [ ] **Step 2: Commit**

```bash
git add CLAUDE.md
git commit -m "docs: update CLAUDE.md with repo structure and workflow"
```

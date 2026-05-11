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

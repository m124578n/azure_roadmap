# Design: Azure Roadmap Weekly Blog

**Date:** 2026-05-11  
**Status:** Approved

## Goals

1. Write one English article per week focused on Azure certification topics
2. Build a learning record that is publicly accessible
3. Practice and improve English writing over time
4. Use AI-assisted correction to accelerate English learning (not just fix, but understand why)

## Repo Structure

```
azure_roadmap/
├── notes/                          # Unstructured learning notes, any format/naming
├── articles/
│   └── YYYY-WXX-kebab-case-title/
│       ├── draft.md                # Raw draft (Chinese/English mix is fine)
│       ├── final.md                # Corrected final version (used for Dev.to)
│       └── corrections.md          # Key correction points from this article
├── roadmap.md                      # Topic planning table with status tracking
└── CLAUDE.md
```

Folder naming convention: `YYYY-WXX-kebab-case-title` (ISO week number for easy sorting).

## Article Lifecycle

```
draft.md → correction session → final.md + corrections.md → publish to Dev.to
```

1. User writes draft and saves as `draft.md` (Chinese/English mix allowed)
2. User pastes draft in conversation or commits and asks Claude to read it
3. Claude outputs:
   - Full corrected article ready to paste into Dev.to
   - Explanation of each significant change (why, not just what)
   - Note of recurring errors ("you've made this mistake 3 times now")
4. User saves final version as `final.md`
5. Claude summarizes correction highlights into `corrections.md`

## Correction Levels

**Level 1 (current):**
- Fix all grammar errors
- Improve sentence flow and naturalness
- Explain the reason for each significant change
- Flag recurring patterns the user keeps making

**Level 2 (when user is ready):**
- Point out problems without giving the answer
- User revises, then Claude reviews the revision

Upgrade is user-initiated — no fixed timeline.

## Topic Roadmap (W20–W31)

| Week | Topic | Status |
|------|-------|--------|
| W20 | What is Azure? A Beginner's Map | planned |
| W21 | Azure Identity: Entra ID vs Traditional AD | planned |
| W22 | Azure Resource Manager & Resource Groups | planned |
| W23 | Azure Networking Basics: VNet, Subnet, NSG | planned |
| W24 | Azure Storage: Blob, Table, Queue, File | planned |
| W25 | Azure Compute: VMs, App Service, Functions | planned |
| W26 | Azure Monitor & Log Analytics | planned |
| W27 | Azure Policy & Governance | planned |
| W28 | Azure Cost Management | planned |
| W29 | Introduction to IaC on Azure | planned |
| W30 | Azure Bicep: First Steps | planned |
| W31 | Bicep vs Terraform: A Real-World Comparison | planned |

Topics are subject to adjustment. W31 (Bicep vs Terraform) is expected to be the most content-rich article due to first-hand IaC evaluation experience at work.

## Publication Platform

**Dev.to** — better engineering community reach than Medium, free, and English technical articles strengthen LinkedIn profile and job applications.

## Notes Directory

The `notes/` directory is intentionally free-form — no template, no required structure. Raw learning notes, lab outputs, exam prep dumps. Naming is up to the user.

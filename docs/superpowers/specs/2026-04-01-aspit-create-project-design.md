# ASPIT Create Project Skill Design

**Date:** 2026-04-01
**Status:** Approved
**Author:** Claude Code

---

## Overview

Create a new Claude Code skill called `aspit-create-project` that generates larger-scale project assignments for ASPIT courses. This complements the existing `aspit-create-exercise` skill by handling multi-day projects (1 day to 2 weeks) instead of short practice exercises.

---

## Problem Statement

The existing `aspit-create-exercise` skill handles small practice activities (10-30 minutes). ASPIT needs a way to generate larger project-based assignments that:
1. Synthesize multiple curriculum concepts
2. Span 1-14 days of work
3. Provide appropriate scaffolding (medium level)
4. Include starter files and example solutions

---

## Design

### Skill Name

`aspit-create-project`

### Skill Inputs

| Input | Description | Example | Required? |
|-------|-------------|---------|----------|
| **Module** | Course level | W1, W2, W3.1, W3.2 | Yes |
| **Topics** | Curriculum files OR topic descriptions | `06-js-functions.md` OR "functions, arrays, DOM" | Yes |
| **Time Scale** | Project duration | "1 day", "3 days", "1 week", "2 weeks" | Yes |
| **Project Name** | Descriptive name (kebab-case) | "personal-portfolio", "quiz-game" | Optional (auto-generated if omitted) |
| **Project Type** | Optional category for customization | "website", "game", "tool", "app" | Optional |

### Time-Based Scaling

| Scale | Time | Task Count | Milestones | File Count |
|-------|------|------------|------------|------------|
| **Short** | 1-2 days | 8-12 tasks | 2-3 | 2-4 files |
| **Medium** | 3-5 days | 15-25 tasks | 4-6 | 4-7 files |
| **Long** | 1-2 weeks | 30-50 tasks | 8-12 | 7-12 files |

### Folder Structure

```
{module}/projects/project-{XX}-{project-name}/
    ├── README.md
    ├── starter-files/
    │   ├── [project-specific files]
    └── example-solution/
        └── [complete working example]
```

### README Template Structure

```markdown
# Project: [Title]

## Overview
[Description + real-world connection]

## Learning Objectives
- [ ] [Objective 1]
- [ ] [Objective 2]

## Prerequisites
- Completed [lessons]
- [Other requirements]

## Project Scope
**Time Estimate**: ~X days
**Difficulty**: [Level]

## Requirements

### Functional Requirements
- [Requirement 1]
- [Requirement 2]

### Technical Requirements
- [Technical constraint 1]
- [Technical constraint 2]

## Milestones
[Milestone 1]
- Tasks
- Verification criteria

[Repeat for each milestone]

## Starter Files
[Description of provided templates]

## Success Criteria
[Completion checklist]

## Common Issues
[Troubleshooting section]

## Extension Ideas
[Optional enhancements]
```

### Key Differences from Exercise Skill

| Aspect | Exercise Skill | Project Skill |
|--------|---------------|---------------|
| **Scope** | Single concept | Multi-concept synthesis |
| **Duration** | 10-30 minutes | 1-14 days |
| **Structure** | Sequential tasks | Milestone-based phases |
| **Files** | 1-3 files | 2-12 files |
| **Difficulty** | Easy/Medium/Hard | Time-based tiers |
| **Solutions** | Inline folder | Separate example-solution |

---

## Implementation Notes

1. **Always include starter files** - Generate appropriate templates based on project scope
2. **Medium scaffolding** - High-level requirements with milestones, less prescriptive than exercises
3. **Neurodiversity-friendly** - Follow CLAUDE.md accessibility guidelines
4. **Topic flexibility** - Accept both file paths and topic descriptions
5. **Consistent with existing patterns** - Mirror exercise skill structure where applicable

---

## Success Criteria

- [ ] Skill file created at `.claude/skills/aspit-create-project/SKILL.md`
- [ ] Skill generates projects for all modules (W1, W2, W3.1, W3.2)
- [ ] Time-based scaling produces appropriate scope
- [ ] Starter files are generated for all projects
- [ ] Example solutions are included
- [ ] README follows neurodiversity-friendly guidelines
- [ ] User can specify topics via file path or description

---
name: aspit-create-exercise
description: Use when creating ASPIT course exercises for any module (W1/W2/W3.1/W3.2). Reads curriculum article, generates specified number of exercises at chosen difficulty levels, follows neurodiversity-friendly README template from CLAUDE.md. Use when user requests "create X exercises" or "generate practice materials".
---

# ASPIT Exercise Creation

## Overview

This skill guides the creation of ASPIT (autism-friendly) coding exercises. Exercises are self-contained practice activities that reinforce curriculum concepts. Each exercise includes a README with explicit instructions, starter files, and troubleshooting guidance.

**Core principle:** Exercises must be neurodiversity-friendly - explicit language, numbered steps, clear success criteria, and troubleshooting for common issues.

## Inputs Required

Before starting, gather these from the user:

| Input | Description | Example | Required? |
|-------|-------------|---------|----------|
| **Module** | Course level | W1, W2, W3.1, W3.2 | Yes |
| **Curriculum file** | Source lesson to base exercises on | `08-css-selectors.md` | Yes |
| **Exercises needed** | Count and difficulty levels | "2 easy, 1 medium" or "3 hard" | Yes |
| **Exercise names** | Descriptive names (kebab-case) | Derived from curriculum or user-provided | Optional |

**Example user request:**
> "Create 3 exercises for W1 based on 08-css-selectors.md: 1 easy, 1 medium, 1 hard"

## Folder Structure Pattern

```
{module}/exercises/{XX}-{difficulty}/{YY}-{exercise-name}/
    ├── README.md
    ├── index.html (or other starter file)
    └── styles.css (or exercise-specific files)
```

**Naming conventions:**
- `XX` = Difficulty level number (01, 02, 03...)
- `difficulty` = `easy`, `medium`, or `hard`
- `YY` = Exercise number within difficulty (01, 02, 03...)
- `exercise-name` = kebab-case descriptive name

**Examples:**
```
W1/exercises/04-css-fundamentals/01-easy/01-styled-greeting/
W1/exercises/05-css-selectors/02-medium/01-id-chaining/
W2/exercises/01-js-basics/03-hard/02-function-practice/
```

**Important:** Use number prefixes on difficulty folders to ensure correct sort order:
- `01-easy/`, `02-medium/`, `03-hard/` (NOT `easy/`, `medium/`, `hard/`)

## Difficulty Guidelines

Use these as default guidance. Adjust based on curriculum complexity.

| Difficulty | Time Estimate | Task Count | Concepts |
|------------|---------------|------------|----------|
| **Easy** | ~10 minutes | 2-4 tasks | Single concept, explicit instructions |
| **Medium** | ~20 minutes | 5-7 tasks | 2-3 concepts, some combination |
| **Hard** | ~30 minutes | 8-12 tasks | Multiple concepts, higher complexity |

**Scaling difficulty:**
- **Easy**: Students fill in declarations only, or write simple selectors
- **Medium**: Students write declarations, combine 2-3 properties, basic selector patterns
- **Hard**: Students write full rules, complex selectors, multiple concepts together

## README Template

Every exercise README MUST follow this structure:

```markdown
# Exercise: [Descriptive Title]

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] [Specific, actionable objective 1]
- [ ] [Specific, actionable objective 2]

## Prerequisites

Before starting this exercise, you should have:

- Completed "[Curriculum Lesson Name]" ([lesson-file].md)
- [Previous exercise if building on concepts]
- [Any other specific requirements]

## What You'll Build

[Brief description of what student will create]

[Additional context - what this demonstrates, real-world connection]

## Tasks

1. **[Action step with clear directive]** - [Specific instruction]
   - [Sub-bullet with exact property/value if needed]

2. **[Next action step]** - [Specific instruction]

[Number all steps. Never group multiple actions in one step.]

## Expected Result

[Visual or text description of what completed exercise looks like]

[Key features to verify - bullets or simple format]

## How to Check Your Work

1. **[Verification step 1]**
   - [What to check]

2. **[Verification step 2]**
   - [What to verify]

[Give students concrete ways to validate their work]

## Common Issues

### Issue: [Symptom students might see]

**Possible cause:** [Most likely reason]

**Fix:** [Specific solution with example if helpful]

[Include 3-5 common issues based on curriculum concepts]

## Time Estimate

~X minutes
```

## Neurodiversity Guidelines (From CLAUDE.md)

### Language & Communication

- **Use explicit, unambiguous language** - avoid "try this", "play around with"
- **Provide concrete examples before abstract concepts** - show, then explain
- **Break complex tasks into numbered, sequential steps** - never group multiple actions
- **Include clear success criteria** - define what "done" looks like
- **Use consistent terminology** - match language used in curriculum
- **Anticipate common confusion points** - address proactively in Common Issues

### Visual Structure

- **Use clear headings** - H1, H2, H3 hierarchy
- **Employ lists extensively** - numbered for sequences, bulleted for options
- **Format code blocks clearly** - always specify language
- **Provide visual separation** - horizontal lines between sections
- **Create clear checkpoints** - help students track progress

### Content Presentation

- **Include validation checkpoints** - ways to verify work
- **Offer multiple explanation approaches** when possible (analogy + example + technical)
- **Include troubleshooting sections** - common issues with specific fixes

## Starter File Patterns

### HTML Files

- Always include `<!DOCTYPE html>` and `<html lang="en">`
- Include `<link rel="stylesheet" href="styles.css">` for CSS exercises
- Use extensive comments explaining what each section does
- Pre-fill content that students will style (don't make them write HTML if focus is CSS)

**Example HTML structure:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Exercise Title</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Content with comments -->
    <h1>Heading to style</h1>
    <p class="description">Paragraph with class</p>
</body>
</html>
```

### CSS Files

Two patterns based on exercise focus:

**Pattern A: Selectors pre-written (CSS fundamentals)**
```css
/*
 * Exercise: [Title]
 *
 * Your task: Write CSS declarations inside each selector.
 */

/* TASK: Style the heading */
h1 {
    /* Write your CSS here */
}
```

**Pattern B: Empty file (CSS selectors/advanced)**
```css
/*
 * Exercise: [Title]
 *
 * Your task: Write selectors AND declarations.
 * Follow the tasks in README.md
 */

/* Write your CSS here */
```

### JavaScript Files (W2 and above)

- Use `//` comments for single-line explanations
- Include `/* */` for block explanations
- Provide structure but leave implementation to student

## Module-Specific Considerations

### W1 (HTML & CSS Only)

- **No JavaScript** - keep it strictly HTML/CSS
- **External CSS only** - use `<link>` tag, not inline/internal
- **Properties limited to fundamentals** in early exercises: `color`, `background-color`, `font-size`, `font-family`, `text-align`, `text-decoration`
- **Introduce new properties gradually** across difficulty levels

### W2 (HTML, CSS & JavaScript)

- **Build on W1 foundation** - assume HTML/CSS knowledge
- **Introduce JS gradually** - start with console.log, variables, functions
- **Keep CSS simple** - focus on JS concepts, reuse W1 CSS knowledge
- **Include debugging guidance** - JS errors can be cryptic

### W3.1 (Full Stack - PHP/Backend)

- **Separate frontend/backend files** - keep concerns clear
- **Show complete request/response** - help students understand the cycle
- **Include database examples** - show SQL queries and results
- **Debug server errors** - common PHP/database issues

### W3.2 (WordPress)

- **Start with WordPress concepts** - themes, plugins, posts, pages
- **Use practical examples** - real WordPress patterns
- **Explain the ecosystem** - hooks, filters, custom post types
- **Debug plugin conflicts** - common WordPress issues

## Quick Reference

| Task | How |
|------|-----|
| Determine exercise count | Ask user: "How many exercises at each difficulty?" |
| Name exercises | Use kebab-case, descriptive: `styled-greeting`, `selector-chaining` |
| Set time estimate | Easy ~10min, Medium ~20min, Hard ~30min (adjust as needed) |
| Write tasks | Number each step, be explicit about property/values |
| Add troubleshooting | Think: "What will students get wrong?" |
| Verify neurodiversity | Check: explicit language? numbered steps? success criteria? |

## Common Mistakes

### Mistake: Vague task instructions

**Bad:**
> "Style the heading to look nice."

**Good:**
> "Style the heading (`h1`) - Add `color: navy;` and `text-align: center;`"

### Mistake: Grouping multiple actions

**Bad:**
> "Open the files, write the CSS, and check your work in the browser."

**Good:**
> 1. Open `styles.css`
> 2. Add `color: navy;` inside the `h1` selector
> 3. Save both files
> 4. Open `index.html` in your browser

### Mistake: No validation steps

**Bad:** [No "How to Check Your Work" section]

**Good:**
> 1. Open `index.html` in your browser
> 2. Verify the heading is navy blue
> 3. Verify the heading is centered

### Mistake: Missing troubleshooting

**Bad:** [No "Common Issues" section]

**Good:**
> ### Issue: The heading isn't centered
> **Possible cause:** Misspelled `text-align` or forgot hyphen
> **Fix:** Check that you wrote `text-align: center;` (not `textalign: centered`)

### Mistake: Wrong folder sort order

**Bad:**
```
exercises/
├── easy/
├── hard/
└── medium/
```
(Sorts as: easy, hard, medium - wrong order!)

**Good:**
```
exercises/
├── 01-easy/
├── 02-medium/
└── 03-hard/
```
(Sorts correctly: 01-easy, 02-medium, 03-hard)

## Implementation Steps

1. **Get inputs from user** - module, curriculum file, exercise count/difficulties
2. **Read curriculum file** - understand topics covered
3. **Plan exercises** - determine progression, what each exercise covers
4. **Create folder structure** - use numbered difficulty folders
5. **Write READMEs** - follow template exactly, incorporate neurodiversity guidelines
6. **Create starter files** - HTML/CSS/JS with appropriate scaffolding
7. **Review** - check all accessibility checklist items
8. **Verify in browser** - test that exercises work as expected

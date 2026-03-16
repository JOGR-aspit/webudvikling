# ASPIT Teaching Materials Repository

## Repository Overview

This repository contains web development teaching materials designed specifically for students with autism, ADHD, and similar neurodiverse conditions. All materials are created using Claude Code and stored as Markdown files with extensive code examples.

### Curriculum Structure

The curriculum is organized by course levels:

- **W1**: Introduction to Web Development (HTML & CSS only)
- **W2**: Intermediate Web Development (HTML, CSS & JavaScript introduction)
- **W3.1**: Full Stack Web Development (currently PHP, subject to change)
- **W3.2**: WordPress Development

Each course follows a consistent structure for easy navigation.

---

## Neurodiversity-Friendly Guidelines

When creating or modifying content, follow these accessibility principles:

### Language & Communication

- **Use explicit, unambiguous language** - avoid vague instructions
- **Provide concrete examples before abstract concepts** - show, then explain
- **Break complex tasks into numbered, sequential steps** - never group multiple actions together
- **Include clear success criteria** - define what "done" looks like for each task
- **Use consistent terminology** - establish a vocabulary and stick to it
- **Anticipate common confusion points** - address them proactively before they occur

### Visual Structure

- **Use clear headings** - create a visual hierarchy (H1, H2, H3)
- **Employ lists extensively** - use numbered lists for sequences, bulleted lists for options
- **Format code blocks clearly** - always specify the language
- **Provide visual separation** - use horizontal lines or blank space between sections
- **Create clear checkpoints** - help students track their progress

### Content Presentation

- **Provide step-by-step breakdowns** for complex concepts
- **Include validation checkpoints** - ways for students to verify their work
- **Offer multiple explanation approaches** when possible (analogy, concrete example, technical explanation)
- **Include troubleshooting sections** - common issues and their solutions

---

## Content Guidelines

### Markdown Formatting

#### Document Structure

Every document should follow this template:

```markdown
# Title (Clear and Descriptive)

## Learning Objectives
- [ ] Objective 1
- [ ] Objective 2

## Prerequisites
- List what students need to know before starting

## Content
[Main content here]

## Summary
[Brief recap of key points]

## Next Steps
[What to do after completing this material]
```

#### Code Examples

All code examples must:

1. **Be runnable and self-contained** - include all necessary code
2. **Have extensive inline comments** - explain what each line does
3. **Include input/output examples** - show what happens when code runs
4. **Explain non-obvious operations** - don't assume prior knowledge
5. **Be properly formatted** - use syntax highlighting with language specified

Example format:

```html
<!-- This is a comment explaining what this code does -->
<!DOCTYPE html>
<html>
<head>
    <title>Page Title</title>
</head>
<body>
    <!-- This creates a heading -->
    <h1>Hello World</h1>
</body>
</html>
```

#### Instructions

When giving instructions:

1. **Use numbered lists** for sequential steps
2. **Be specific about file names and locations**
3. **Include expected outcomes** - what should students see?
4. **Provide validation steps** - how to verify it's working
5. **Offer troubleshooting tips** - common issues and fixes

### File Naming Conventions

Use **kebab-case** (lowercase with hyphens) for all files:

- `my-first-webpage.md` (not `MyFirstWebPage.md` or `my_first_webpage.md`)
- `assignment-01-basics.md`
- `project-portfolio.md`
- `code-example-variables.md`

Be descriptive but concise. File names should clearly indicate content.

---

## Folder Structure

```
aspit/
├── W1/                     # Introduction to Web Development (HTML & CSS)
│   ├── curriculum/         # Main course content and learning materials
│   ├── assignments/        # Individual assignments and exercises
│   │   └── solutions/      # Assignment solutions (controlled access)
│   ├── projects/           # Course projects and practical work
│   ├── code-examples/      # Extensive, well-commented code examples
│   └── README.md           # Course overview and navigation guide
├── W2/                     # Intermediate Web Development (HTML, CSS & JavaScript)
│   ├── curriculum/
│   ├── assignments/
│   │   └── solutions/
│   ├── projects/
│   ├── code-examples/
│   └── README.md
├── W3.1/                   # Full Stack Web Development (PHP/other backend)
│   ├── curriculum/
│   ├── assignments/
│   │   └── solutions/
│   ├── projects/
│   ├── code-examples/
│   └── README.md
├── W3.2/                   # WordPress Development
│   ├── curriculum/
│   ├── assignments/
│   │   └── solutions/
│   ├── projects/
│   ├── code-examples/
│   └── README.md
├── resources/              # Shared resources across all courses
│   ├── images/             # Screenshots, illustrations, visual aids
│   ├── diagrams/           # Flowcharts, architecture diagrams, UML
│   ├── checklists/         # Step-by-step checklists for common tasks
│   ├── references/         # Reference materials, cheat sheets, quick guides
│   └── external-links/     # Curated external resources and documentation
└── docs/                   # Repository documentation
    ├── setup.md            # Getting started with the repository
    ├── contributing.md     # Guidelines for adding/modifying content
    └── accessibility.md    # Neurodiversity-friendly design principles
```

---

## Content Types

### Curriculum

Main course content including:
- Learning modules and lessons
- Topic-specific deep-dives
- Prerequisite knowledge and foundations
- Reference materials and quick guides

**Location**: Each course's `curriculum/` folder

### Assignments

Individual student work including:
- Solo assignments with clear, isolated tasks
- Practice exercises for skill building
- Assignment templates with structure examples
- **Solutions** stored in `assignments/solutions/` (controlled access)

**Location**: Each course's `assignments/` folder

### Projects

Larger project-based learning including:
- Entry-level projects with detailed guidance
- Mid-level projects with some autonomy
- Advanced projects with minimal scaffolding
- Occasional exam-style assessments (in `projects/exams/` when needed)

**Location**: Each course's `projects/` folder

### Code Examples

Extensive, well-commented code examples including:
- Fundamental programming concepts
- Design patterns and best practices
- Algorithm implementations
- Helper functions and common snippets

**Location**: Each course's `code-examples/` folder

---

## Claude Code Instructions

When using Claude Code to create or modify materials:

### General Approach

1. **Always read existing materials first** - understand the style, tone, and structure
2. **Follow the established patterns** - don't reinvent the wheel
3. **Be explicit about course context** - specify which course (W1, W2, W3.1, W3.2)
4. **Consider the target audience** - students with autism, ADHD, and similar conditions
5. **Use consistent terminology** - check how concepts have been introduced previously

### Course-Specific Guidelines

#### W1 (HTML & CSS Only)

- **Focus on fundamentals** - don't introduce JavaScript
- **Use extensive visual examples** - show what HTML/CSS produces
- **Break down each concept** - explain tags, attributes, properties separately
- **Provide immediate visual feedback** - students see results quickly
- **Include troubleshooting** - common CSS issues and their fixes

#### W2 (HTML, CSS & JavaScript)

- **Build on W1 foundation** - assume HTML/CSS knowledge
- **Introduce JavaScript gradually** - start simple, add complexity slowly
- **Explain the "why"** - why we use JavaScript, what problems it solves
- **Provide clear examples** - show HTML/CSS/JS working together
- **Debug heavily** - show common JavaScript errors and how to fix them

#### W3.1 (Full Stack - PHP/Backend)

- **Connect frontend to backend** - explain the full request/response cycle
- **Use clear analogies** - explain server-side concepts concretely
- **Provide complete working examples** - frontend + backend code together
- **Document database interactions** - show SQL queries and results
- **Debug common issues** - server errors, database connection problems

#### W3.2 (WordPress)

- **Start with WordPress concepts** - explain themes, plugins, posts, pages
- **Use practical examples** - real WordPress sites and their structure
- **Explain the WordPress ecosystem** - themes, plugins, custom post types
- **Debug common issues** - plugin conflicts, theme problems
- **Provide development workflow** - local development, staging, deployment

### Content Creation Steps

When creating new materials:

1. **Define learning objectives** - What should students be able to do?
2. **Identify prerequisites** - What do students need to know first?
3. **Outline the content** - Create a structure before writing
4. **Write with accessibility** - Apply neurodiversity-friendly guidelines
5. **Include code examples** - Make them runnable, commented, and self-contained
6. **Add validation steps** - How can students verify their work?
7. **Provide troubleshooting** - What problems might students encounter?
8. **Review for clarity** - Is every instruction explicit and unambiguous?
9. **Add summary and next steps** - Help students progress forward

### Accessibility Checklist

Before finalizing any content, verify:

- [ ] Language is explicit and unambiguous
- [ ] Concrete examples precede abstract concepts
- [ ] Complex tasks are broken into numbered steps
- [ ] Success criteria are clearly defined
- [ ] Terminology is consistent with previous materials
- [ ] Code examples are runnable and well-commented
- [ ] Visual structure is clear (headings, lists, spacing)
- [ ] Common confusion points are addressed proactively
- [ ] Troubleshooting information is included
- [ ] File follows the standard document structure

---

## Quick Reference

### Creating New Content

```bash
# Navigate to the appropriate course folder
cd W1/  # or W2/, W3.1/, W3.2/

# Create new content in the appropriate subfolder
# For curriculum: W1/curriculum/new-topic.md
# For assignments: W1/assignments/assignment-01.md
# For projects: W1/projects/project-portfolio.md
# For code examples: W1/code-examples/example-variables.md
```

### Common Markdown Patterns

```markdown
# Main Title

## Section Title

### Subsection Title

- Bullet point 1
- Bullet point 2

1. Step one
2. Step two

```language
Code block here
```

> Important note

---

Horizontal separator
```

### Code Commenting Style

```javascript
// Single-line comment explaining what this line does
function exampleFunction(param) {
    // This comment explains the purpose of the next block
    const result = param * 2;  // Multiply by 2

    // Return the calculated result
    return result;
}
```

---

## Getting Help

- **Repository Setup**: See [docs/setup.md](docs/setup.md)
- **Contributing**: See [docs/contributing.md](docs/contributing.md)
- **Accessibility Guidelines**: See [docs/accessibility.md](docs/accessibility.md)
- **Course Overview**: See each course's README.md (W1, W2, W3.1, W3.2)

---

## Important Notes

1. **Always create materials in the appropriate course folder** - Don't mix courses
2. **Solutions go in assignments/solutions/ within each course** - Not at the top level
3. **Use shared resources for cross-course content** - Put reusable content in resources/
4. **Follow the accessibility checklist** - Every piece of content should be neurodiversity-friendly
5. **Maintain consistent structure** - All courses have the same subfolder organization
6. **Be explicit and specific** - Avoid vague instructions or assumptions
7. **Include validation and troubleshooting** - Help students verify and fix their work

---

**Last Updated**: 2026-03-16
**Maintained With**: Claude Code

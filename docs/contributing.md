# Contributing Guidelines

Thank you for your interest in contributing to the ASPIT Teaching Materials Repository! This guide will help you understand how to contribute effectively.

## Table of Contents

1. [Types of Contributions](#types-of-contributions)
2. [Getting Started](#getting-started)
3. [Content Guidelines](#content-guidelines)
4. [Accessibility Requirements](#accessibility-requirements)
5. [File Organization](#file-organization)
6. [Code of Conduct](#code-of-conduct)
7. [Review Process](#review-process)

---

## Types of Contributions

We welcome several types of contributions:

### Content Contributions

- **New curriculum materials** - Lessons, tutorials, and explanations
- **Assignments** - Practice exercises and activities
- **Projects** - Practical applications and capstone work
- **Code examples** - Well-commented, runnable code snippets
- **Solutions** - Assignment and project solutions

### Improvements

- **Bug fixes** - Correct errors in existing materials
- **Clarifications** - Improve explanations that are unclear
- **Additions** - Expand on existing topics with more detail
- **Updates** - Update outdated information or deprecated practices
- **Troubleshooting** - Add common issues and their solutions

### Resources

- **Diagrams** - Visual aids to explain concepts
- **Checklists** - Step-by-step guides for common tasks
- **References** - Quick reference materials and cheat sheets
- **Links** - Curated external resources and documentation

---

## Getting Started

### For Students

If you want to contribute:

1. **Complete the course** - Make sure you understand the material thoroughly
2. **Identify gaps** - Note what's missing or unclear
3. **Create materials** - Write content following these guidelines
4. **Submit for review** - Share with your instructor for feedback

### For Instructors

If you want to contribute:

1. **Review existing materials** - Understand the structure and style
2. **Identify needs** - Determine what's missing or could be improved
3. **Create content** - Follow the content and accessibility guidelines
4. **Test thoroughly** - Ensure all code examples work correctly
5. **Submit for review** - Share with the maintainers

### Workflow

1. **Clone the repository** - Get a local copy
2. **Create a branch** - Work on your contribution separately
3. **Make your changes** - Follow the guidelines below
4. **Test your changes** - Verify everything works correctly
5. **Commit your changes** - Write clear, descriptive commit messages
6. **Submit for review** - Share your work with the maintainers

---

## Content Guidelines

### Document Structure

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

### Writing Style

#### Use Explicit Language

- **Be specific** - Don't say "try this" when you can say "do this"
- **Avoid ambiguity** - Don't leave room for interpretation
- **Be direct** - Say exactly what needs to be done

#### Provide Examples First

- **Show, then explain** - Start with a concrete example
- **Use real code** - Don't use pseudocode or abstract examples
- **Make it runnable** - Ensure examples can be executed

#### Break Down Complex Tasks

- **Use numbered lists** - For sequential steps
- **One action per step** - Don't combine multiple actions
- **Include validation** - Tell students how to verify each step

#### Include Success Criteria

- **Define "done"** - What should students see or be able to do?
- **Provide checkpoints** - Ways to verify progress
- **Show expected output** - What should happen?

### Code Examples

All code examples must:

1. **Be runnable** - Include all necessary code
2. **Be self-contained** - Don't rely on external files (unless specified)
3. **Be well-commented** - Explain what each line does
4. **Show input/output** - Demonstrate what the code produces
5. **Follow best practices** - Use clean, modern code

#### Commenting Style

```javascript
// This is a single-line comment explaining the purpose
function exampleFunction(param) {
    // This comment explains what the next block does
    const result = param * 2;  // Multiply by 2

    // Return the calculated result
    return result;
}
```

### File Naming

- **Use kebab-case** - `my-file-name.md` (not `MyFileName.md`)
- **Be descriptive** - Names should clearly indicate content
- **Be consistent** - Follow existing patterns in the repository

Examples:
- ✅ `assignment-01-basics.md`
- ✅ `code-example-variables.md`
- ✅ `project-portfolio.md`
- ❌ `Assignment1Basics.md`
- ❌ `codeExampleVariables.md`

---

## Accessibility Requirements

### Neurodiversity-Friendly Design

All materials must be accessible to students with autism, ADHD, and similar conditions. Review the detailed guidelines in [accessibility.md](accessibility.md).

### Checklist

Before submitting, verify:

- [ ] Language is explicit and unambiguous
- [ ] Concrete examples precede abstract concepts
- [ ] Complex tasks are broken into numbered steps
- [ ] Success criteria are clearly defined
- [ ] Code examples are runnable and well-commented
- [ ] Visual structure is clear (headings, lists, spacing)
- [ ] Common confusion points are addressed proactively
- [ ] Troubleshooting information is included
- [ ] File follows the standard document structure
- [ ] Terminology is consistent with existing materials

---

## File Organization

### Course-Specific Content

Always place content in the appropriate course folder:

- **W1**: HTML & CSS content only
- **W2**: HTML, CSS, and JavaScript content
- **W3.1**: Full stack development (PHP, backend, databases)
- **W3.2**: WordPress-specific content

### Content Types

Place content in the appropriate subfolder:

- `curriculum/` - Learning materials and lessons
- `assignments/` - Practice exercises
- `assignments/solutions/` - Assignment solutions only
- `projects/` - Larger practical projects
- `code-examples/` - Code snippets and examples

### Shared Resources

Place cross-course resources in:

- `resources/images/` - Visual aids and illustrations
- `resources/diagrams/` - Flowcharts and architecture diagrams
- `resources/checklists/` - Step-by-step guides
- `resources/references/` - Quick reference materials
- `resources/external-links/` - Curated external resources

---

## Code of Conduct

### Respect and Inclusivity

- **Be respectful** - Treat everyone with dignity and respect
- **Be inclusive** - Welcome contributors from all backgrounds
- **Be patient** - Remember that everyone learns at their own pace
- **Be constructive** - Provide helpful, actionable feedback

### Communication

- **Be clear** - Communicate in an explicit, unambiguous way
- **Be kind** - Assume good intentions
- **Be open** - Accept feedback gracefully
- **Be collaborative** - Work together to improve the materials

### Accessibility

- **Prioritize accessibility** - Consider diverse learning needs
- **Follow guidelines** - Adhere to neurodiversity-friendly design principles
- **Seek feedback** - Ask for input from diverse perspectives
- **Iterate** - Continuously improve accessibility based on feedback

---

## Review Process

### Before Submitting

1. **Review your content** - Check for errors and clarity
2. **Test code examples** - Ensure they run correctly
3. **Verify accessibility** - Use the accessibility checklist
4. **Check formatting** - Follow markdown and structure guidelines
5. **Proofread** - Check for typos and grammatical errors

### Submission

1. **Prepare a summary** - Describe what you've contributed
2. **Highlight changes** - Note any significant additions or modifications
3. **Provide context** - Explain why this contribution is valuable
4. **Address feedback** - Be responsive to reviewer comments

### Review Criteria

Contributions will be reviewed based on:

- **Accuracy** - Is the information correct?
- **Clarity** - Is it easy to understand?
- **Accessibility** - Is it neurodiversity-friendly?
- **Consistency** - Does it match existing materials?
- **Quality** - Is the content high-quality and valuable?

### After Review

- **Accept** - If approved, your contribution will be merged
- **Request Changes** - You may be asked to make revisions
- **Decline** - Not all contributions will be accepted

---

## Getting Help

If you need help contributing:

1. **Read the guidelines** - Review this document thoroughly
2. **Check existing materials** - Look at similar contributions
3. **Ask questions** - Don't hesitate to reach out to maintainers
4. **Start small** - Consider starting with minor improvements

---

## Recognition

Contributors will be recognized for their valuable contributions. Thank you for helping make these materials better for everyone!

---

## Additional Resources

- **Content Guidelines**: [CLAUDE.md](../CLAUDE.md) - Detailed content creation guidelines
- **Accessibility Principles**: [accessibility.md](accessibility.md) - Neurodiversity-friendly design
- **Setup Guide**: [setup.md](setup.md) - Getting started with the repository

---

**Last Updated**: 2026-03-16

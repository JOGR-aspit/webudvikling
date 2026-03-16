# Neurodiversity-Friendly Design Principles

This document outlines the accessibility principles for creating teaching materials that are inclusive of students with autism, ADHD, and similar neurodiverse conditions.

## Table of Contents

1. [Understanding Our Audience](#understanding-our-audience)
2. [Core Principles](#core-principles)
3. [Language & Communication](#language--communication)
4. [Visual Structure](#visual-structure)
5. [Content Presentation](#content-presentation)
6. [Code Examples](#code-examples)
7. [Instructions & Tasks](#instructions--tasks)
8. [Common Challenges & Solutions](#common-challenges--solutions)
9. [Checklist](#checklist)

---

## Understanding Our Audience

### Who We Serve

Our teaching materials are designed for students with:

- **Autism Spectrum Disorder (ASD)** - May prefer explicit instructions, clear structure, and reduced ambiguity
- **Attention Deficit Hyperactivity Disorder (ADHD)** - May benefit from engaging content, clear organization, and manageable chunking
- **Similar neurodiverse conditions** - May have varying needs for clarity, structure, and support

### Key Considerations

- **Explicit communication** - Avoid vague or ambiguous language
- **Clear structure** - Provide logical organization and progression
- **Concrete examples** - Show before explaining abstract concepts
- **Manageable complexity** - Break down complex tasks into smaller steps
- **Validation support** - Provide ways to verify understanding and progress

---

## Core Principles

### 1. Be Explicit

**What it means**: Say exactly what you mean, without relying on context or assumptions.

**Examples**:

- ✅ "Click the 'Submit' button in the top-right corner of the screen"
- ❌ "Click submit" (ambiguous - where is it?)
- ✅ "Create a new file named `index.html` in the W1 folder"
- ❌ "Create a file called index" (missing extension and location)

**Why it matters**: Reduces confusion and ensures everyone understands exactly what to do.

### 2. Show Before You Tell

**What it means**: Provide concrete examples before explaining abstract concepts.

**Examples**:

```javascript
// First, show the code
let x = 5;
let y = x + 3;

// Then explain what it does
// The code above creates a variable named 'x' with the value 5,
// then creates a variable named 'y' with the value 8 (5 + 3)
```

**Why it matters**: Concrete examples provide a mental model that abstract explanations can build upon.

### 3. Break It Down

**What it means**: Divide complex tasks into numbered, sequential steps.

**Examples**:

Instead of:
> "Create a webpage with a header, navigation, and footer."

Use:
1. Create the HTML document structure
2. Add a header section at the top
3. Add a navigation bar below the header
4. Add a footer at the bottom

**Why it matters**: Small, sequential steps are easier to follow and less overwhelming.

### 4. Define "Done"

**What it means**: Provide clear success criteria and expected outcomes.

**Examples**:

- "You will know you've completed this task when you see a heading that says 'Welcome' on your webpage"
- "After running the code, you should see the message 'Hello, World!' printed in the console"

**Why it matters**: Students need to know what success looks like to verify their work.

### 5. Anticipate Confusion

**What it means**: Address common misunderstandings before they occur.

**Examples**:

> "Note: Make sure you're using curly quotes (`"` and `'`) not straight quotes. Using the wrong type will cause an error."

**Why it matters**: Prevents frustration by addressing issues proactively.

---

## Language & Communication

### Use Explicit, Unambiguous Language

#### DO

- "Save the file as `index.html` in the `W1/assignments/` folder"
- "Open the file by double-clicking on its icon"
- "Type the code exactly as shown, including all semicolons and brackets"

#### DON'T

- "Save the file" (where? as what?)
- "Open the file" (how? which file?)
- "Type the code" (what code? exactly how?)

### Use Consistent Terminology

Establish a vocabulary and stick to it throughout all materials.

**Example Terms**:
- Always say "element" not "tag", "node", or "component" (unless specifically differentiating)
- Always say "function" not "method" (unless specifically discussing methods)
- Always say "variable" not "identifier" (unless specifically discussing identifiers)

### Provide Concrete Examples

**Before Abstract Explanation**:

```html
<!-- First, show a concrete example -->
<h1>Main Heading</h1>
<p>This is a paragraph of text.</p>
```

**Then Explain**:

> The code above creates a heading using the `<h1>` tag and a paragraph using the `<p>` tag. Headings are used for titles, while paragraphs contain regular text.

### Avoid Idioms and Metaphors

**DON'T**:
- "Hit the ground running"
- "Keep your eye on the ball"
- "Think outside the box"

**DO**:
- "Start working quickly"
- "Stay focused on the task"
- "Consider alternative approaches"

---

## Visual Structure

### Use Clear Headings

Create a visual hierarchy with H1, H2, H3 tags.

**Example**:

```markdown
# Main Title (H1)

## Section Title (H2)

### Subsection Title (H3)

Content here...
```

**Why it matters**: Clear headings help students scan and navigate content.

### Employ Lists Extensively

#### Numbered Lists for Sequences

Use numbered lists when order matters:

1. Create the HTML file
2. Add the basic structure
3. Add content to the body
4. Save and test the file

#### Bulleted Lists for Options

Use bulleted lists when order doesn't matter:

- You can use Chrome, Firefox, Safari, or Edge
- All modern browsers support JavaScript
- Choose the one you're most comfortable with

### Format Code Blocks Clearly

Always specify the language for syntax highlighting:

```javascript
// JavaScript code
let x = 5;
```

```html
<!-- HTML code -->
<h1>Hello</h1>
```

```css
/* CSS code */
body {
    background-color: white;
}
```

### Provide Visual Separation

Use horizontal lines or blank space between sections:

```markdown
# Section 1

Content...

---

# Section 2

Content...
```

---

## Content Presentation

### Provide Step-by-Step Breakdowns

For complex concepts, break them down into smaller pieces:

**Instead of**:
> "Here's how to create a responsive layout using Flexbox."

**Use**:
1. Set the display property to flex
2. Define the flex direction
3. Set the alignment of items
4. Add responsive breakpoints for different screen sizes

Then explain each step in detail.

### Include Validation Checkpoints

After each major section, provide a way to verify understanding:

> **Check Your Work**:
> - [ ] You've created an HTML file with the correct structure
> - [ ] You've added a heading and a paragraph
> - [ ] When you open the file in a browser, you see your content displayed

### Offer Multiple Explanation Approaches

When possible, explain concepts in multiple ways:

1. **Analogy**: Relate to something familiar
2. **Concrete Example**: Show actual code or behavior
3. **Technical Explanation**: Provide the formal definition

**Example**:

> **Analogy**: Think of a variable like a box where you can store information. You can put things in the box, take them out, or replace them with new things.

> **Concrete Example**: In JavaScript, you might create a variable like this:
> ```javascript
> let userName = "Alice";
> ```
> This creates a box (variable) named `userName` and puts the value "Alice" inside it.

> **Technical Explanation**: A variable is a named storage location in memory that holds a value. You can use the variable name to access or modify the value.

### Include Troubleshooting Sections

After explaining how to do something, explain what might go wrong:

> **Common Issues**:
>
> **Problem**: My code isn't working.
> **Solution**: Check that you've saved the file and that your browser has refreshed.
>
> **Problem**: I see an error message.
> **Solution**: Read the error message carefully. It usually tells you exactly what's wrong and where.

---

## Code Examples

### Make Code Runnable

Ensure all code examples are self-contained and can be executed:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Example</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is a complete, runnable example.</p>
</body>
</html>
```

### Add Extensive Comments

Comment every non-obvious line of code:

```javascript
// Create a variable named 'count' and set it to 0
let count = 0;

// Increment the count by 1
count = count + 1;

// Print the current value of count to the console
console.log(count);  // Output: 1
```

### Show Input/Output

Demonstrate what code produces:

**Code**:
```javascript
let x = 5;
let y = 3;
console.log(x + y);
```

**Output**:
```
8
```

### Explain Non-Obvious Operations

Don't assume students know what each line does:

```javascript
// This line creates an array (a list) of numbers
let numbers = [1, 2, 3, 4, 5];

// The reduce method goes through each number and adds them together
let sum = numbers.reduce((total, num) => total + num, 0);

console.log(sum);  // Output: 15
```

### Create Scaffolded Code

For exercises, provide code with blanks for students to fill:

```javascript
// Create a variable named 'userName' and set it to "Alice"
let userName = __________;

// Print a greeting to the console
console.log("Hello, " + __________ + "!");
```

---

## Instructions & Tasks

### Use Numbered Lists for Sequential Steps

**DON'T**:
> "Create a webpage with a header, content section, and footer."

**DO**:
1. Create the HTML document structure
2. Add a header section
3. Add a content section
4. Add a footer section

### Be Specific About File Names and Locations

**DON'T**:
> "Create an HTML file."

**DO**:
> Create a new file named `index.html` in the `W1/assignments/` folder.

### Include Expected Outcomes

After giving instructions, tell students what they should see:

> After completing this task, you should see a webpage with a blue heading that says "My Website" and a paragraph that says "Welcome to my site."

### Provide Validation Steps

Give students a way to verify their work:

> **Verify Your Work**:
> 1. Double-click the `index.html` file to open it in your browser
> 2. Check that you see a heading and a paragraph
> 3. Right-click and select "Inspect" to verify the HTML structure

### Offer Troubleshooting Tips

Address common issues:

> **Troubleshooting**:
>
> **Problem**: The file won't open in my browser.
> **Solution**: Make sure you've saved the file with the `.html` extension. Sometimes computers hide file extensions, so you might have saved it as `index.html.txt` without realizing it.

---

## Common Challenges & Solutions

### Challenge: Information Overload

**Symptoms**: Students feel overwhelmed by too much information at once.

**Solutions**:
- Break content into smaller sections
- Use headings to create visual structure
- Use bulleted lists to make content scannable
- Provide summaries after each section

### Challenge: Ambiguous Instructions

**Symptoms**: Students aren't sure what to do or how to do it.

**Solutions**:
- Use explicit, specific language
- Include examples showing exactly what to do
- Provide file names and locations
- Show expected outcomes

### Challenge: Lack of Feedback

**Symptoms**: Students can't tell if they're doing it correctly.

**Solutions**:
- Include success criteria for each task
- Provide checkpoints to verify progress
- Show expected output for code examples
- Include troubleshooting sections

### Challenge: Abstract Concepts

**Symptoms**: Students struggle to understand theoretical concepts.

**Solutions**:
- Provide concrete examples first
- Use analogies to relate to familiar concepts
- Break down abstract concepts into concrete parts
- Offer multiple explanation approaches

---

## Checklist

Before finalizing any content, verify:

### Language & Communication

- [ ] All instructions are explicit and unambiguous
- [ ] Concrete examples precede abstract explanations
- [ ] Terminology is consistent throughout
- [ ] No idioms, metaphors, or vague expressions

### Visual Structure

- [ ] Clear headings (H1, H2, H3) create a hierarchy
- [ ] Numbered lists are used for sequential steps
- [ ] Bulleted lists are used for options or unordered items
- [ ] Code blocks specify the language for syntax highlighting
- [ ] Visual separation between sections (horizontal lines or blank space)

### Content Presentation

- [ ] Complex tasks are broken into numbered steps
- [ ] Success criteria are clearly defined
- [ ] Validation checkpoints are included
- [ ] Multiple explanation approaches are provided when possible
- [ ] Troubleshooting information is included

### Code Examples

- [ ] All code examples are runnable and self-contained
- [ ] Code includes extensive inline comments
- [ ] Input/output examples are shown
- [ ] Non-obvious operations are explained
- [ ] Scaffolded code is provided for exercises

### Instructions & Tasks

- [ ] File names and locations are specified
- [ ] Expected outcomes are included
- [ ] Validation steps are provided
- [ ] Common issues and solutions are addressed

### Overall Accessibility

- [ ] Content is organized logically
- [ ] Progression from simple to complex
- [ ] Students can verify their understanding
- [ ] Support is provided for common challenges

---

## Additional Resources

- **Main Guidelines**: [CLAUDE.md](../CLAUDE.md) - Comprehensive content creation guidelines
- **Contributing**: [contributing.md](contributing.md) - How to contribute materials
- **Setup Guide**: [setup.md](setup.md) - Getting started with the repository

---

**Remember**: The goal is to create materials that are clear, accessible, and supportive for students with diverse learning needs. When in doubt, err on the side of being more explicit, providing more examples, and breaking things down further.

**Last Updated**: 2026-03-16

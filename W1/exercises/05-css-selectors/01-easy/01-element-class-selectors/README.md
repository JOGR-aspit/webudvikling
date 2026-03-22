# CSS Exercise: Element & Class Selectors

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Write element selectors from scratch (tag name only)
- [ ] Write class selectors using the `.` prefix
- [ ] Write complete CSS rules (selector + declarations)
- [ ] Understand the difference between element and class selectors

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Selectors" lesson (08-css-selectors.md)
- Completed at least one CSS Fundamentals exercise
- Understand the basic structure of a CSS rule

## What You'll Build

You will style a simple webpage by writing CSS selectors AND declarations. The HTML is already written for you. Your job is to:

1. **Write the selector** - Choose the right selector type
2. **Write the declarations** - Add the CSS properties inside the curly braces

This is different from the previous exercises - now YOU write the selectors!

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write everything from scratch.

2. **Style all h1 elements**
   - Selector: Write `h1` (just the tag name, no `.` or `#`)
   - Declarations: `color: navy;` and `font-size: 32px;`

3. **Style all paragraphs**
   - Selector: Write `p` (just the tag name)
   - Declarations: `color: #333333;` and `line-height: 1.6;`

4. **Style elements with class "highlight"**
   - Selector: Write `.highlight` (with the `.` prefix!)
   - Declarations: `background-color: yellow;` and `padding: 5px;`

5. **Style elements with class "link"**
   - Selector: Write `.link` (with the `.` prefix!)
   - Declarations: `color: blue;` and `text-decoration: none;`

## Selector Syntax Reminder

| Selector Type | Syntax | Example | Targets |
|---------------|--------|---------|----------|
| **Element** | `tagname` | `h1 { }` | All `<h1>` elements |
| **Class** | `.classname` | `.highlight { }` | All elements with `class="highlight"` |

**Key difference**: Class selectors need the `.` (dot) prefix!

## Expected Result

When you complete this exercise, your page will look like this:

```
WELCOME
(Navy blue, 32px, large heading)

This is the introduction.
(Dark grey text, better line spacing)

This is regular text.
(Dark grey text, same as above)

THIS IS HIGHLIGHTED.
(Yellow background, some padding, stands out)

Click here
(Blue link, no underline)
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the heading**:
   - "Welcome" should be **navy blue**
   - It should be **larger** (32px instead of default)

4. **Verify the paragraphs**:
   - All paragraph text should be **dark grey** (not pure black)
   - Lines should have **more spacing** (easier to read)

5. **Verify the highlight**:
   - The paragraph "This is highlighted" should have a **yellow background**
   - It should have **small padding** around the text

6. **Verify the link**:
   - "Click here" should be **blue**
   - It should have **no underline**

## Common Issues

### Issue: My CSS selectors aren't working

**Possible cause:** You might have forgotten the `.` prefix for class selectors.

**Fix:**
- Element selectors: just the tag name (`h1`, `p`, `a`)
- Class selectors: need the dot prefix (`.highlight`, `.link`)

```css
/* WRONG - this targets <highlight> tags (which don't exist!) */
highlight { }

/* RIGHT - this targets elements with class="highlight" */
.highlight { }
```

### Issue: The h1 isn't navy

**Possible cause:** You might have written `color: navy blue;` instead of `color: navy;`.

**Fix:** CSS color names don't have spaces. Use `navy` not `navy blue`.

### Issue: Nothing is styled

**Possible cause:** You might have forgotten to link the CSS file, or there's a syntax error.

**Fix:**
1. Check that `index.html` has `<link rel="stylesheet" href="styles.css">`
2. Check that every declaration ends with a semicolon `;`
3. Check that every rule has opening `{` and closing `}` braces

### Issue: I wrote `.highlight` but it's not working

**Possible cause:** The HTML might use a different class name, or you have a typo.

**Fix:** Check the HTML file - look for `class="highlight"`. Make sure your CSS matches exactly (including capitalization).

## Time Estimate

~10 minutes
